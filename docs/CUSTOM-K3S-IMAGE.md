# Custom k3s Image

`uds-k3d` publishes a custom k3s image at `ghcr.io/defenseunicorns/uds-k3d/k3s` that extends the standard `rancher/k3s` image with glibc and OpenSSL libraries. This image is the default for `uds-k3d` deployments.

## Why It Exists

The standard `rancher/k3s` image is Alpine-based and uses musl libc. FIPS CNI plugins such as `istio-install-cni-fips` are dynamically linked against glibc and require the glibc ELF interpreter (`ld-linux-*.so`) plus `libcrypto.so.3` (loaded at runtime via Go's opensslcrypto backend). On a musl-only image, these binaries fail to start.

The custom image solves this by keeping the Alpine k3s base intact and copying only the required libraries from `cgr.dev/chainguard/wolfi-base` (a free, publicly accessible Chainguard image). No Alpine packages are modified or replaced.

Libraries added:

| Library | Purpose |
|---|---|
| `ld-linux-*.so` | glibc ELF interpreter, required to exec glibc-linked binaries |
| `libc.so.6` | glibc C runtime |
| `libdl.so.2` | compat stub (merged into libc since glibc 2.34) |
| `libpthread.so.0` | compat stub (merged into libc since glibc 2.34) |
| `libcrypto.so.3` | OpenSSL, dlopen'd at runtime by Go's opensslcrypto backend |

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

This repo intentionally stays n-1 on k3s (one minor version behind latest). The `allowedVersions: "<1.36"` constraint in `renovate.json` enforces this; update it manually when adopting a new minor version.

All k3s references track the upstream `k3s-io/k3s` GitHub releases directly, so version bumps come in a **single PR** that updates `tasks.yaml`, `build-test.yaml`, and `zarf.yaml`'s `K3D_IMAGE` default together. CI passes because both the connected and airgap builds construct the custom image locally, with no GHCR pull during CI. After the PR merges, `publish-image.yaml` triggers and publishes the new image to GHCR.

The airgap package builds the custom k3s image locally during `zarf package create` using the version from `tasks.yaml`, so it has no GHCR dependency at package creation time.

`cgr.dev/chainguard/wolfi-base` (the glibc source) is grouped with k3s in Renovate since it directly affects the published image artifact.
