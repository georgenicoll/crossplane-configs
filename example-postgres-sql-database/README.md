# Crossplane docs example - CloudSQLInstance

See https://crossplane.io/docs/v1.6/getting-started/create-configuration.html

## Build it...

```
kubectl crossplane build configuration
```

## Push to docker hub

NOTE:  following assumes only a single `.xpkg` file in the directory

```
kubectl crossplane push configuration georgenicoll/example-gcp-postgres-sql-database
```

## Install

```
kubectl crossplane install configuration georgenicoll/example-gcp-postgres-sql-database:latest
# ... and wait for deployment to go healthy
watch kubectl get pkg
```

Then continue following 'Get GCP Account Keyfile' here:  https://crossplane.io/docs/v1.6/getting-started/install-configure.html

## Undeploy

```
kubectl delete ???/example-gcp-postgres-sql-database
```
