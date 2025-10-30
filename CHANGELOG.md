# Changelog

All notable changes to this project will be documented in this file.

## [0.19.2](https://github.com/defenseunicorns/uds-k3d/compare/v0.19.1...v0.19.2) (2025-10-30)


### Documentation

* handle airgap version ([#292](https://github.com/defenseunicorns/uds-k3d/issues/292)) ([dc423f6](https://github.com/defenseunicorns/uds-k3d/commit/dc423f68c170045771be8e030c3d2ff5fbd03cf7))

## [0.19.1](https://github.com/defenseunicorns/uds-k3d/compare/v0.19.0...v0.19.1) (2025-10-30)


### Miscellaneous

* **deps:** update support-deps to v1.21.1 ([#289](https://github.com/defenseunicorns/uds-k3d/issues/289)) ([e5eca19](https://github.com/defenseunicorns/uds-k3d/commit/e5eca199401815c2a5d8660f55908c4178c22e69))
* move uds-dev-stack to kube-system, cleanup docs ([#291](https://github.com/defenseunicorns/uds-k3d/issues/291)) ([fbb0c1f](https://github.com/defenseunicorns/uds-k3d/commit/fbb0c1fd686b8009a9620a3d3221487837fe05e3))

## [0.19.0](https://github.com/defenseunicorns/uds-k3d/compare/v0.18.0...v0.19.0) (2025-10-27)


### ⚠ BREAKING CHANGES

* downgrade default k3s version to 1.32.5 ([#288](https://github.com/defenseunicorns/uds-k3d/issues/288))

### Bug Fixes

* downgrade default k3s version to 1.32.5 ([#288](https://github.com/defenseunicorns/uds-k3d/issues/288)) ([000104b](https://github.com/defenseunicorns/uds-k3d/commit/000104bced204bb97490030503d6f00d7170bd5a))


### Miscellaneous

* **deps:** update release-please to v4.4.0 ([#286](https://github.com/defenseunicorns/uds-k3d/issues/286)) ([04cc64b](https://github.com/defenseunicorns/uds-k3d/commit/04cc64b969e424b28aad890db65da1870b8cbc23))
* **deps:** update support-deps ([#287](https://github.com/defenseunicorns/uds-k3d/issues/287)) ([73cfba1](https://github.com/defenseunicorns/uds-k3d/commit/73cfba10f6dc28fb5889285f5e6044a072bbe0d5))
* **deps:** update uds-cli to v0.27.16 ([#284](https://github.com/defenseunicorns/uds-k3d/issues/284)) ([f7d3c5a](https://github.com/defenseunicorns/uds-k3d/commit/f7d3c5a0f86cc63f6ee8e6f6770ef4374bb46bf5))

## [0.18.0](https://github.com/defenseunicorns/uds-k3d/compare/v0.17.1...v0.18.0) (2025-10-17)


### Features

* support variable overrides for multicluster ([#281](https://github.com/defenseunicorns/uds-k3d/issues/281)) ([ecac0dd](https://github.com/defenseunicorns/uds-k3d/commit/ecac0ddd95659267f4aab8a0bd2735b63588afa4))


### Miscellaneous

* **deps:** update dev-stack to v1.29.2 ([#279](https://github.com/defenseunicorns/uds-k3d/issues/279)) ([83bea45](https://github.com/defenseunicorns/uds-k3d/commit/83bea45b337a3cdff504d69c03933aa5746b1068))
* **deps:** update support-deps to v0.27.15 ([#276](https://github.com/defenseunicorns/uds-k3d/issues/276)) ([2587ec9](https://github.com/defenseunicorns/uds-k3d/commit/2587ec948d14f815eea63aea3ec1b22bdf5f8289))
* **deps:** update uds-common to v1.20.4 ([#278](https://github.com/defenseunicorns/uds-k3d/issues/278)) ([1969ab2](https://github.com/defenseunicorns/uds-k3d/commit/1969ab2646aba50cef160281245ead62f974bd22))
* **deps:** update uds-common to v1.20.5 ([#282](https://github.com/defenseunicorns/uds-k3d/issues/282)) ([e82c896](https://github.com/defenseunicorns/uds-k3d/commit/e82c8966a2bea1c5bb3a57d5aaa0a810837e6c3d))

## [0.17.1](https://github.com/defenseunicorns/uds-k3d/compare/v0.17.0...v0.17.1) (2025-10-01)


### Bug Fixes

* downgrade to k3s 1.33.1 ([#275](https://github.com/defenseunicorns/uds-k3d/issues/275)) ([e0b9110](https://github.com/defenseunicorns/uds-k3d/commit/e0b911058d6e8eda3fa493be8d066ea504f547fa))


### Miscellaneous

* **deps:** update dev-stack ([#268](https://github.com/defenseunicorns/uds-k3d/issues/268)) ([120ba48](https://github.com/defenseunicorns/uds-k3d/commit/120ba48edc84ec770b00ceef0b259db332c17c65))
* **deps:** update support-deps ([#262](https://github.com/defenseunicorns/uds-k3d/issues/262)) ([62c3e80](https://github.com/defenseunicorns/uds-k3d/commit/62c3e80c40b19dad970d7d927e40b3ffe96c30ae))
* **deps:** update support-deps ([#271](https://github.com/defenseunicorns/uds-k3d/issues/271)) ([561379f](https://github.com/defenseunicorns/uds-k3d/commit/561379f81f86f48456a3774b2319b9d863c91f11))
* **deps:** update support-deps to v1.20.1 ([#270](https://github.com/defenseunicorns/uds-k3d/issues/270)) ([94798a4](https://github.com/defenseunicorns/uds-k3d/commit/94798a4ce10f1aa2b103ad2ef227ffc72fe7a13d))

## [0.17.0](https://github.com/defenseunicorns/uds-k3d/compare/v0.16.0...v0.17.0) (2025-09-03)


### Features

* add debug mode var ([#264](https://github.com/defenseunicorns/uds-k3d/issues/264)) ([476c7e7](https://github.com/defenseunicorns/uds-k3d/commit/476c7e7b4d90435c6bda355d5008bc23d22194b7))
* make ports configurable ([#263](https://github.com/defenseunicorns/uds-k3d/issues/263)) ([c06e215](https://github.com/defenseunicorns/uds-k3d/commit/c06e215cb81ff9d64b048bd0df6cec3b29ef57f1))


### Miscellaneous

* add milestone trigger, docs-shim ([#265](https://github.com/defenseunicorns/uds-k3d/issues/265)) ([372bad2](https://github.com/defenseunicorns/uds-k3d/commit/372bad2d74024cb7a186415b9f86e9a46bb9ccd5))
* **deps:** update dependency defenseunicorns/uds-common to v1.17.1 ([#254](https://github.com/defenseunicorns/uds-k3d/issues/254)) ([aa82d29](https://github.com/defenseunicorns/uds-k3d/commit/aa82d297a594f89b979c822562a9f7bd95fb9bfd))
* **deps:** update nginx to v1.29.1 ([#256](https://github.com/defenseunicorns/uds-k3d/issues/256)) ([366a588](https://github.com/defenseunicorns/uds-k3d/commit/366a588c54c3811d0eec213aed910e0937fdb034))
* **deps:** update release-please action to v4.3.0 ([#259](https://github.com/defenseunicorns/uds-k3d/issues/259)) ([1e3ca0f](https://github.com/defenseunicorns/uds-k3d/commit/1e3ca0fd39c4f75bc071c55234a4135ef5ab1f88))
* **deps:** update support-deps to v1.18.0 ([#260](https://github.com/defenseunicorns/uds-k3d/issues/260)) ([787181a](https://github.com/defenseunicorns/uds-k3d/commit/787181a8d9b44113810f2c8dfeaab33126d26e6a))
* drop deprecated zarf --no-progress flag ([#266](https://github.com/defenseunicorns/uds-k3d/issues/266)) ([815f30a](https://github.com/defenseunicorns/uds-k3d/commit/815f30a4af94a5340b6d651050aa12a2ec76bb74))
* update k3s to 1.33.4 ([#267](https://github.com/defenseunicorns/uds-k3d/issues/267)) ([3ba4303](https://github.com/defenseunicorns/uds-k3d/commit/3ba4303f133ddbb946270ce52b722fcdf917ba42))
* update renovate grouping and rate limits ([#258](https://github.com/defenseunicorns/uds-k3d/issues/258)) ([671090b](https://github.com/defenseunicorns/uds-k3d/commit/671090b71d8243e28aff7b17ef9e4e06441d903a))

## [0.16.0](https://github.com/defenseunicorns/uds-k3d/compare/v0.15.2...v0.16.0) (2025-08-12)


### Features

* add default ulimit nofile for k3d ([#253](https://github.com/defenseunicorns/uds-k3d/issues/253)) ([914d1a1](https://github.com/defenseunicorns/uds-k3d/commit/914d1a1881e626d9c681b966d336d2bee45561d4))


### Miscellaneous

* **deps:** update checkout and download-artifact to v5 ([#251](https://github.com/defenseunicorns/uds-k3d/issues/251)) ([939046b](https://github.com/defenseunicorns/uds-k3d/commit/939046b58772aa96c06a67e3f84e5341d78f8d39))
* **deps:** update dev-stack to v0.0.32 ([#249](https://github.com/defenseunicorns/uds-k3d/issues/249)) ([b36f337](https://github.com/defenseunicorns/uds-k3d/commit/b36f3377036183e8c5fab3ff1581f2ed4b0396fb))
* **deps:** update uds-cli to v0.27.11 ([#252](https://github.com/defenseunicorns/uds-k3d/issues/252)) ([8df2306](https://github.com/defenseunicorns/uds-k3d/commit/8df2306d9b5ecb485deeb5a4f4502b535aa4b7f8))

## [0.15.2](https://github.com/defenseunicorns/uds-k3d/compare/v0.15.1...v0.15.2) (2025-07-29)


### Bug Fixes

* docker volume reference /Users/steven.gettys/go/src/github.com/defenseunicorns/uds-k3d instead of . ([#248](https://github.com/defenseunicorns/uds-k3d/issues/248)) ([c5dfa5b](https://github.com/defenseunicorns/uds-k3d/commit/c5dfa5b559c193ca463fe1df040c3dc21723b367))


### Miscellaneous

* **deps:** update githubactions to v0.27.10 ([#244](https://github.com/defenseunicorns/uds-k3d/issues/244)) ([2ef4564](https://github.com/defenseunicorns/uds-k3d/commit/2ef45643a0ffffb271bfe08b93d6bfc985b548cf))

## [0.15.1](https://github.com/defenseunicorns/uds-k3d/compare/v0.15.0...v0.15.1) (2025-07-25)


### Miscellaneous

* **deps:** update dependency defenseunicorns/uds-common to v1.17.0 ([#242](https://github.com/defenseunicorns/uds-k3d/issues/242)) ([c28c558](https://github.com/defenseunicorns/uds-k3d/commit/c28c558fd98f5602a05681cff454db6b0752cc39))
* revert latest k3s patch versions ([#243](https://github.com/defenseunicorns/uds-k3d/issues/243)) ([68b9e3e](https://github.com/defenseunicorns/uds-k3d/commit/68b9e3e01fd28d7d0a2b14160278fbfbbc036850))

## [0.15.0](https://github.com/defenseunicorns/uds-k3d/compare/v0.14.4...v0.15.0) (2025-07-24)


### Features

* add root domain to nginx config ([#240](https://github.com/defenseunicorns/uds-k3d/issues/240)) ([e84f6c1](https://github.com/defenseunicorns/uds-k3d/commit/e84f6c1f04ef067b06daeb4e28a8bc549514b1dd))

## [0.14.4](https://github.com/defenseunicorns/uds-k3d/compare/v0.14.3...v0.14.4) (2025-07-24)


### Miscellaneous

* **deps:** update dependency defenseunicorns/uds-common to v1.16.4 ([#233](https://github.com/defenseunicorns/uds-k3d/issues/233)) ([5271890](https://github.com/defenseunicorns/uds-k3d/commit/5271890e02e87810b49a8d06ba34e1be6106d54e))
* **deps:** update dev-stack ([#237](https://github.com/defenseunicorns/uds-k3d/issues/237)) ([8aff8f8](https://github.com/defenseunicorns/uds-k3d/commit/8aff8f8645bac0827f39882d7b0100825a24fed5))
* **deps:** update dev-stack ([#239](https://github.com/defenseunicorns/uds-k3d/issues/239)) ([859c685](https://github.com/defenseunicorns/uds-k3d/commit/859c685bf227b381193f1f92be129bdb0fc8dbc2))
* **deps:** update githubactions to v0.27.9 ([#235](https://github.com/defenseunicorns/uds-k3d/issues/235)) ([50f681f](https://github.com/defenseunicorns/uds-k3d/commit/50f681f873757b0d3caeabe87dc46930c009ec81))
* **deps:** update harden-runner to v2.13.0 ([#236](https://github.com/defenseunicorns/uds-k3d/issues/236)) ([a2c439e](https://github.com/defenseunicorns/uds-k3d/commit/a2c439e1e66b5cc9db99959edc2f427e6a030f63))
* **deps:** update k8s-pause to v3.10.1 ([#234](https://github.com/defenseunicorns/uds-k3d/issues/234)) ([3c1d1be](https://github.com/defenseunicorns/uds-k3d/commit/3c1d1be4774296159463c555d248e5950f0157ee))
* **deps:** update uds-cli to v0.27.8 ([#231](https://github.com/defenseunicorns/uds-k3d/issues/231)) ([ac3d6b5](https://github.com/defenseunicorns/uds-k3d/commit/ac3d6b5f6f463ede7f7b2be8bd959dc9d532a0d2))
* update to latest k3s patch versions ([#238](https://github.com/defenseunicorns/uds-k3d/issues/238)) ([10f53a2](https://github.com/defenseunicorns/uds-k3d/commit/10f53a2d92584015e3c68277408f7198f365bfe2))

## [0.14.3](https://github.com/defenseunicorns/uds-k3d/compare/v0.14.2...v0.14.3) (2025-06-30)


### Miscellaneous

* **deps:** update dependency defenseunicorns/uds-common to v1.15.2 ([#218](https://github.com/defenseunicorns/uds-k3d/issues/218)) ([53c23c2](https://github.com/defenseunicorns/uds-k3d/commit/53c23c28be1b9bf0047675f3338ba1a9ff163109))
* **deps:** update dependency defenseunicorns/uds-common to v1.16.0 ([#220](https://github.com/defenseunicorns/uds-k3d/issues/220)) ([21e49b4](https://github.com/defenseunicorns/uds-k3d/commit/21e49b4fe079d259e463985266b467b1cd9d9d47))
* **deps:** update dependency defenseunicorns/uds-common to v1.16.2 ([#224](https://github.com/defenseunicorns/uds-k3d/issues/224)) ([5230385](https://github.com/defenseunicorns/uds-k3d/commit/523038593fc1051c5290f9a46312255fa3037751))
* **deps:** update dependency defenseunicorns/uds-common to v1.16.3 ([#226](https://github.com/defenseunicorns/uds-k3d/issues/226)) ([b7667be](https://github.com/defenseunicorns/uds-k3d/commit/b7667be29309156bec0414e9f7bfe707c9e58cf5))
* **deps:** update githubactions ([#223](https://github.com/defenseunicorns/uds-k3d/issues/223)) ([5372413](https://github.com/defenseunicorns/uds-k3d/commit/53724135866b5e772d974e951b4641b8896ab5a7))
* **deps:** update githubactions to v2.12.1 ([#221](https://github.com/defenseunicorns/uds-k3d/issues/221)) ([9b3c1c9](https://github.com/defenseunicorns/uds-k3d/commit/9b3c1c941811f9fb0cde18191d75fe82d02444be))
* **deps:** update githubactions to v2.12.2 ([#229](https://github.com/defenseunicorns/uds-k3d/issues/229)) ([64a0978](https://github.com/defenseunicorns/uds-k3d/commit/64a0978adf2c5b50efe92dc0c4d8e1706352944e))
* **deps:** update githubactions to v3.11.0 ([#222](https://github.com/defenseunicorns/uds-k3d/issues/222)) ([4b11594](https://github.com/defenseunicorns/uds-k3d/commit/4b11594b95445f8d9bde498a156462f64dc602c9))
* **deps:** update minio to release.2025-06-13t11-33-47z ([#225](https://github.com/defenseunicorns/uds-k3d/issues/225)) ([989238c](https://github.com/defenseunicorns/uds-k3d/commit/989238c8bb4daaff781f87a3e8630bb3ffc48074))
* **deps:** update nginx to v1.29.0 ([#227](https://github.com/defenseunicorns/uds-k3d/issues/227)) ([219d7f1](https://github.com/defenseunicorns/uds-k3d/commit/219d7f1b9d798393da56c94a5c12f0fed5b427e8))
* **deps:** update quay.io/nginx/nginx-unprivileged docker tag to v1.29.0 ([#228](https://github.com/defenseunicorns/uds-k3d/issues/228)) ([bb65f47](https://github.com/defenseunicorns/uds-k3d/commit/bb65f474293fac06feeca1e03ee9a8b75907c62a))

## [0.14.2](https://github.com/defenseunicorns/uds-k3d/compare/v0.14.1...v0.14.2) (2025-06-06)


### Bug Fixes

* change version check to work on all systems ([#215](https://github.com/defenseunicorns/uds-k3d/issues/215)) ([0595696](https://github.com/defenseunicorns/uds-k3d/commit/05956960778022545ef9d794f1dbc978a46f8cd2))


### Miscellaneous

* **deps:** update dependency defenseunicorns/uds-common to v1.15.1 ([#216](https://github.com/defenseunicorns/uds-k3d/issues/216)) ([622509b](https://github.com/defenseunicorns/uds-k3d/commit/622509b122d753525296ed379def083ebd1e6e92))

## [0.14.1](https://github.com/defenseunicorns/uds-k3d/compare/v0.14.0...v0.14.1) (2025-06-04)


### Bug Fixes

* action tags in workflow comments ([#193](https://github.com/defenseunicorns/uds-k3d/issues/193)) ([3425b8b](https://github.com/defenseunicorns/uds-k3d/commit/3425b8b39e0c95349f1b2bf7fd66407f3920a08e))
* **ci:** add maru auth for remote tasks ([#197](https://github.com/defenseunicorns/uds-k3d/issues/197)) ([1248f9d](https://github.com/defenseunicorns/uds-k3d/commit/1248f9ddfc54e8c697d3f6bb44ae912353b17cf9))


### Miscellaneous

* **deps:** update dependency defenseunicorns/uds-common to v1.14.4 ([#195](https://github.com/defenseunicorns/uds-k3d/issues/195)) ([6edd3cf](https://github.com/defenseunicorns/uds-k3d/commit/6edd3cfe79bf6787bc91b310c808138d863cbd8f))
* **deps:** update dependency defenseunicorns/uds-common to v1.14.5 ([#196](https://github.com/defenseunicorns/uds-k3d/issues/196)) ([5243fce](https://github.com/defenseunicorns/uds-k3d/commit/5243fce1b746ca3de1c3764715ec100176eb1849))
* **deps:** update dependency defenseunicorns/uds-common to v1.15.0 ([#203](https://github.com/defenseunicorns/uds-k3d/issues/203)) ([aaa8e26](https://github.com/defenseunicorns/uds-k3d/commit/aaa8e269e455cd833b9999a2b34e4e378cf90edc))
* **deps:** update githubactions to v0.27.4 ([#198](https://github.com/defenseunicorns/uds-k3d/issues/198)) ([a6e9532](https://github.com/defenseunicorns/uds-k3d/commit/a6e9532fc8e9aae75f9f125cfca6d350dc713839))
* **deps:** update githubactions to v0.27.6 ([#207](https://github.com/defenseunicorns/uds-k3d/issues/207)) ([61667d9](https://github.com/defenseunicorns/uds-k3d/commit/61667d97c481b799b22ac6daf3aa50f4756ebeeb))
* **deps:** update metallb to 0.15.0 ([#206](https://github.com/defenseunicorns/uds-k3d/issues/206)) ([610aef9](https://github.com/defenseunicorns/uds-k3d/commit/610aef95c6262cd8c8796dad796490e8401bc046))
* **deps:** update quay.io/minio/mc docker tag to release.2025-05-21t01-59-54z ([#202](https://github.com/defenseunicorns/uds-k3d/issues/202)) ([8e2177b](https://github.com/defenseunicorns/uds-k3d/commit/8e2177bf06298135f4155bffd859237e85589b8c))
* **deps:** update quay.io/minio/minio docker tag to release.2025-05-24t17-08-30z ([#201](https://github.com/defenseunicorns/uds-k3d/issues/201)) ([fc1b5a4](https://github.com/defenseunicorns/uds-k3d/commit/fc1b5a4b83f31bb66e786a423c40e81a263e995e))
* **deps:** update uds-cli to v0.27.5 ([#199](https://github.com/defenseunicorns/uds-k3d/issues/199)) ([29dbef3](https://github.com/defenseunicorns/uds-k3d/commit/29dbef301e26a4ea3fe4a843a0980ac434194020))
* update metallb to 0.15.2, fix grouping in renovate ([#212](https://github.com/defenseunicorns/uds-k3d/issues/212)) ([8045599](https://github.com/defenseunicorns/uds-k3d/commit/8045599ff379b1531a2058cdebcd27bffd6fbb7c))
* update to latest k3s patch versions ([#208](https://github.com/defenseunicorns/uds-k3d/issues/208)) ([e849ba6](https://github.com/defenseunicorns/uds-k3d/commit/e849ba66218da57e859994c2aa10835ec03cf4e9))

## [0.14.0](https://github.com/defenseunicorns/uds-k3d/compare/v0.13.0...v0.14.0) (2025-05-16)


### Features

* `uds-k3d` airgap package flavor ([#176](https://github.com/defenseunicorns/uds-k3d/issues/176)) ([64a0c76](https://github.com/defenseunicorns/uds-k3d/commit/64a0c767f181b2c7442eaadea2bd4955df2d719f))


### Bug Fixes

* artifact download for publish ([#191](https://github.com/defenseunicorns/uds-k3d/issues/191)) ([8a328bf](https://github.com/defenseunicorns/uds-k3d/commit/8a328bf20aa8a66b025a4d821bcdb77bd04a5bbe))
* revert broken releases and fix publishing ([#189](https://github.com/defenseunicorns/uds-k3d/issues/189)) ([60cae00](https://github.com/defenseunicorns/uds-k3d/commit/60cae00fde852cd33d1937856069657724db20ac))
* tag-release workflow publish fix ([#187](https://github.com/defenseunicorns/uds-k3d/issues/187)) ([569e787](https://github.com/defenseunicorns/uds-k3d/commit/569e787061fda54152f3366e8583e5b2bad88f02))


### Miscellaneous

* **deps:** update githubactions ([#182](https://github.com/defenseunicorns/uds-k3d/issues/182)) ([0f6c488](https://github.com/defenseunicorns/uds-k3d/commit/0f6c488b1aeb8a1f137671c74f2f606532bb133d))
* **deps:** update quay.io/frrouting/frr docker tag to v9.1.3 ([#183](https://github.com/defenseunicorns/uds-k3d/issues/183)) ([e164ea4](https://github.com/defenseunicorns/uds-k3d/commit/e164ea4ebf9b3f8640a38263536efaef3196d052))
* **deps:** update quay.io/minio/mc docker tag to v2025 ([#186](https://github.com/defenseunicorns/uds-k3d/issues/186)) ([1969b77](https://github.com/defenseunicorns/uds-k3d/commit/1969b77e834016ac9874913e52f612d1303d0021))
* **main:** release 0.14.0 ([#184](https://github.com/defenseunicorns/uds-k3d/issues/184)) ([c7422dd](https://github.com/defenseunicorns/uds-k3d/commit/c7422dd792d564879148b4ed4e9950ddda6655fc))
* **main:** release 0.14.0 ([#190](https://github.com/defenseunicorns/uds-k3d/issues/190)) ([4055957](https://github.com/defenseunicorns/uds-k3d/commit/405595797693261195d60b2cd0c2296b05f09dc1))
* **main:** release 0.14.1 ([#188](https://github.com/defenseunicorns/uds-k3d/issues/188)) ([ff020a2](https://github.com/defenseunicorns/uds-k3d/commit/ff020a22d2eb3a1dcf8bdcc95e448ce6538e7323))

## [0.13.0](https://github.com/defenseunicorns/uds-k3d/compare/v0.12.3...v0.13.0) (2025-05-14)


### Features

* support for passthrough ([#180](https://github.com/defenseunicorns/uds-k3d/issues/180)) ([f95abb5](https://github.com/defenseunicorns/uds-k3d/commit/f95abb54bf85bcd80f587a8bffdd683b1fc7db30))


### Miscellaneous

* **deps:** update dependency defenseunicorns/uds-common to v1.14.2 ([#171](https://github.com/defenseunicorns/uds-k3d/issues/171)) ([728ec18](https://github.com/defenseunicorns/uds-k3d/commit/728ec18aa0eeb496236c1809282eba2ff7115fc7))
* **deps:** update dependency defenseunicorns/uds-common to v1.14.3 ([#181](https://github.com/defenseunicorns/uds-k3d/issues/181)) ([abd8af4](https://github.com/defenseunicorns/uds-k3d/commit/abd8af4ebb7488055f57fa531390d3a4b4682a01))
* **deps:** update dev-stack to v1.28.0 ([#172](https://github.com/defenseunicorns/uds-k3d/issues/172)) ([e62d52e](https://github.com/defenseunicorns/uds-k3d/commit/e62d52edbb07f9659c25b68b0b7b25e581f8057a))
* **deps:** update githubactions to v0.27.0 ([#168](https://github.com/defenseunicorns/uds-k3d/issues/168)) ([68711c0](https://github.com/defenseunicorns/uds-k3d/commit/68711c0a298537c51ca02ee629688cb261757bfb))
* **deps:** update githubactions to v0.27.1 ([#170](https://github.com/defenseunicorns/uds-k3d/issues/170)) ([0a37cc7](https://github.com/defenseunicorns/uds-k3d/commit/0a37cc735d80c96bad262c17de80877c7e9ae329))
* **deps:** update quay.io/minio/minio docker tag to release.2025-04-22t22-12-26z ([#179](https://github.com/defenseunicorns/uds-k3d/issues/179)) ([5082a6d](https://github.com/defenseunicorns/uds-k3d/commit/5082a6d3779c64aad6e436cf988363a6316c5d0b))
* **deps:** update uds-cli to v0.27.2 ([#175](https://github.com/defenseunicorns/uds-k3d/issues/175)) ([f923702](https://github.com/defenseunicorns/uds-k3d/commit/f923702a552d943a5b3c96636058f77633560a00))
* update k3s to 1.32.4 by default ([#178](https://github.com/defenseunicorns/uds-k3d/issues/178)) ([1e5855b](https://github.com/defenseunicorns/uds-k3d/commit/1e5855b59209d66daab56afcd435516516481219))

## [0.12.3](https://github.com/defenseunicorns/uds-k3d/compare/v0.12.2...v0.12.3) (2025-04-16)


### Bug Fixes

* set temp paths to /tmp dir ([#166](https://github.com/defenseunicorns/uds-k3d/issues/166)) ([8b49db3](https://github.com/defenseunicorns/uds-k3d/commit/8b49db375e1f9d5f85a6a355fb12c279ee6ea345))


### Miscellaneous

* **deps:** update dependency defenseunicorns/uds-common to v1.14.0 ([#163](https://github.com/defenseunicorns/uds-k3d/issues/163)) ([06741f3](https://github.com/defenseunicorns/uds-k3d/commit/06741f333e7b5df215b5617f79d7a5bacbf12fb5))
* **deps:** update dependency defenseunicorns/uds-common to v1.14.1 ([#165](https://github.com/defenseunicorns/uds-k3d/issues/165)) ([f7bc8dd](https://github.com/defenseunicorns/uds-k3d/commit/f7bc8dd7c05c5fddfbda8deb237441085369951b))
* **deps:** update githubactions to v0.26.2 ([#167](https://github.com/defenseunicorns/uds-k3d/issues/167)) ([f1172de](https://github.com/defenseunicorns/uds-k3d/commit/f1172deeda77f71253c51adc72d1e800b9c69c04))

## [0.12.2](https://github.com/defenseunicorns/uds-k3d/compare/v0.12.1...v0.12.2) (2025-04-09)


### Miscellaneous

* **deps:** update dependency defenseunicorns/uds-common to v1.11.2 ([#157](https://github.com/defenseunicorns/uds-k3d/issues/157)) ([5fa71c2](https://github.com/defenseunicorns/uds-k3d/commit/5fa71c20643815bb088e8a78c0551eac2c0aa811))
* **deps:** update dependency defenseunicorns/uds-common to v1.12.0 ([#159](https://github.com/defenseunicorns/uds-k3d/issues/159)) ([1467cca](https://github.com/defenseunicorns/uds-k3d/commit/1467ccad61c3c7a590d7eb4c039f4214836944ac))
* **deps:** update dependency defenseunicorns/uds-common to v1.13.0 ([#161](https://github.com/defenseunicorns/uds-k3d/issues/161)) ([5659569](https://github.com/defenseunicorns/uds-k3d/commit/56595690eca6d2b2964b3df2f6f6f94ba8fc17a6))
* **deps:** update githubactions to v0.26.1 ([#162](https://github.com/defenseunicorns/uds-k3d/issues/162)) ([2289530](https://github.com/defenseunicorns/uds-k3d/commit/228953032ccbf2f11af1628896c4a9409bcafebb))
* update minio, switch to quay nginx ([#160](https://github.com/defenseunicorns/uds-k3d/issues/160)) ([1203d08](https://github.com/defenseunicorns/uds-k3d/commit/1203d08990bd4b0bd745d4aa4591b01ce69ea26c))

## [0.12.1](https://github.com/defenseunicorns/uds-k3d/compare/v0.12.0...v0.12.1) (2025-03-27)


### Miscellaneous

* **deps:** update dependency defenseunicorns/uds-common to v1.11.0 ([#152](https://github.com/defenseunicorns/uds-k3d/issues/152)) ([2114584](https://github.com/defenseunicorns/uds-k3d/commit/21145848327f51ca662a9e86a10b74742fd221fd))
* **deps:** update dependency defenseunicorns/uds-common to v1.11.1 ([#154](https://github.com/defenseunicorns/uds-k3d/issues/154)) ([a14303d](https://github.com/defenseunicorns/uds-k3d/commit/a14303d059462435c84db6bfc4fb6fb566aa8ee8))
* **deps:** update dev-stack to v0.0.31 ([#141](https://github.com/defenseunicorns/uds-k3d/issues/141)) ([c7939e4](https://github.com/defenseunicorns/uds-k3d/commit/c7939e4e1d2f62210ec82a81b497def9b123c661))
* **deps:** update githubactions ([#145](https://github.com/defenseunicorns/uds-k3d/issues/145)) ([d6ae168](https://github.com/defenseunicorns/uds-k3d/commit/d6ae168a7d5fe9c593e3bd148437e6b0e4580feb))
* **deps:** update githubactions ([#146](https://github.com/defenseunicorns/uds-k3d/issues/146)) ([28406dd](https://github.com/defenseunicorns/uds-k3d/commit/28406dd77fc0054ce39f113fb03d760abbd4de71))
* **deps:** update githubactions ([#151](https://github.com/defenseunicorns/uds-k3d/issues/151)) ([bdb2827](https://github.com/defenseunicorns/uds-k3d/commit/bdb2827f8606393f990fb7625cc3916d9195075b))
* **deps:** update githubactions to v4.1.4 ([#148](https://github.com/defenseunicorns/uds-k3d/issues/148)) ([c183858](https://github.com/defenseunicorns/uds-k3d/commit/c183858d42c25a7bbbd5d5d3b5750c620522627c))
* **deps:** update githubactions to v4.1.5 ([#149](https://github.com/defenseunicorns/uds-k3d/issues/149)) ([28ef31e](https://github.com/defenseunicorns/uds-k3d/commit/28ef31e985d2461d8f7a226de50e7a5c470f23a2))
* **deps:** update placeholder ([#143](https://github.com/defenseunicorns/uds-k3d/issues/143)) ([2c5bd26](https://github.com/defenseunicorns/uds-k3d/commit/2c5bd2634fcb237b86a90bc2d7594ddbe0b8c10b))
* **deps:** update rancher/k3s docker tag to v1.32.2 ([#147](https://github.com/defenseunicorns/uds-k3d/issues/147)) ([f8ae305](https://github.com/defenseunicorns/uds-k3d/commit/f8ae3054a08377b10ea9c209d4222bccfd431256))
* **deps:** update rancher/k3s docker tag to v1.32.3 ([#153](https://github.com/defenseunicorns/uds-k3d/issues/153)) ([11ff3a5](https://github.com/defenseunicorns/uds-k3d/commit/11ff3a5e042391241e902a0aac69a1e217c10694))
* switch to cgr busybox ([#155](https://github.com/defenseunicorns/uds-k3d/issues/155)) ([378914a](https://github.com/defenseunicorns/uds-k3d/commit/378914aae77cd17affa9cab31c2c0220e516f624))
* update to k3s 1.31.6 by default ([#150](https://github.com/defenseunicorns/uds-k3d/issues/150)) ([0038feb](https://github.com/defenseunicorns/uds-k3d/commit/0038febf2f9b9644799eec5004f83cd7dfe2e261))
* use k3s 1.31.7 by default ([#156](https://github.com/defenseunicorns/uds-k3d/issues/156)) ([30a0b0f](https://github.com/defenseunicorns/uds-k3d/commit/30a0b0f98748b546df3f89c3f03558e541826d10))

## [0.12.0](https://github.com/defenseunicorns/uds-k3d/compare/v0.11.0...v0.12.0) (2025-01-14)


### ⚠ BREAKING CHANGES

* This package will now strictly enforce a k3d version of 5.7.1 or higher during deployment. While this will cause failures where it wouldn't have before, this aligns with the minimum known working k3d version that is compatible with the package defaults.

### Bug Fixes

* Add a wait after deploying the k3d cluster so that slow internet connections don't get errors ([#138](https://github.com/defenseunicorns/uds-k3d/issues/138)) ([b07531f](https://github.com/defenseunicorns/uds-k3d/commit/b07531f10e534bab4ed35219d21a359b997cf4e2))


### Miscellaneous

* **deps:** update dev-stack to v5.4.0 ([#134](https://github.com/defenseunicorns/uds-k3d/issues/134)) ([58f5dc5](https://github.com/defenseunicorns/uds-k3d/commit/58f5dc55329a5246ee6beb86f1aa299118f072e0))
* **deps:** update rancher/k3s docker tag to v1.32.0 ([#136](https://github.com/defenseunicorns/uds-k3d/issues/136)) ([b358253](https://github.com/defenseunicorns/uds-k3d/commit/b358253ddba39bc5003a6d5f760aa81c8cfc6eb9))
* upgrade k3s version, add k3d version check (https://github.com/defenseunicorns/uds-k3d/pull/140) ([855a99c](https://github.com/defenseunicorns/uds-k3d/commit/855a99c73479d7959774f1d3864a1c9d2236e849))

## [0.11.0](https://github.com/defenseunicorns/uds-k3d/compare/v0.10.1...v0.11.0) (2024-12-18)


### Features

* add ability to override nginx domain ([#129](https://github.com/defenseunicorns/uds-k3d/issues/129)) ([3c0a28c](https://github.com/defenseunicorns/uds-k3d/commit/3c0a28cf3cb02d937ba36d589c9dc40f4082561b))


### Miscellaneous

* **deps:** update dev-stack to v0.14.9 ([#131](https://github.com/defenseunicorns/uds-k3d/issues/131)) ([c07a957](https://github.com/defenseunicorns/uds-k3d/commit/c07a957eb59bd4b304b775be2688ce082441b77d))
* **deps:** update githubactions ([#130](https://github.com/defenseunicorns/uds-k3d/issues/130)) ([93be017](https://github.com/defenseunicorns/uds-k3d/commit/93be01765b7a4845358e524d62b647024f072438))
* **deps:** update githubactions to v0.19.2 ([#126](https://github.com/defenseunicorns/uds-k3d/issues/126)) ([b2fc29d](https://github.com/defenseunicorns/uds-k3d/commit/b2fc29ddcb42afd79b06f6ba9d60bdda51977208))
* **deps:** update githubactions to v1.0.1 ([#132](https://github.com/defenseunicorns/uds-k3d/issues/132)) ([ec8caf5](https://github.com/defenseunicorns/uds-k3d/commit/ec8caf50c53f288e3bbba6e24c1d202b99e1a5d8))
* **deps:** update rancher/k3s docker tag to v1.31.3 ([#127](https://github.com/defenseunicorns/uds-k3d/issues/127)) ([c368a2f](https://github.com/defenseunicorns/uds-k3d/commit/c368a2fc82ca1c0bbbf90ae91f229d1e6713eac6))
* **deps:** update rancher/k3s docker tag to v1.31.4 ([#133](https://github.com/defenseunicorns/uds-k3d/issues/133)) ([f019107](https://github.com/defenseunicorns/uds-k3d/commit/f0191077973bf39f957f18c78ca07a250211f521))

## [0.10.1](https://github.com/defenseunicorns/uds-k3d/compare/v0.10.0...v0.10.1) (2024-11-08)


### Bug Fixes

* workflow permissions for cgr login ([#124](https://github.com/defenseunicorns/uds-k3d/issues/124)) ([8baade6](https://github.com/defenseunicorns/uds-k3d/commit/8baade6b2634d5da9082963f61acf29c269aad49))

## [0.10.0](https://github.com/defenseunicorns/uds-k3d/compare/v0.9.0...v0.10.0) (2024-11-07)


### Features

* add ability to support additional gateway/domain ([#115](https://github.com/defenseunicorns/uds-k3d/issues/115)) ([4c62e6c](https://github.com/defenseunicorns/uds-k3d/commit/4c62e6ce11de8ad39e98e2cb7990fe56f17192da))
* implement graceful, modifiable CoreDNS helm overrides ([#112](https://github.com/defenseunicorns/uds-k3d/issues/112)) ([7fe1876](https://github.com/defenseunicorns/uds-k3d/commit/7fe1876859af840e47ff1acc03b93733748cd4f9))


### Bug Fixes

* port uds-common/setup action ([#121](https://github.com/defenseunicorns/uds-k3d/issues/121)) ([b2ed83f](https://github.com/defenseunicorns/uds-k3d/commit/b2ed83f1fd6b5bb0fa759a39cb41cfef0b36be03))


### Miscellaneous

* allow volumeexpansion in localpath storageclass ([#111](https://github.com/defenseunicorns/uds-k3d/issues/111)) ([4d0fb5c](https://github.com/defenseunicorns/uds-k3d/commit/4d0fb5cae7c7ab0a0f971a4df07e5ab36ec90516))
* **config:** migrate config renovate.json ([#123](https://github.com/defenseunicorns/uds-k3d/issues/123)) ([6b4d5a6](https://github.com/defenseunicorns/uds-k3d/commit/6b4d5a6651fcfa6ffeb8d99c76ee2e323382379e))
* **deps:** update dev-stack ([#114](https://github.com/defenseunicorns/uds-k3d/issues/114)) ([5b4f5ec](https://github.com/defenseunicorns/uds-k3d/commit/5b4f5ec6bf5c98c52b8d3d000ab29ca2e56cc4de))
* **deps:** update githubactions ([#110](https://github.com/defenseunicorns/uds-k3d/issues/110)) ([868ace5](https://github.com/defenseunicorns/uds-k3d/commit/868ace5468e7366f44720812cb1203b6d5a69f66))
* **deps:** update githubactions ([#113](https://github.com/defenseunicorns/uds-k3d/issues/113)) ([0e9cde1](https://github.com/defenseunicorns/uds-k3d/commit/0e9cde12563fced4074157f52cf28e202f07341f))
* **deps:** update githubactions to 11bd719 ([#119](https://github.com/defenseunicorns/uds-k3d/issues/119)) ([3dccbed](https://github.com/defenseunicorns/uds-k3d/commit/3dccbeda12d45eb3a43b0f850a5e98e116854909))
* **deps:** update rancher/k3s docker tag to v1.31.2 ([#120](https://github.com/defenseunicorns/uds-k3d/issues/120)) ([49bb437](https://github.com/defenseunicorns/uds-k3d/commit/49bb4378a5c6c18339dc8e354d3eaf4b4108cd0d))
* **deps:** update uds-common to v0.13.0 ([#107](https://github.com/defenseunicorns/uds-k3d/issues/107)) ([ac3f60d](https://github.com/defenseunicorns/uds-k3d/commit/ac3f60d611e2edf29ca09b404cf70630768fd385))
* update sha/version reference for action/checkout ([#122](https://github.com/defenseunicorns/uds-k3d/issues/122)) ([3e826bf](https://github.com/defenseunicorns/uds-k3d/commit/3e826bfe7462cfe052d12cd0576ea9343f9d6b76))

## [0.9.0](https://github.com/defenseunicorns/uds-k3d/compare/v0.8.0...v0.9.0) (2024-09-17)


### ⚠ BREAKING CHANGES

* add extra port support ([#103](https://github.com/defenseunicorns/uds-k3d/issues/103))

### Features

* add extra port support ([#103](https://github.com/defenseunicorns/uds-k3d/issues/103)) ([9299bc5](https://github.com/defenseunicorns/uds-k3d/commit/9299bc5bf4da40ffd6e30596d01e5a8b50793217))


### Miscellaneous

* **deps:** update dev-stack to v0.0.29 ([#102](https://github.com/defenseunicorns/uds-k3d/issues/102)) ([402b20e](https://github.com/defenseunicorns/uds-k3d/commit/402b20eb32cac3f19b0bc4cbc49e9578a60dca49))
* **deps:** update githubactions ([#94](https://github.com/defenseunicorns/uds-k3d/issues/94)) ([fda8d99](https://github.com/defenseunicorns/uds-k3d/commit/fda8d99ce4925822e2bbfbe2610aa928e306182d))
* **deps:** update githubactions ([#96](https://github.com/defenseunicorns/uds-k3d/issues/96)) ([a730642](https://github.com/defenseunicorns/uds-k3d/commit/a730642d76d2ada2695350ac360a9e3bd8d86847))
* **deps:** update githubactions to v0.12.0 ([#101](https://github.com/defenseunicorns/uds-k3d/issues/101)) ([d110f93](https://github.com/defenseunicorns/uds-k3d/commit/d110f937a2c07e3fc107bcf1a01f2b56ea7a3130))
* **deps:** update metallb to v0.14.8 ([#93](https://github.com/defenseunicorns/uds-k3d/issues/93)) ([b9c61c6](https://github.com/defenseunicorns/uds-k3d/commit/b9c61c625447ce2894a6660c6c207cf5b5258b8c))
* **docs:** graceful k3d shutdown and startup ([#100](https://github.com/defenseunicorns/uds-k3d/issues/100)) ([876a19b](https://github.com/defenseunicorns/uds-k3d/commit/876a19b6984d9269354d6618befc819e3adaa006))
* fix codeowners ([#97](https://github.com/defenseunicorns/uds-k3d/issues/97)) ([6daf597](https://github.com/defenseunicorns/uds-k3d/commit/6daf597ef0872e53c29c431a44aa45e9bbb2d663))
* update k3s test versions, default to 1.30.4 ([#104](https://github.com/defenseunicorns/uds-k3d/issues/104)) ([1aa5cb3](https://github.com/defenseunicorns/uds-k3d/commit/1aa5cb3489e0df6e9115dad1b11baffb55ca7409))

## [0.8.0](https://github.com/defenseunicorns/uds-k3d/compare/v0.7.0...v0.8.0) (2024-07-16)


### Miscellaneous

* **deps:** update actions/checkout digest to 692973e ([#84](https://github.com/defenseunicorns/uds-k3d/issues/84)) ([ff44cce](https://github.com/defenseunicorns/uds-k3d/commit/ff44cce500216ab57f17e01b97e440c9120339ad))
* **deps:** update defenseunicorns/uds-common action to v0.8.0 ([#81](https://github.com/defenseunicorns/uds-k3d/issues/81)) ([f9eab1d](https://github.com/defenseunicorns/uds-k3d/commit/f9eab1dcc0c89e5d425cce1fe89bbb022964e4ba))
* **deps:** update docker/login-action digest to 0d4c9c5 ([#79](https://github.com/defenseunicorns/uds-k3d/issues/79)) ([0fcbb5a](https://github.com/defenseunicorns/uds-k3d/commit/0fcbb5af5e6ba72fb24f718f4625aced8c7ec1d5))
* **deps:** update docker/setup-buildx-action action to v3.4.0 ([#87](https://github.com/defenseunicorns/uds-k3d/issues/87)) ([85cc784](https://github.com/defenseunicorns/uds-k3d/commit/85cc7843a4a90109f7782c47fd9264a6755ea66f))
* **deps:** update googleapis/release-please-action action to v4.1.3 ([#82](https://github.com/defenseunicorns/uds-k3d/issues/82)) ([2ede840](https://github.com/defenseunicorns/uds-k3d/commit/2ede84035b20d652541efefa1eabc50eae7c8024))
* **deps:** update helm release metallb to v0.14.6 ([#90](https://github.com/defenseunicorns/uds-k3d/issues/90)) ([5c510bb](https://github.com/defenseunicorns/uds-k3d/commit/5c510bbac61528096fec2dd38c2a067ece3986d3))
* **deps:** update rancher/local-path-provisioner docker tag to v0.0.28 ([#80](https://github.com/defenseunicorns/uds-k3d/issues/80)) ([d9af211](https://github.com/defenseunicorns/uds-k3d/commit/d9af2113a061b309000ddf6b554680068b176e87))
* **deps:** update registry.k8s.io/pause docker tag to v3.10 ([#78](https://github.com/defenseunicorns/uds-k3d/issues/78)) ([85b6fa4](https://github.com/defenseunicorns/uds-k3d/commit/85b6fa46a7b92c925fefa84b0b16738513704d2b))
* update k3s version, comment out custom image (https://github.com/defenseunicorns/uds-k3d/pull/92) ([9a5776d](https://github.com/defenseunicorns/uds-k3d/commit/9a5776d824cffe75078b3af6abd43de7dabcb2c1))

## [0.7.0](https://github.com/defenseunicorns/uds-k3d/compare/v0.6.0...v0.7.0) (2024-05-23)


### Features

* add custom k3s image ([#55](https://github.com/defenseunicorns/uds-k3d/issues/55)) ([707f7d5](https://github.com/defenseunicorns/uds-k3d/commit/707f7d5b07d9ecf7317439704a3d738b42ff01fb))


### Bug Fixes

* broken validate task ([#71](https://github.com/defenseunicorns/uds-k3d/issues/71)) ([fbe6146](https://github.com/defenseunicorns/uds-k3d/commit/fbe6146536d93f2ebcb89a67176df72bbd44f198))
* buildx for publish image ([#59](https://github.com/defenseunicorns/uds-k3d/issues/59)) ([427af5c](https://github.com/defenseunicorns/uds-k3d/commit/427af5c615d1b8f9f87a68dab97d13ad483e99c3))


### Miscellaneous

* **deps:** pin dependencies ([#66](https://github.com/defenseunicorns/uds-k3d/issues/66)) ([122380a](https://github.com/defenseunicorns/uds-k3d/commit/122380afe200f251eac85f51df1de06cbf082337))
* **deps:** update actions/checkout digest to a5ac7e5 ([#70](https://github.com/defenseunicorns/uds-k3d/issues/70)) ([01422ba](https://github.com/defenseunicorns/uds-k3d/commit/01422ba11eb5b68664691953067c4baa45f03713))
* **deps:** update defenseunicorns/uds-common action to v0.4.2 ([#61](https://github.com/defenseunicorns/uds-k3d/issues/61)) ([c92cf9d](https://github.com/defenseunicorns/uds-k3d/commit/c92cf9d4356f164dead4a58eeeca55e1e612f62d))
* **deps:** update defenseunicorns/uds-common action to v0.4.3 ([#77](https://github.com/defenseunicorns/uds-k3d/issues/77)) ([4960e94](https://github.com/defenseunicorns/uds-k3d/commit/4960e946159d4681c235e5303f9ecb6a69fcbac0))
* **deps:** update defenseunicorns/uds-common digest to a6fba9c ([#72](https://github.com/defenseunicorns/uds-k3d/issues/72)) ([d2da739](https://github.com/defenseunicorns/uds-k3d/commit/d2da739759c5a973c91db0dfee39377881dddfc8))
* **deps:** update docker/setup-buildx-action action to v3.2.0 ([#54](https://github.com/defenseunicorns/uds-k3d/issues/54)) ([e7a639d](https://github.com/defenseunicorns/uds-k3d/commit/e7a639d75f1fc3b8a49f0963a1cb8e4ea7ec0cfc))
* **deps:** update docker/setup-buildx-action action to v3.3.0 ([#68](https://github.com/defenseunicorns/uds-k3d/issues/68)) ([770d3ed](https://github.com/defenseunicorns/uds-k3d/commit/770d3ed9e3905a4a5a9668e6a8051b081893ffe2))
* **deps:** update google-github-actions/release-please-action action to v4 ([#21](https://github.com/defenseunicorns/uds-k3d/issues/21)) ([8e8400d](https://github.com/defenseunicorns/uds-k3d/commit/8e8400de5a83f3702eb94a59471eb2f99cdc21df))
* **deps:** update google-github-actions/release-please-action digest to e4dc86b ([#74](https://github.com/defenseunicorns/uds-k3d/issues/74)) ([27e0723](https://github.com/defenseunicorns/uds-k3d/commit/27e0723c7c5a453ad8fc8c109596d1726ca96508))
* **deps:** update helm release metallb to v0.14.5 ([#62](https://github.com/defenseunicorns/uds-k3d/issues/62)) ([381ec21](https://github.com/defenseunicorns/uds-k3d/commit/381ec21285f770c3186705244c1b20736286d129))
* **deps:** update helm release minio to v5.2.0 ([#63](https://github.com/defenseunicorns/uds-k3d/issues/63)) ([d826b55](https://github.com/defenseunicorns/uds-k3d/commit/d826b550d33c1df6b8899501b8d011d064f9bfa2))
* switch to common renovate config ([#60](https://github.com/defenseunicorns/uds-k3d/issues/60)) ([61e015b](https://github.com/defenseunicorns/uds-k3d/commit/61e015bcb37d811ec0f7cec0c3762d7650190064))
* update codeowners ([#69](https://github.com/defenseunicorns/uds-k3d/issues/69)) ([9f6391d](https://github.com/defenseunicorns/uds-k3d/commit/9f6391d955430e5fb6587f26e63adfc28a15cd59))
* update to latest k3s patches, switch port mapping to standard ports ([#76](https://github.com/defenseunicorns/uds-k3d/issues/76)) ([6339460](https://github.com/defenseunicorns/uds-k3d/commit/63394606f77a8c78c7b47b8c46a7d8a6b88c1157))

## [0.6.0](https://github.com/defenseunicorns/uds-k3d/compare/v0.5.0...v0.6.0) (2024-03-09)


### Features

* rewrite answer as well ([#51](https://github.com/defenseunicorns/uds-k3d/issues/51)) ([baf69f6](https://github.com/defenseunicorns/uds-k3d/commit/baf69f6ceb89d03eec6c1fc68783d72cb4e5ad85))


### Miscellaneous

* **deps:** update defenseunicorns/uds-common action to v0.2.2 ([#50](https://github.com/defenseunicorns/uds-k3d/issues/50)) ([e34753d](https://github.com/defenseunicorns/uds-k3d/commit/e34753d62034b711443707443a9ff8cfd4a96e97))

## [0.5.0](https://github.com/defenseunicorns/uds-k3d/compare/v0.4.0...v0.5.0) (2024-03-01)


### Features

* internal uds.dev resolution ([#46](https://github.com/defenseunicorns/uds-k3d/issues/46)) ([e677483](https://github.com/defenseunicorns/uds-k3d/commit/e67748334ec45ab3a4361eaea9d674d0d9d4a5c8))


### Miscellaneous

* **deps:** update dependency defenseunicorns/zarf to v0.32.4 ([#39](https://github.com/defenseunicorns/uds-k3d/issues/39)) ([0dd4735](https://github.com/defenseunicorns/uds-k3d/commit/0dd4735f93b50cad786459747108190536e544fd))
* fix codeowners file ([#42](https://github.com/defenseunicorns/uds-k3d/issues/42)) ([a108b5f](https://github.com/defenseunicorns/uds-k3d/commit/a108b5f70a43f6dba8e2bc68043e5015d721be94))

## [0.4.0](https://github.com/defenseunicorns/uds-k3d/compare/v0.3.1...v0.4.0) (2024-02-16)


### Features

* add loki user and bucket ([#41](https://github.com/defenseunicorns/uds-k3d/issues/41)) ([509114d](https://github.com/defenseunicorns/uds-k3d/commit/509114d9f2269d141a1dff3b3f37ab9f8fe9e3a4))

## [0.3.1](https://github.com/defenseunicorns/uds-k3d/compare/v0.3.0...v0.3.1) (2024-01-17)


### Bug Fixes

* add zarf var for k3d_extra_args ([#32](https://github.com/defenseunicorns/uds-k3d/issues/32)) ([6f8cb93](https://github.com/defenseunicorns/uds-k3d/commit/6f8cb93cf8d568e12fdf1e217c11905249b730e4))

## [0.3.0](https://github.com/defenseunicorns/uds-k3d/compare/v0.2.1...v0.3.0) (2024-01-10)


### Features

* switch to nginx from haproxy for lower resource use ([#35](https://github.com/defenseunicorns/uds-k3d/issues/35)) ([041226f](https://github.com/defenseunicorns/uds-k3d/commit/041226f59f5bb151679fc0070d81d52357ffcaf4))


### Bug Fixes

* update release process for zarf 0.32 ([#36](https://github.com/defenseunicorns/uds-k3d/issues/36)) ([a8a9acb](https://github.com/defenseunicorns/uds-k3d/commit/a8a9acb28098ae4aa0e7b3c783e86b4f567995b4))


### Miscellaneous

* **deps:** update dependency defenseunicorns/zarf to v0.31.4 ([#29](https://github.com/defenseunicorns/uds-k3d/issues/29)) ([e32e831](https://github.com/defenseunicorns/uds-k3d/commit/e32e831a2f531bc0a257063cd6c5e030d92b42be))
* **deps:** update dependency defenseunicorns/zarf to v0.32.1 ([#34](https://github.com/defenseunicorns/uds-k3d/issues/34)) ([cd8db52](https://github.com/defenseunicorns/uds-k3d/commit/cd8db5287113946683241b941f4006ce26222406))

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
