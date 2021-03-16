# DH-Trino

This repo contains our OpenShift templates for deploying our Trino
cluster. Trino is the Open Source project of Starburst trino.

## Components in this repo

This repo contains deployment artifacts for all components associated with
the internal Data Hub's trino deployment. The list of components deployed
are the following:

  1. PostgreSQL database.
  2. Hive Metastore.
  3. Trino Coordinator and workers.

The deployment instructions that follow deploy all of the above components.

## Deployment Instructions

### Deploy Manually in Dev

Run the following commands to deploy the cluster to your environment.
```
oc new-project dh-dev-trino
oc project dh-dev-trino
kustomize build trino/overlays/dev/ --enable_alpha_plugins | oc -n dh-dev-trino apply -f -
```

## Further Documentation

### Installation Issues
