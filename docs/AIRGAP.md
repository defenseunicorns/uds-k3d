# Airgap Flavor

This package can be deployed fully airgapped by using the `airgap` flavor. All of the images required for the `k3d` cluster to spin up are loaded into `docker` using `docker load` before the cluster is created. Then all of the images required for the `uds-dev-stack` are loaded into the `k3d` cluster using `k3d image load`.

## Considerations

The version of `k3s` that is deployed by the `airgap` flavor is static and not configurable. 