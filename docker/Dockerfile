# Copyright 2026 Defense Unicorns
# SPDX-License-Identifier: AGPL-3.0-or-later OR LicenseRef-Defense-Unicorns-Commercial

# Custom k3s image with glibc and OpenSSL for FIPS CNI compatibility.
#
# The default rancher/k3s image is Alpine-based (musl libc). FIPS CNI plugins
# (e.g. istio-install-cni-fips from cgr.dev) are dynamically linked against glibc
# and require dlopen("libcrypto.so.3") at runtime via Go's opensslcrypto backend.
#
# We keep the Alpine k3s base intact and copy only the required glibc and OpenSSL
# libraries from cgr.dev/chainguard/wolfi-base (free, publicly accessible).
# Wolfi places libs in /usr/lib/ (no arch-specific subdir), which is a default
# search path for the glibc dynamic linker.

# K3S_TAG has no default — callers must pass --build-arg K3S_TAG=<version>.
ARG K3S_TAG
# Pinned to a digest for reproducible builds. Renovate manages this via the
# built-in Docker manager (ARG followed by FROM ${VAR} pattern).
ARG WOLFI_IMAGE="cgr.dev/chainguard/wolfi-base:latest@sha256:1af610c4a70668dad46159ee178b20378c79a49b554f76405670fc442d30183a"

FROM ${WOLFI_IMAGE} AS wolfi
FROM rancher/k3s:${K3S_TAG}

# Copy glibc runtime libraries from Wolfi.
# The ELF interpreter filename differs by architecture (ld-linux-x86-64.so.2 vs
# ld-linux-aarch64.so.1), so use a glob to pick up whichever the platform ships.
COPY --from=wolfi /usr/lib/ld-linux-*.so* /usr/lib/
# libdl.so.2 and libpthread.so.0 are compat stubs since glibc 2.34 (both merged
# into libc.so.6). Included for backward compatibility with binaries that link
# against them explicitly.
COPY --from=wolfi \
    /usr/lib/libc.so.6 \
    /usr/lib/libdl.so.2 \
    /usr/lib/libpthread.so.0 \
    /usr/lib/

# Copy OpenSSL — Go's opensslcrypto backend calls dlopen("libcrypto.so.3") at runtime.
# libcrypto.so.3 depends only on libc.so.6 (verified via readelf -d).
COPY --from=wolfi /usr/lib/libcrypto.so.3 /usr/lib/

# Create the ELF interpreter symlinks that glibc-linked binaries expect.
# Symlink paths differ by architecture:
#   amd64: /lib64/ld-linux-x86-64.so.2 and /lib/ld-linux-x86-64.so.2
#   arm64: /lib/ld-linux-aarch64.so.1 (no /lib64 convention on arm64)
ARG TARGETARCH
RUN case "${TARGETARCH}" in \
    amd64) \
        mkdir -p /lib64 && \
        ln -sf /usr/lib/ld-linux-x86-64.so.2 /lib64/ld-linux-x86-64.so.2 && \
        ln -sf /usr/lib/ld-linux-x86-64.so.2 /lib/ld-linux-x86-64.so.2 \
        ;; \
    arm64) \
        ln -sf /usr/lib/ld-linux-aarch64.so.1 /lib/ld-linux-aarch64.so.1 \
        ;; \
    *) echo "Unsupported architecture: ${TARGETARCH}" >&2 && exit 1 ;; \
    esac

# Verify the glibc dynamic linker is functional and libcrypto is present.
# Catches broken symlinks or missing libraries at build time rather than at
# runtime in the cluster.
RUN /usr/lib/ld-linux-*.so* --version 2>&1 | grep -qi "glibc" || \
    (echo "ERROR: glibc ELF interpreter not functional" >&2 && exit 1)
RUN test -f /usr/lib/libcrypto.so.3 || \
    (echo "ERROR: libcrypto.so.3 not found" >&2 && exit 1)
