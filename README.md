# UDS K3d Environment

> [!IMPORTANT]
> This package should only be used for development and testing purposes. It is not intended for production use and all data is overwritten when the package is re-deployed.

This zarf package serves as a universal dev (local & remote) and test environment for testing [UDS Core](https://github.com/defenseunicorns/uds-core), individual UDS Capabilities, and UDS capabilities aggregated via the [UDS CLI](https://github.com/defenseunicorns/uds-cli). If working with a remote cluster over SSH, you can use SSH port-forwarding to connect:

```console
# Non-standard ports
ssh -N -L 8080:localhost:80 -L 8443:localhost:443 -L 6550:localhost:6550 <your-remote-host>

# Standard ports (requires sudo)
sudo ssh -N -L 80:localhost:80 -L 443:localhost:443 -L 6550:localhost:6550 <your-remote-host>
```

> [!NOTE]
> UDS K3d does also publish an `airgap` flavor that includes a fully airgapped version of k3d. This is still not intended for production use, and does not deploy Zarf's init package. This allows you to initialize the cluster with your own configuration or use it for `zarf dev deploy`.

## Prerequisites

- [UDS CLI](https://uds.defenseunicorns.com/reference/cli/quickstart-and-usage/#install): version 0.27.0 or later
- [K3d](https://k3d.io/#installation): version 5.7.1 or later
- [Docker](https://docs.docker.com/get-docker/) or [Podman](https://podman.io/getting-started/installation) for running K3d

## Deploy

To deploy the standard package:

<!-- x-release-please-start-version -->

`uds zarf package deploy oci://defenseunicorns/uds-k3d:0.19.1`

<!-- x-release-please-end -->

Or for the airgap version append `-airgap`, for example `uds zarf package deploy oci://defenseunicorns/uds-k3d:x.y.z-airgap`.

## Create

This package is published via CI, but can be created locally with the following command:

`uds run build`

Or for the airgap flavor:

`uds run build-airgap-package`

## Remove

To delete your k3d cluster run:

`k3d cluster delete uds` (uds is the default cluster name)

If you deployed the airgap flavor you may also want to clean up the image volume:

`docker volume rm "k3s-airgap-images"`

## Start and Stop

To stop and start an existing UDS K3d cluster gracefully, use the following prior to host hibernation, suspension, restart, or shutoff:

```bash
# to stop the default UDS cluster
k3d cluster stop uds

# to start the default UDS cluster
k3d cluster start uds
```

## Additional Info

You can set extra k3d args by setting the deploy-time Zarf variable `K3D_EXTRA_ARGS`. See below `zarf-config.yaml` example k3d args:

```yaml
package:
  deploy:
    set:
      k3d_extra_args: "--k3s-arg --gpus=1 --k3s-arg --<arg2>=<value>"
```

### Additional Details and Documentation

- [UDS Dev Stack](docs/DEV-STACK.md)
- [Configuring Minio](docs/MINIO.md)
- [DNS Assumptions](docs/DNS.md)
- [Airgap](docs/AIRGAP.md)
