## Preparation
Based on your system, install the CLI tools used in this guide if you don't already have them:
+ kind
+ kubectl
+ Helm

## Create a local Kubernetes cluster
Create a local Kubernetes cluster with the following command:

`kind create cluster --name dgpro`

Next, switch to the new cluster context using the following command:

`kubectl config use-context kind-dgpro`

## Clean
If you don't need the cluster anymore, you can just delete the local KIND cluster:

`kind delete cluster --name dgpro`

## Deploy postgres into the cluster
Let’s have a closer look on helm install command, what each of an argument means: 

`helm install` `-f postgres.yaml` `postgres` `./postgres`

(**install a chart**) - (**override values from a file**) - (**relase name**) - (**base chart name**)

