# Overview
Azure CLI and Azure Powershell's built-in CDN commands did not support creating China CDN endpoints for the moment. 
If you have the requirement, suggest to use ARM template as a workaround. Remember to modify the parameters according to your requirements.

Powershell command goes like:

`New-AzResourceGroupDeployment -Name $deploymentName -ResourceGroupName $resourceGroupName -TemplateFile cdn_create_template.json -TemplateParameterFile china_cdn_create_paramters.json`

Azure CLI command goes like:

`az deployment group create --name ExampleDeployment --resource-group ExampleGroup --template-file cdn_create_template.json --parameters @china_cdn_create_paramters.json`

Make sure to use different deployment names if you want to create endpoints in parallel.