# Changelog

All notable changes to this project will be documented in this file.

## [0.2.1](https://github.com/defenseunicorns/uds-k3d/compare/v0.2.0...v0.2.1) (2023-12-07)


### Bug Fixes

* update policy value and document using minio ([#26](https://github.com/defenseunicorns/uds-k3d/issues/26)) ([b564248](https://github.com/defenseunicorns/uds-k3d/commit/b564248e739ee016085d7ae101d0cb7dd6955b75))

## [0.2.0](https://github.com/defenseunicorns/uds-k3d/compare/v0.1.14...v0.2.0) (2023-12-04)


### Features

* use uds-dev-stack for all namespaces ([#23](https://github.com/defenseunicorns/uds-k3d/issues/23)) ([3e80c89](https://github.com/defenseunicorns/uds-k3d/commit/3e80c890d4649f0f48675a266b306dff68934c40))


### Miscellaneous

* **deps:** update docker image rancher/local-path-provisioner to v0.0.26 ([#16](https://github.com/defenseunicorns/uds-k3d/issues/16)) ([e8a4a63](https://github.com/defenseunicorns/uds-k3d/commit/e8a4a63aa61b17a790cebe57e60d02ec9912351f))

## [0.1.14](https://github.com/defenseunicorns/uds-k3d/compare/v0.1.13...v0.1.14) (2023-11-30)


### Miscellaneous

* **deps:** update dependency defenseunicorns/zarf to v0.31.3 ([#20](https://github.com/defenseunicorns/uds-k3d/issues/20)) ([758ad7c](https://github.com/defenseunicorns/uds-k3d/commit/758ad7c57da2d5cb930ca48e5becfddd3d5054cc))
* make release-please less stupid ([#18](https://github.com/defenseunicorns/uds-k3d/issues/18)) ([01b36ae](https://github.com/defenseunicorns/uds-k3d/commit/01b36aecb35ffd5433647f2dffe82bb59bf676d1))

## [0.1.13](https://github.com/defenseunicorns/uds-k3d/compare/v0.1.12...v0.1.13) (2023-11-29)


### Features

* add minio and local-path-rwx to dev stack and refactor dev stack manifests into helm chart ([#10](https://github.com/defenseunicorns/uds-k3d/issues/10)) ([3648fa0](https://github.com/defenseunicorns/uds-k3d/commit/3648fa0c219f40b07a2d8ce7ebebe0afe9c22cd2))


### Miscellaneous

* **deps:** replace docker image k8s.gcr.io/pause to 3.9 ([#13](https://github.com/defenseunicorns/uds-k3d/issues/13)) ([0235f05](https://github.com/defenseunicorns/uds-k3d/commit/0235f050bd355e21372c90e3f1cd914b0e0479f3))
* **deps:** update dependency defenseunicorns/zarf to v0.31.2 ([#14](https://github.com/defenseunicorns/uds-k3d/issues/14)) ([3e433f4](https://github.com/defenseunicorns/uds-k3d/commit/3e433f48e2269d78ed51634e580c69ca44e4401a))
* **deps:** update docker image k8s.gcr.io/pause to v3.9 ([#17](https://github.com/defenseunicorns/uds-k3d/issues/17)) ([c3b6e0c](https://github.com/defenseunicorns/uds-k3d/commit/c3b6e0c29a5d77917ba38eafbdd51436bcda0f37))
* update renovate config ([#11](https://github.com/defenseunicorns/uds-k3d/issues/11)) ([d3a44bc](https://github.com/defenseunicorns/uds-k3d/commit/d3a44bcbd043357b8fbbb5794a771d3452b3f286))

## [0.1.12](https://github.com/defenseunicorns/uds-k3d/compare/v0.1.11...v0.1.12) (2023-11-09)


### Features

* use daemonset for machineid instead of docker mount ([#8](https://github.com/defenseunicorns/uds-k3d/issues/8)) ([2a49404](https://github.com/defenseunicorns/uds-k3d/commit/2a494044e71228a29cdb102d3f85e53dd4873f35))

## [0.1.11](https://github.com/defenseunicorns/uds-k3d/compare/v0.1.10...v0.1.11) (2023-11-02)


### Features

* publish multi/arm/amd packages for UDS CLI happiness ([#6](https://github.com/defenseunicorns/uds-k3d/issues/6)) ([861ce6d](https://github.com/defenseunicorns/uds-k3d/commit/861ce6d4c76edc283b8737929f7a071aecce1fb3))

## [0.1.10](https://github.com/defenseunicorns/uds-k3d/compare/v0.1.9...v0.1.10) (2023-10-30)


### Bug Fixes

* add k3d to test workflow ([ae46119](https://github.com/defenseunicorns/uds-k3d/commit/ae461191641f7151259fa48deea88fee3dfae70d))


### Miscellaneous

* add codeowners ([87f67ea](https://github.com/defenseunicorns/uds-k3d/commit/87f67ead297ed78634ba65fd9fcab1d6a7a9dfd5))

## [0.1.9](https://github.com/defenseunicorns/uds-k3d/compare/v0.1.8...v0.1.9) (2023-10-30)


### Features

* deploy to common 🦄 shorthand repo ([579f0b8](https://github.com/defenseunicorns/uds-k3d/commit/579f0b8fb4f0aa93f03763d1e5f56e7fe4cd842c))


### Miscellaneous

* fix readme release annotation ([d0ea198](https://github.com/defenseunicorns/uds-k3d/commit/d0ea1987e3a69f06dece471eb96a51bbdf232ff2))

## [0.1.8](https://github.com/defenseunicorns/uds-k3d/compare/v0.1.7...v0.1.8) (2023-10-30)


### Bug Fixes

* package release workflow ([efa0d22](https://github.com/defenseunicorns/uds-k3d/commit/efa0d228b4345c6c4cd9170cd35a43c43fa7c7dd))

## [0.1.7](https://github.com/defenseunicorns/uds-k3d/compare/v0.1.6...v0.1.7) (2023-10-30)


### Features

* initial release ([f66ef5f](https://github.com/defenseunicorns/uds-k3d/commit/f66ef5f5283c31c7bd3ca48610775f032a4f9af1))


### Miscellaneous

* release config work ([c3523dc](https://github.com/defenseunicorns/uds-k3d/commit/c3523dc9d3e2ad74f308b3c786c021a51c6fb29f))

## [0.0.0] - YYYY-MM-DD
PRE RELEASE

### Added
- Initial CHANGELOG.md
- CODEOWNERS
- CONTRIBUTING.md
- DEVELOPMENT_MAINTENANCE.md
- LICENSE
- READEME.md
- zarf.yaml
