
# Azure Hybrid Benefit Workbook

## Workbook Overview

The Azure Hybrid Benefit Workbook provides a detailed overview of Windows VMs, Linux VMs, and Windows VMSS with and without Azure Hybrid Benefit (AHUB) enabled. The workbook also allows you to filter the results by subscription, resource group, or tags.

### Deployment
* Consider the following least-privilege (minimum) RBAC permissions when deploying the workbook:

  * **Reader** and **Workbook Contributor** : allows you to import the workbook, view all of the workbook tabs and save the workbook in a resource group.
  * **Reader** : allows you to import the workbook and view all of the workbook tabs.

Use the following link to deploy the AHUB Workbook:

   <a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Farthurclares%2FAzureHybridBenefitWorkbook%2Fmain%2Fworkbook%2Fazuredeploy.json" target="_blank"><img src="https://aka.ms/deploytoazurebutton"/></a>
    

    
## Table of Contents
- [Workbook Overview](#workbook-overview)
  - [Filtering](#filtering)
  - [Resource Location](#resource-location)
- [Virtual Machine/VMSS Tab](#virtual-machinevmss-tab)
  - [Windows VMs Overview](#windows-vms-overview)
  - [Linux VMs Overview](#linux-vms-overview)
  - [Windows VMSS Overview](#windows-vmss-overview)
- [SQL Tab](#sql-tab)
- [Feedback](#feedback)

## Workbook Overview

### Filtering

The Azure Hybrid Benefit Workbook allows you to filter the results by subscription, resource group, or tags. This can be useful if you need to focus on specific parts of your environment

 ![FilterBy](https://github.com/arthurclares/AzureHybridBenefitWorkbook/raw/main/images/FilterBy.png)

### Resource Location
> [!NOTE]
>The **Resource Location** parameter is required to load the SKU available in that region. Please note that not all the SKUs are available in all regions, so if you are using some specific SKUs, make sure this parameter is set to the correct location.
By default, the parameter will pick any location.

The Resource Location parameter is important to ensure that the workbook displays accurate information about the SKUs available in your region. Be sure to set this parameter correctly to ensure that you are seeing the most relevant information.

## Virtual Machine/VMSS Tab

In this tab, you can see the list of Windows VMs, Linux VMs and Windows VMSS with and without AHUB.


### Windows VMs Overview

In this subtab, you can see the list of Windows VMs where AHUB is enabled and where it is not enabled. 

The virtual machines (VMs) with less than 8 cores are categorized as **Low Priority**, while those with 8 or more cores are classified as **High Priority**. In situations where there are insufficient Azure Hybrid Benefit licenses to cover all the VMs in the environment, **it is recommended to prioritize the High Priority VMs**.

![WindowsOverview](https://github.com/arthurclares/AzureHybridBenefitWorkbook/raw/main/images/WindowsOverview.jpg)


This workbook also provides you with the view of VMs that have enabled the Hybrid Benefit in the past 7 days. This can be useful for you to monitor and prioritize VMs that you will bring the biggest savings.

![Cores Enabled 7 days Overview](https://github.com/arthurclares/AzureHybridBenefitWorkbook/raw/main/images/Cores%20Enabled%207%20days.jpg)

#### View list of Windows VMs 

You can change the above parameters to see the list of all VMs that have AHUB enabled / disabled. It is also possible to download those results to a CSV file by clicking in the download button at the top right of each table.


![AHUB Enabled1](https://github.com/arthurclares/AzureHybridBenefitWorkbook/raw/main/images/AHUB%20Enabled1.jpg)
![AHUB Disabled1](https://github.com/arthurclares/AzureHybridBenefitWorkbook/raw/main/images/AHUB%20Disabled1.jpg)
![AHUB7DaysDetails](https://github.com/arthurclares/AzureHybridBenefitWorkbook/raw/main/images/AHUB7DaysDetails.jpg)


### Linux VMs Overview

In this tab, you can see the list of Linux VMs where AHUB is enabled and where it is not enabled. 

![LinuxOverview](https://github.com/arthurclares/AzureHybridBenefitWorkbook/raw/main/images/LinuxOverview.jpg)


### Windows VMSS Overview

In this tab, you can see the list of Windows VMSS where AHUB is enabled and where it is not enabled. For Windows VMSS, the same AHUB prioirtization rule applies. 
The Virtual Machines Scale Set(VMSS) with less than 8 cores are categorized as Low Priority, while those with 8 or more cores are classified as High Priority. **In situations where there are insufficient Azure Hybrid benefit licenses to cover all the VMSS in the environment, it is recommended to prioritize the High Priority VMSS.**

![VMSSOverview](https://github.com/arthurclares/AzureHybridBenefitWorkbook/raw/main/images/VMSSOverview.jpg)



## SQL Tab

In this tab, you can see the list of SQL Databases, SQL Managed Instances and SQL on VMs with and without AHUB.

![VMSSOverview](https://github.com/arthurclares/AzureHybridBenefitWorkbook/raw/main/images/SQL%20Overview.jpg)


## Feedback and Suggestions

We welcome any feedback or suggestions on this workbook! If you find any bugs or have ideas for improvements, please create an issue on this repository and we'll get back to you as soon as we can.

To create an issue, click on the "Issues" tab at the top of this page and then click the green "New Issue" button. Please provide as much detail as possible about the issue or suggestion you have, including any steps to reproduce the problem or implement the suggestion.

We appreciate your help in making this workbook better for everyone!
