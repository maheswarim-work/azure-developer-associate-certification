# Exercise: Create a static HTML web app by using Azure Cloud Shell

```bash
mkdir htmlapp
cd htmlapp
git clone https://github.com/Azure-Samples/html-docs-hello-world.git
resourceGroup=$(az group list --query "[].{id:name}" -o tsv)
appName=az204app$RANDOM
echo $resourceGroup
echo $appName
cd html-docs-hello-world
az webapp up -g $resourceGroup -n $appName --html
```

{
"app_url": "https://<myAppName>.azurewebsites.net",
"location": "westeurope",
"name": "<app_name>",
"os": "Windows",
"resourcegroup": "<resource_group_name>",
"serverfarm": "appsvc_asp_Windows_westeurope",
"sku": "FREE",
"src_path": "/home/<username>/demoHTML/html-docs-hello-world ",
< JSON data removed for brevity. >
}