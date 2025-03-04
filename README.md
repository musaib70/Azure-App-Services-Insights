# Azure App Services Insights

The 'Azure App Services Insights' workbook offers a comprehensive view of your Azure App Services resources.

It enables you to delve into and compare key metrics effortlessly, gaining insights into usage trends, optimizing performance, and guiding strategic decisions effectively.

![image](https://github.com/dolevshor/Azure-AppServices-Insights/assets/69309933/2fb16d76-53b7-408b-a1d5-58abd3df7fc2)



### Overview

![image](https://github.com/dolevshor/Azure-AppServices-Insights/assets/69309933/128f640f-7aa3-41dd-bd49-7ea944b28404)

### Monitor

![image](https://github.com/dolevshor/Azure-AppServices-Insights/assets/69309933/8cff5edc-fa0d-4e3f-8e61-0c34d64d87f7)

![image](https://github.com/dolevshor/Azure-AppServices-Insights/assets/69309933/3cd05772-b07d-469e-a717-b1ab1106b5f3)

#### Additional Metrics

Expanding the Additional Metrics will allow to view and compare all the Metrics supported by the resource type. (group by categories)

- App Service Plan: Data, Sockets, TCP, Queue Length
- App Service: Requests/Response, Data, HTTP, IO, Garbage Collections, Others 
- Staging Slot: Requests/Response, Data, HTTP, IO, Garbage Collections, App Domains, Others

![image](https://github.com/dolevshor/Azure-AppServices-Insights/assets/69309933/a603f93b-2520-4541-96d4-790a410406cd)

![image](https://github.com/dolevshor/Azure-AppServices-Insights/assets/69309933/8b7adac7-52a5-4286-acef-b5259358b4b4)

### Inventory

The Inventory dashboard provide an holistic view of all App Services resources.

![image](https://github.com/dolevshor/Azure-AppServices-Insights/assets/69309933/aebe7d80-4045-4593-8482-09c491471562)


## Introduction

Azure App Service offers flexible scaling options (both Scale Up and Scale Out), supports multiple operating systems (Windows and Linux), and enables hosting multiple apps on the same App Service Plan.

Managing multiple App Service Plans, App Services, and Staging Slots requires effective management, performance comparison, and operational oversight — this functionalities facilitated by this workbook. 


## Structure and Views

### Structure

This workbook contains 2 main parts:
- **Overview** - Holistic view of Azure App Services resources.
- **Monitor** - Holistic view of Azure App Services Metrics

> App Services resources = App Service Plans, App Services, Staging slots.

### Views

Types of views this workbook provides:

- **Overview**
  - App Service Plan
    - Name
    - Resource Group
    - Location
    - Kind
    - Size
    - Tier
    - Status
    - Number of Sites
    - Current Instances
    - Maximum scale (instance)
  - App Services + Slots
    - Name
    - Resource Group
    - Location
    - Kind
    - Type
    - SKU
    - App Service Plan
    - State

> The information displayed uses [KQL](https://learn.microsoft.com/en-us/azure/data-explorer/kusto/query/) queries to query the [Azure Resource Graph](https://learn.microsoft.com/en-us/azure/governance/resource-graph/overview).

- **Monitor**
  - App Service Plan
    - CPU Percentage (Avg)
    - Memory Percentage (Avg)
  - App Service
    - CPU Time (Sum)
    - Memory Working Set (Avg)
  - Slots
    - CPU Time (Sum)
    - Memory Working Set (Avg)

- **Inventory**
  - App Service Plan
    - Count by Subscription Id
    - Count by Resource Group
    - Count by Location
    - Count by Status
    - Count by Kind
    - Count by Kind
    - Count by Size
    - Count by Tier
  - App Service
    - Count by Subscription Id
    - Count by Resource Group
    - Count by Location
    - Count by State
    - Count by Kind
    - Count by sku
    - Count by App Service Plan
  - Slots
    - Count by Subscription Id
    - Count by Resource Group
    - Count by Location
    - Count by State
    - Count by Kind
    - Count by sku
    - Count by App Service Plan

#### Filters

This workbook support to filter by:

- Resource Groups
- App Service Plans
- Apps (App Services + Staging slots)
- Time range

## How to use it?

Importing this Workbook to your Azure environment is quite simple.

Follow this steps to use the Workbook:

- Login to [Azure Portal](https://portal.azure.com/) <img src="https://user-images.githubusercontent.com/69309933/172941966-9e030031-6ccb-4ebf-bd2b-04bb623e5ff7.png" width="20" height="20">
- Go to _'Azure Workbooks'_

<img src="https://user-images.githubusercontent.com/69309933/172806635-14051976-328e-4623-96ab-0dd6a7bc7817.png" width="350">

- Click on _'+ Create'_

<img src="https://user-images.githubusercontent.com/69309933/172807465-cced3466-0669-423b-87b3-8fa70fdbf1d1.png" width="350">

- Click on _'+ New'_

<img src="https://user-images.githubusercontent.com/69309933/172807547-52d790ce-7852-4b4b-a81f-81e8b7fac26e.png" width="350"> 

- Open the Advanced Editor using the _'</>'_ button on the toolbar

<img src="https://user-images.githubusercontent.com/69309933/172807673-dfc63741-0c40-47c0-ab58-d39309b06e69.png" width="700"> 

- Select the _'Gallery Template'_ (step 1)
- Replace the JSON code with this JSON code [Azure AppService Insights JSON](https://github.com/dolevshor/Azure-AppServices-Insights/blob/main/Workbook/Azure%20App%20Service%20Insights.workbook) (step 2)

  - We use the _Gallery Templaty type_ (step 1), so we need to use the _'Azure App Service Insights.workbook'_ and not the _'Azure App Service Insights.json'_.
- Click _'Apply'_ (step 3)

<img src="https://user-images.githubusercontent.com/69309933/172807762-17aec6f9-4a81-4d5b-9017-673a0ab6b26e.png" width="700"> 

- Click in the ‘Save’ button on the toolbar

![image](https://github.com/dolevshor/Azure-AppServices-Insights/assets/69309933/88692b70-7d96-42e7-8852-590af825cfb5)

- Select a name and where to save the Workbook:
  - Title: _'Azure App Service Insights'_
  - Subscription: <_Subscription Name_>
  - Resource group: <_Resource Group Name_>
  - Location: <_Region_>
- Click _'Save'_
  
The Workbook is ready to use!
- Click on _'Workbooks'_
- Click on _'Azure App Service Insights'_ Workbook.


