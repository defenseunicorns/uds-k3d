# Custom k3s Image

`uds-k3d` publishes a custom k3s image at `ghcr.io/defenseunicorns/uds-k3d/k3s` that extends the standard `rancher/k3s` image with glibc and OpenSSL libraries. This image is the default for `uds-k3d` deployments.

## Why It Exists

The standard `rancher/k3s` image is Alpine-based and uses musl libc. FIPS CNI plugins — such as `istio-install-cni-fips` from Chainguard — are dynamically linked against glibc and require the glibc ELF interpreter (`ld-linux-*.so`) plus `libcrypto.so.3` (loaded at runtime via Go's opensslcrypto backend). On a musl-only image, these binaries fail to start.

The custom image solves this by keeping the Alpine k3s base intact and copying only the required libraries from `cgr.dev/chainguard/wolfi-base` (a free, publicly accessible Chainguard image). No Alpine packages are modified or replaced.

Libraries added:

| Library | Purpose |
|---|---|
| `ld-linux-*.so` | glibc ELF interpreter — required to exec glibc-linked binaries |
| `libc.so.6` | glibc C runtime |
| `libdl.so.2` | compat stub (merged into libc since glibc 2.34) |
| `libpthread.so.0` | compat stub (merged into libc since glibc 2.34) |
| `libcrypto.so.3` | OpenSSL — dlopen'd at runtime by Go's opensslcrypto backend |

ELF interpreter symlinks are created at the conventional paths expected by glibc-linked binaries:

- amd64: `/lib64/ld-linux-x86-64.so.2` and `/lib/ld-linux-x86-64.so.2`
- arm64: `/lib/ld-linux-aarch64.so.1`

## Building Locally

```bash
uds run build-image --set VERSION=<k3s-version>
# e.g.
uds run build-image --set VERSION=v1.34.4-k3s1
```

This builds a single-platform image tagged `ghcr.io/defenseunicorns/uds-k3d/k3s:<version>` for the local architecture.

## Publishing

CI publishes a multi-platform image (`linux/amd64` and `linux/arm64`) to GHCR when changes to `docker/**` or `.github/workflows/publish-image.yaml` are merged to `main`:

```bash
uds run publish-image --set VERSION=<k3s-version>
```

## Renovate Updates

k3s version bumps require two separate Renovate PRs in sequence:

1. **`k3s-image` group PR** — updates the k3s version in `publish-image.yaml` and `build-test.yaml`. When merged, CI rebuilds and publishes the new image to GHCR.
2. **`dev-stack` group PR** — updates `zarf.yaml` and `airgap/k3d/zarf.yaml` to reference the newly published image.

The `tasks.yaml` `VERSION` variable carries a `datasource=docker depName=ghcr.io/defenseunicorns/uds-k3d/k3s` Renovate annotation so Renovate updates it only after the new image is available in GHCR.
