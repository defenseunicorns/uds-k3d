# UDS Dev Stack

This page documents the developer-focused stack that `uds-k3d` installs to make a single-node k3d cluster behave like a realistic UDS environment.

## What is provided

The UDS Dev Stack provides a number of components to support realistic and simple loadbalancing, DNS resolution, and storage for packages. Most components are deployed in the `kube-system` namespace, following where you might find these components in other clusters, but MinIO is deployed in the `uds-dev-stack` namespace.

Full list of components:

- **MetalLB (controller + IP pool)** — Satisfies Istio LoadBalancer services’ need for routable IPs inside k3d.

- **NGINX DaemonSet (TLS SNI routing)** — Routes incoming traffic based on TLS SNI to the correct MetalLB IPs for admin/tenant (and optional) gateways.

- **CoreDNS override** — Rewrites `*.uds.dev` hostnames to the in-cluster ingress gateway services so pods resolve and route correctly. See: [DNS Assumptions](DNS.md).

- **Local Path Provisioner (RWX)** — Provides a default RWX StorageClass for simple shared-volume needs.

- **Machine ID DaemonSet** — Ensures `/etc/machine-id` exists on nodes for components that expect it.

- **MinIO** — S3-compatible object storage for local development. See: [MinIO Configuration Doc](MINIO.md).

## Customizations

- **Domains**
  - Default domain is `uds.dev`; admin subdomain defaults to `admin.uds.dev`.
  - You can override DNS behavior using the `COREDNS_OVERRIDES` variable for the `uds-dev-stack` chart values. See [DNS Assumptions](DNS.md) for examples and passthrough guidance.

- **NGINX and gateways**
  - `extraPorts` can be exposed and forwarded to the tenant gateway.
  - `customGateway.domainName` adds a second domain routed by NGINX.
  - `passthrough.enabled` plus `passthrough.subdomains` and matching CoreDNS rewrites enable passthrough scenarios.

- **MetalLB IP range**
  - `metallb.ipAddressPool` is set from the computed `BASE_IP` based on the Docker network by default, but can be overridden in chart values to specify a custom range.

- **MinIO Buckets/Users**
  - The upstream MinIO chart provides a number of values to customize buckets and users, as well as API driven ways to interact with the server.
  - See [MinIO Configuration Doc](MINIO.md) for more details.
