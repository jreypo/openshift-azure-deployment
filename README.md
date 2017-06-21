# openshift-azure-deployment

This repo contains the ARM template to deploy the infrastrucutre for a fully distributed installation of Openshift Container Platform on Azure. It is based on Microsoft [openshift-container-platform](https://github.com/Microsoft/openshift-container-platform) repository. nodes 

The template will deploy the following virtual machines:
- Bastion host
- 2 OCP master nodes
- etcd cluster with 3 nodes
- 3 infra nodes for the routers, metrics and logs
- 2 infra nodes for the registry
- A number of app nodes

The template will also launch a custom script that will prepare the Bastion host. 

Prerequisites:
- SSH keys
- Azure Key Vault and secret (The procedure is documented on above Microsoft repo)
- Azure Active Directory Service Principal
- Active Red Hat subscription credentials
