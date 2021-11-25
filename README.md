# Hands on Lab - Creating an Azure function

In this lab we'll be learning how to create our own azure function.

---
### Lab 1
Create an Azure Function with a timer trigger
1. Create a new Azure Functions project in Visual Studio or vs code
> Tip: Quickstart on creating Azure Functions in VS Code: https://docs.microsoft.com/en-us/azure/azure-functions/create-first-function-vs-code-csharp (sample is C# but other languages are on the left in the menu)
2. Create an azure function in VS Code with a timer trigger
> Tip: Timer triggers in Azure Functions: https://docs.microsoft.com/en-us/azure/azure-functions/functions-bindings-timer?tabs=csharp
3. Create an Azure Storage account in your student resource group 
4. Add a Storage output binding
> Tip: Storage account binding: https://docs.microsoft.com/en-us/azure/azure-functions/functions-bindings-storage-blob-output?tabs=csharp
5. Every minute the Azure function should write a file to the storage account containing the date

---
### Lab 2:

Create a local azure function from file new project in Visual Studio or VS Code


0. We'll be using a CosmosDB later on in our labs. since creating one takes 15 minutes create one first in your resourcegroup (using the azure portal). You can use most basic settings. Create one by hand, using cli or arm template (your choice)
1. Create a new Azure Functions project in Visual Studio or vs code
> Tip: creating a new Functions project: https://docs.microsoft.com/en-us/azure/azure-functions/functions-develop-vs-code?tabs=csharp

2. Add a HTTP trigger function that takes 2 numbers as parameters (either in body or URL your choice) and make the function return the result of adding both numbers together.
3. instead of returning the results send the results (HTTP POST) to the following URL: https://webhook.site/a01b6c75-3bc8-4fbc-a0b3-630b4943f4a5

---
### Lab 3:

Trigger on CosmosDB

1. Add a new Azure Function that triggers on changes in the CosmosDB for each new record
2. send the "name" property of each file added to CosmosDB to URL https://webhook.site/a01b6c75-3bc8-4fbc-a0b3-630b4943f4a5

---
### Lab 4:

Deploy your function to Azure

1. Create an Azure function resource in your resource group (using portal, cli or arm template)
2. Deploy the Azure function project to the Azure function on Azure
> tip: Deploying from VS Code: https://docs.microsoft.com/en-us/azure/developer/javascript/tutorial/tutorial-vscode-serverless-node-deploy-hosting

3. Bonus: Deploy your Azure Function project from a Azure DevOps pipeline
> tip: Yaml documentation for deploying functions: https://docs.microsoft.com/en-us/azure/devops/pipelines/targets/azure-functions?view=azure-devops&tabs=dotnet-core%2Cyaml

---
### Lab 5:

Add logging to Application Insights

1. Deploy an Application Insights resource in your resource group (using portal, cli or arm template)
> tip: application insights docs: https://docs.microsoft.com/en-us/azure/azure-monitor/app/app-insights-overview

2. Write custom logs of output of your azure functions to Application Insights
https://docs.microsoft.com/en-us/azure/azure-functions/functions-monitoring?tabs=cmd#writing-to-logs
