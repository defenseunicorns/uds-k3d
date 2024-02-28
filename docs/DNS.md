## Domain Assumptions

One of the core assumptions of the `uds-k3d` package is the use of `uds.dev` as the base domain for your development environment. This assumption is integral to the DNS and network configuration provided by the package. It is based on an existing DNS entry for `*.uds.dev` that resolves to `127.0.0.1`, facilitating local development and testing.

### CoreDNS Override

The package includes a CoreDNS configuration override designed to rewrite requests for `*.uds.dev` to `host.k3d.internal`. This rewrite ensures that any DNS resolution request within the cluster targeting a `*.uds.dev` address will be correctly routed to `host.k3d.internal` which is an internal K3D alias which resolves to the host gateway. 

The outcome of this is a pods in the cluster can resolve domains like sso.uds.dev to an address (not 127.0.0.1) that will ultimately get routed correctly.

### Nginx Configuration

Additionally, the package includes Nginx configuration that assumes the use of `uds.dev` as the base domain. This configuration is tailored to support the development environment setup, ensuring that Nginx correctly handles requests and routes them within the cluster, based on the `uds.dev` domain.