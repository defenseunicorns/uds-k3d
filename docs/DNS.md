# Domain Assumptions

One of the core assumptions of the `uds-k3d` package is the use of `uds.dev` as the base domain for your development environment. This assumption is integral to the DNS and network configuration provided by the package. It is based on an existing DNS entry for `*.uds.dev` that resolves to `127.0.0.1`, facilitating local development and testing.

## CoreDNS Override

[UDS Core](https://github.com/defenseunicorns/uds-core) is assumed to be the main infrastructure and/or testing target in local development; therefore, the DNS resolution assumes the existence of the default admin and tenant Istio gateways.

This package includes a CoreDNS configuration override designed to rewrite requests for `*.uds.dev` to the tenant and admin Istio gateways based on the subdomain, `*.admin.uds.dev` or `*.uds.dev`. This rewrite ensures that any DNS resolution request within the cluster targeting a `*.uds.dev` address will be correctly routed to the correct service mesh gateway.

The outcome of this is a pods in the cluster can resolve domains like sso.uds.dev to an address (not 127.0.0.1) that will ultimately get routed correctly.

To add additional CoreDNS overrides, you can set the `coreDnsOverrides` value by supplying the following to the deployment command:

```bash
--set COREDNS_OVERRIDES="
rewrite {
  name regex (.*\.uds\.dev) host.k3d.internal answer auto
}
"
```

## Nginx Configuration

Additionally, the package includes Nginx configuration that assumes the use of `uds.dev` as the base domain. This configuration is tailored to support the development environment setup, ensuring that Nginx correctly handles requests and routes them within the cluster, based on the `uds.dev` domain.
