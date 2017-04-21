# Simple Arm Template for Docker

To deploy:

```
az login
az account set --subscription {subscription-id}
az group create --name dockerabc --location eastus
```

In bash:
```
az group deployment create --name docker2 --resource-group dockerabc --template-file DockerOnUbuntuServer.json --parameters  '{"adminUsername": {"value": "dockervmadmin"}, "adminPassword": {"value": "<yourpass>"},"vmName": {"value": "<VMname>"}}'
 ```
 
 On windows (have to escape quotes):
 ```
 az group deployment create --name docker3 --resource-group dockerabc --template-uri https://raw.githubusercontent.com/jsturtevant/azure-docker-simple-arm/master/DockerOnUbuntuServer.json --parameters "{\"adminUsername\": {\"value\": \"dockervmadmin\"}, \"adminPassword\": {\"value\": \"<yourpass>\"}, \"vmName\": {\"value\": \"<VMname>"}}"
 ```
