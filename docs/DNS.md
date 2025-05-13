# Domain Assumptions

One of the core assumptions of the `uds-k3d` package is the use of `uds.dev` as the base domain for your development environment. This assumption is integral to the DNS and network configuration provided by the package. It is based on an existing DNS entry for `*.uds.dev` that resolves to `127.0.0.1`, facilitating local development and testing.

## CoreDNS Override

[UDS Core](https://github.com/defenseunicorns/uds-core) is assumed to be the main infrastructure and/or testing target in local development; therefore, the DNS resolution assumes the existence of the default admin and tenant Istio gateways.

This package includes a CoreDNS configuration override designed to rewrite requests for `*.uds.dev` to the tenant and admin Istio gateways based on the subdomain, `*.admin.uds.dev` or `*.uds.dev`. This rewrite ensures that any DNS resolution request within the cluster targeting a `*.uds.dev` address will be correctly routed to the correct service mesh gateway. A final rewrite in this package is used as a catch-all by redirecting `*.uds.dev` requests to `host.k3d.internal`.

The outcome of this is a pods in the cluster can resolve domains like sso.uds.dev to an address (not 127.0.0.1) that will ultimately get routed correctly.

You can use Zarf Helm overrides to overwrite the overrides provided by default in this package. To do so you must have Zarf >= v0.33.0. An example of how one might use this override with the default UDS task is as follows:

```bash
# Define the overrides
COREDNS_OVERRIDES=$(cat << 'EOF'
rewrite stop {
  name regex (.*\.uds\.dev) host.k3d.internal answer auto
}
EOF
)

# Now use the variable in your command
uds run --set COREDNS_OVERRIDES="$COREDNS_OVERRIDES"
```

## Nginx Configuration

Additionally, the package includes Nginx configuration that assumes the use of `uds.dev` as the base domain. This configuration is tailored to support the development environment setup, ensuring that Nginx correctly handles requests and routes them within the cluster, based on the `uds.dev` domain.

### Nginx Additional Gateway Support

You can add an additional Gateway to the Nginx configuration by overriding the helm value `customGateway.domainName` with the desired domain name.

For example, to add a custom gateway with the domain `uds2.dev` you would add the following helm overrides for the `uds-dev-stack` chart:

```yaml
customGateway:
  domainName: uds2.dev
```

## Passthrough Gateway Support

To enable passthrough gateway support, you will need to modify two values fields in the `uds-dev-stack` chart:

* `coreDnsOverrides` - Add support to re-write the desired domain to the passthrough-ingressgateway; e.g.,
  ```yaml
  coreDnsOverrides: |
    rewrite stop {
      name regex (.*\.admin\.uds\.dev) admin-ingressgateway.istio-admin-gateway.svc.cluster.local answer auto
    }
    rewrite stop {
      name regex (.*\.uds\.dev) tenant-ingressgateway.istio-tenant-gateway.svc.cluster.local answer auto
    }
    rewrite stop name mysubdomin.uds.dev passthrough-ingressgateway.istio-passthrough-gateway.svc.cluster.local
  ```
  
* `passthrough` - Enable passthrough gateway support by setting the `enabled` field to `true` and add `upstreams` need, this is the unique list of subdomains accessed through the passthrough; e.g.,
  ```yaml
  passthrough:
    enabled: true
    upstreams:
      - mysubdomain
  ```