# Minio Usage Examples

By default, the provided Minio instance provisions a minimal set up that includes a single bucket named `uds` that is accessible by the `uds` user:

```
users:
  - accessKey: uds
    secretKey: uds-secret
    policy: readwrite-username-policy
```

You can port-forward ```kubectl port-forward service/minio 9000:9000 -n uds-dev-stack``` to access the service externally from where you can use any s3 compatible client to configure your buckets or the minio (mc) cli to handle other configurations, users or policy management. Similar functions could be performed in-cluster as well via a Job or other means.

## Quickstart

```bash
# portforward the Minio service
kubectl port-forward service/minio 9000:9000 -n uds-dev-stack

# Get the Minio Admin Credentials
ROOT_PASSWORD=$(kubectl get secret "minio" -n "uds-dev-stack" -o json | jq -r '.data.rootPassword' | base64 --decode)
ROOT_USER=$(kubectl get secret "minio" -n "uds-dev-stack" -o json | jq -r '.data.rootUser' | base64 --decode)
```

### Minio CLI

```bash
# Configure MC Alias
set +o history
mc alias set myalias http://localhost:9000 "$ROOT_USER" "$ROOT_PASSWORD"
set -o history

# Get Buckets
mc ls myalias

# Create a Bucket
mc mb myalias/mybucket

# Create a User (mc cli only)
mc admin user add myalias bob bobs-secret 

# List policies
mc admin policy ls myalias
```

### AWS CLI

```bash
# Configure AWS CLI
set +o history
aws configure set aws_access_key_id "$ROOT_USER"
aws configure set aws_secret_access_key "$ROOT_PASSWORD"
aws configure set region "default"
set -o history

# Get buckets
aws s3 ls --endpoint http://localhost:9000

# Create a bucket
aws s3 mb s3://mybucket --endpoint http://localhost:9000
```

Please see the [reference](https://min.io/docs/minio/linux/reference/minio-mc-admin.html) docs for the mc tool for further administrative usage examples.

## Configuring Minio in This Package

The Minio config provided in this package cannot be modified at deploy time without building a custom version of the package that overrides the values file defaults in ```values/minio-values.yaml```.

Example Values File:

```yaml
# buckets
buckets: 
  - name: mybucket
    policy: none
    purge: false
  - name: otherbucket
  - name: thirdbucket
# users
users:
  - accessKey: console
    secretKey: "console-secret"
    policy: consoleAdmin
  - accessKey: logging
    existingSecret: my-secret
    existingSecretKey: password
    policy: readwrite
```

Please see the Minio chart's [values](https://github.com/minio/minio/blob/master/helm/minio/values.yaml) file for more examples.

## Configuring Minio in a Bundle

If you are building a uds bundle and are using uds-k3d as a base for that bundle, you might want to configure the bundle to be able to customize the minio deployment either at bundle create or deploy time.

### Configure Create Time Minio Overrides

This example will override the default users and buckets provisioned in the minio instance. These are bundle create time overrides.

> **_NOTE:_** Because the underlying fields for `users` and `buckets` are arrays, overriding these options via values will result in the default `uds` user and `uds` bucket not being created.

```yaml
# uds-bundle.yaml

packages:
  - name: uds-k3d-dev
    repository: ghcr.io/defenseunicorns/packages/uds-k3d
    ref: 0.2.0
    overrides:
      uds-dev-stack:
        minio:
          values:
          - path: "users"
            value:
              - accessKey: console
                secretKey: "console-secret"
                policy: consoleAdmin
              - accessKey: logging
                secretKey: "logging-secret"
                policy: readwrite
          - path: "buckets"
            value:
              - name: "loki"  
              - name: "velero"
              - name: "myapp"
              - name: "myotherapp"
```

### Configure Deploy Time Minio Overrides

This example will show how to expose the ability to override the default users, policies, service accounts and buckets provisioned in the minio instance at bundle deploy time.

```yaml
# uds-bundle.yaml

packages:
  - name: uds-k3d-dev
    repository: ghcr.io/defenseunicorns/packages/uds-k3d
    ref: 0.2.0
    overrides:
      uds-dev-stack:
        minio:
          variables:
            - name: buckets
              description: "Set Minio Buckets"
              path: buckets
            - name: svcaccts
              description: "Minio Service Accounts"
              path: svcaccts
            - name: users
              description: "Minio Users"
              path: users
            - name: policies
              description: "Minio policies"
              path: policies
```

Once the bundle has been created the deployer can customize the resources deployed by providing the values to the uds-config.yaml

```yaml
bundle:
  deploy:
    zarf-packages:
      uds-k3d-dev:
        set:
          buckets:
            - name: "myfavoritebucket"
                policy: "public"
                purge: false
          users:
            - accessKey: console
                secretKey: "console-secret"
                policy: consoleAdmin
          policies:
            - name: example-policy
              statements:
                - effect: Allow  # this is the default
                  resources:
                    - 'arn:aws:s3:::${aws:username}*/*'
                  actions:
                    - "s3:AbortMultipartUpload"
                    - "s3:GetObject"
                    - "s3:DeleteObject"
                    - "s3:PutObject"
                    - "s3:ListMultipartUploadParts"
                - resources:
                    - 'arn:aws:s3:::${aws:username}*'
                  actions:
                    - "s3:CreateBucket"
                    - "s3:DeleteBucket"
                    - "s3:GetBucketLocation"
                    - "s3:ListBucket"
                    - "s3:ListBucketMultipartUploads"
```
