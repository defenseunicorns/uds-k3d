# UDS K3d Environment

> [!IMPORTANT]
> This package should only be used for development and testing purposes. It is not intended for production use and all data is overwritten when the package is re-deployed.

This zarf package serves as a universal dev (local & remote) and test environment for testing [UDS Core](https://github.com/defenseunicorns/uds-core), invidual UDS Capabilities, and UDS capabilities aggregated via the [UDS CLI](https://github.com/defenseunicorns/uds-cli). If working with a remote cluster over SSH, you can use SSH port-forwarding to connect:

`ssh -N -L 8080:localhost:80 -L 8443:localhost:443 -L 6550:localhost:6550`

> [!NOTE]
> UDS K3d intentionally does not address airgap concerns for K3d or the load balancer logic deployed in this package. This allows running `zarf init` or deploying a Zarf Init Package via a UDS Bundle after the UDS K3d environment is deployed.

## Prerequisites

- [Zarf](https://docs.zarf.dev/docs/getting-started#installing-zarf) v0.31.0 or later
- [K3d](https://k3d.io/#installation) v5 or later
- [Docker](https://docs.docker.com/get-docker/) or [Podman](https://podman.io/getting-started/installation) for running K3d


## Deploy

`zarf package deploy oci://defenseunicorns/uds-k3d:0.2.0`<!-- {x-release-please-version} -->`-multi`

## Create

This package is published via CI, but can be created locally with the following command:

`zarf package create`

## Remove

`k3d cluster delete uds` (uds is the default cluster name).
