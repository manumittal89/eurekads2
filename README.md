Deploy an AKS cluster running a ds2 services over AKS cluster using a container instances via container image from https://ghcr.io/manumittal89/eurekads2/init-container

This ARM template does the following:

1. Provision a virtual network
2. Provision the AKS cluster
3. Give cluster Network Contributor role to vnet
4. Deploy ACI that runs a script to install all the ds2 services in the AKS cluster 

Note the container image is assumed to be public.

Initiate the deployment by running the following:

#### Manual Steps to initiate the deployment ####

```bash
# create resource group
az group create -n aks-arm -l eastus
# initiate deployment
az deployment group create -n aks-deploy -g aks-arm -f azuredeploy.json
```
