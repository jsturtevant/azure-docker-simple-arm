# Simple Arm Template for Docker

To deploy:

```
az login
az account set --subscription {subscription-id}
az group create --name dockerabc --location eastus

az group deployment create --name docker2 --resource-group dockerabc --template-file DockerOnUbuntuServer.json --parameters  '{"adminUsername": {"value": "jsturtevant"}, "adminPassword": {"value": "@234567Asdfgh"},"vmName": {"value": "dockerjs-swarm2"}}'
 ```