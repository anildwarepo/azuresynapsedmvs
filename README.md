# Power BI Visualization for Azure Synapse SQL Pool Database Management Views

This repo provides Power BI Desktop template that can be used to visualize Azure Synapse DMVs. DMVs provide more insights into the internals of Azure Synapse Pools. This helps to better understand the performance problems, tune distribution and understand overall performance of the database. 

The template uses direct query mode to connect to DMVs so that the visualization is up to date. 
Template uses Azure Monitor REST API to retrive metrics specific to Synapse SQL Pools. 

Template uses Azure Active Directory Authentication to connect and simplifies authentication. 

The template connects to more than 30 DMVs and Azure Monitor metrics. The template provides some baseline visuals which can be extended further. 


<img src="https://github.com/anildwarepo/azuresynapsedmvs/raw/main/imgs/DMV%20relationship.png" width="500">



## Getting Started

### Pre-requisites
- Access to Azure Synapse Workspace
- Access to Azure Monitor Metrics
- Power BI Desktop installed on local computer which has network connectivity to Azure Synapse SqlPool(incase of Private Link)
- Sign in to Power BI Desktop using Azure Active Directory that can access Azure Synapse and Azure Monitor. 


### Launch Template 

Download Synapse-DMVs.pbit Power BI Desktop template and launch it with Power BI Desktop. 
Provide inputs to the parameters
- subscriptionId - Azure Subscription where Synapse Workspace is provisioned
- resourceGroup - Resource Group where Synapse workspace is provisioned
- synapseWorkspaceName - Synapse workspace name
- sqlPoolName - Synapse SQLPool Name
- synapseEndPoint - [sqlPoolName].sql.azuresynapse.net

<img src="https://github.com/anildwarepo/azuresynapsedmvs/raw/main/imgs/TemplateParameters.png" width="500">

### Validate Query

Power BI Desktop will prompt to validate query. Click Validate and grant permissions to execute query. 

<img src="https://github.com/anildwarepo/azuresynapsedmvs/raw/main/imgs/ValidateQuery.png" width="300">

### Visualize DMVs

That's it!! You can now add visuals and start visualizing DMVs.

### DMV Visualization samples

#### Nodes

<img src="https://github.com/anildwarepo/azuresynapsedmvs/raw/main/imgs/NodeCount.png" width="500">

#### Storage

<img src="https://github.com/anildwarepo/azuresynapsedmvs/raw/main/imgs/Storage.png" width="500">

#### Table Distribution

<img src="https://github.com/anildwarepo/azuresynapsedmvs/raw/main/imgs/Table%20Distribution.png" width="500">