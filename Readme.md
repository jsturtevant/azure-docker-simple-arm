# Simple Arm Template for Docker

To deploy:

```
az login
az account set --subscription {subscription-id}
az group create --name dockerabc --location eastus

az group deployment create --name docker2 --resource-group dockerabc --template-file DockerOnUbuntuServer.json --parameters  '{"adminUsername": {"value": "dockervmadmin"}, "adminPassword": {"value": "<yourpass>"},"vmName": {"value": "<VMname>"}}'
 ```