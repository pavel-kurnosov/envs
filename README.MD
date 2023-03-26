# Create new IX instance

Use env you want to create a new instance
Copy 0X-interaxo and and update all overrides for credentials and etc
Create new Ix applciation and apply it to the cluster via k

```
k apply -f ./envs/se-prod-01/02-interaxo.yaml -n argocd

```

## Env setup:

Variants consists of common property for location or env type like dev, stage or prod.
Evnts folder contains cluster name and applications that available in the cluster.

## Run interaxo

```
k apply -f ./envs/se-prod-01/00-app-project.yaml -n argocd

```

This will create a app project interaxo that all IX instances will use.

Then you create a 01-interaxo project using

```
k apply -f ./envs/se-prod-01/01-interaxo.yaml -n argocd

```

## Repositories

Create a repository for github and for helm from configuration file.
Config default docker-registry for cluster
