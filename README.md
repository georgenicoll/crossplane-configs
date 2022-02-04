# Crossplane Configs

Various configurations for crossplane.

# GCP Setup

## Install gcp-provider into crossplane

Find out the latest version from https://github.com/crossplane/provider-gcp and replace v0.19.0 in the following command if there is a later one:

```
kubectl crossplane install provider crossplane/provider-gcp:v0.19.0
```

## Set up GCP creds

See: https://github.com/crossplane/crossplane/blob/master/docs/cloud-providers/gcp/gcp-provider.md

# Provision PostgreSQLInstance

Follow the instructions in [example-postgres-sql-database/README.md](example-postgres-sql-database/README.md) first to install georgenicoll/example-gcp-postgres-sql-database to the cluster.

## Provision...

```
kubectl apply -f claim-gcp.yaml
# ... watch the progress with
watch kubectl get postgresqlinstance
```
## Deprovision...

```
kubectl delete -f claim-gcp.yaml
```
