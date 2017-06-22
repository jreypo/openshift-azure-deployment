# openshift-azure-deployment

This repo contains the ARM template to deploy the infrastrucutre for a fully distributed installation of Openshift Container Platform on Azure. It is based on Microsoft [openshift-container-platform](https://github.com/Microsoft/openshift-container-platform) repository. nodes 

The template will deploy the following virtual machines:
- Bastion host
- 1 to 3 OCP master nodes
- etcd cluster with 3 nodes
- 1 to 3 infra nodes for the routers, metrics and logs
- 1 to 3 infra nodes for the registry
- A number of app nodes 

## Prerequisites

- SSH keys
- Azure Key Vault and secret (The procedure is documented on above Microsoft repo)
- Azure Active Directory Service Principal
- Active Red Hat subscription credentials

## TODO

- Fix scripts to prepare the bastion host
- Add scripts to install OCP
- Add conditionals to allow etcd cluster or only masters
- Add conditionals to separate registry on separate infra nodes
- Add the possibility to select between OCP or Openshift Origin

## Deploy Template

Deploy to Azure using Azure Portal: 

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fjreypo%2Fopenshift-azure-deployment%2Fmaster%2Fazuredeploy.json" target="_blank"><img src="http://azuredeploy.net/deploybutton.png"/></a>
<a href="http://armviz.io/#/?load=https%3A%2F%2Fraw.githubusercontent.com%2Fjreypo%2Fopenshift-azure-deployment%2Fmaster%2Fazuredeploy.json" target="_blank">
    <img src="http://armviz.io/visualizebutton.png"/>
</a><br/>