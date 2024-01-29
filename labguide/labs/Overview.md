# Data Security with Microsoft Purview	

## Overview

Microsoft Purview is a data governance service by Microsoft that enables organizations to discover, understand, and manage their data across on-premises, multi-cloud, and SaaS environments. It provides a unified view of data assets, helps maintain data compliance, and facilitates collaboration among teams for effective data management and utilization. With automated discovery and classification, Purview enhances data visibility and empowers organizations to make informed decisions based on trusted and well-governed data.

## Key features of Microsoft Purview

- Data security: Microsoft Purview provides a robust and coordinated set of risk and compliance solutions to help you discover and protect sensitive information.
- Threat Detection: Microsoft Purview includes unified data governance solutions that help you manage data services across your on-premises, multi-cloud, and software-as-a-service (SaaS) estate. That includes Azure storage services, Power BI, databases like SQL or Hive, file services like Amazon S3, and many more.
- Risk and compliance: Microsoft Purview includes risk and compliance solutions to help your organization minimize compliance risks and meet regulatory requirements. 

## Sandbox Scenario
Contoso, a multinational corporation, operates a complex IT infrastructure with a mix of on-premises data centers and cloud-based resources. Facing challenges in managing and governing their expanding data landscape, Contoso decides to implement Microsoft Purview to streamline data discovery, classification, and management across their entire IT environment.

By implementing Microsoft Purview, Contoso achieves a unified and streamlined approach to data governance, allowing them to effectively manage, classify, and collaborate on their diverse data assets. This enhances their ability to meet compliance requirements and ensures a proactive stance in addressing data-related challenges across their complex IT infrastructure.

## About the Sandbox

Using this environment, You'll be able to explore complete features and offerings offered by Microsoft Sentinel. Please find the detailed overview of the sandbox environment below.

### Pre-provisioned resources

#### **Virtual Machine**: 

- 1 *Windows 11* Virtual machine, virtual machine-related resources like Virtual networks, Network security groups, managed disks, Network interface cards, and IP addresses are deployed as part of the automation.

   These virtual machines are tailored and configured to the sandbox's specifications. Files, applications, packages, and OS configurations are all pre-configured. It is recommended that you use the same virtual machine throughout the lab for the best experience.

#### **License and subscription**: 

- You'll have access to a pre-configured Microsoft user account with an active Azure subscription, a tenant, and a Microsoft 365 E5 license assigned to the user. 
   
  User account has assigned as Owner at subscription and Global administrator at the tenant level. You need to use the same user account throughout the lab to get the most out of the lab. 

#### **Azure Credits**: 

- You have been given Azure credit of **$83 USD** which includes the running cost of pre-deployed Azure resources, license cost, and other Azure resources deployed while running through the lab.

  You will receive **cost alerts** to your registered email address at **50%/75%/90%/95%/100%** of the allotted Azure Credit is spent.

  You can visit the Azure Subscription page to check the current Azure credit spend and Analysis on the **Cost analysis** tab under the Cost Management option.

  ![Picture 1](../media/o1.jpg)

#### **Duration and Deletion of sandbox**:  

- The sandbox environment will be active for **30 days/720** hours from the time of registration. 
- The maximum allowed virtual machine uptime is only **40 hours**. It is recommended to deallocate the virtual machine when not in use.
- The virtual machine is set up with a custom feature called Idle start/stop. This custom package will check the virtual machine's idleness every **2 hours/120 minutes**. If the virtual machine is left idle for over 2 hours, a pop-up window will appear, prompting you to respond. If you do take action within 10 minutes, the virtual machine will shut down automatically.  This feature is enabled in virtual machines to optimize Azure costs.
- when 100% of Azure credits are spent, the sandbox environment will get automatically deleted without any prior notification. To retain the environment for a longer period and to get the most out of the environment, please follow the best practices mentioned below.

#### **Best practices**: 

- **Resources usage**: Please stop the virtual machines and other resources when not in use to minimize the Azure spend.
  
- **Azure Cost Analysis**: Maintain a practice of checking the Cost Analysis report of the assigned Azure subscription often in check the Azure spending so that the environment can be retained for a longer duration of time.

- **Alert notifications**: Make sure to check your registered email's inbox for any alert-related mails. Alerts give you can head start to keep your Azure spending in control and to plan out the remaining credits in the best way possible.


## Lab guide Content:

You will have access to a lab guide which is a reference material to assist you in getting started with the exploration. 

Based on your interests, you can use this lab guide as a reference to learn and test any Microsoft Purview feature.  You are also encouraged to explore additional features of Microsoft Purview based on your interests and preferences.

- Lab 01 - Configure Sensitive Labels 
- Lab 02 - Publish sensitivity labels
- Lab 03 - Configure Message Encryption
- Lab 04 - Install and Use Azure Information Protection Unified Labeling Client To Classify Files
- Lab 05 - Use M365 Apps to Label data
- Lab 06 - Create a Data Loss Prevention (DLP) policy
- Lab 07 - Implementing Microsoft Purview extension for Chrome
- Lab 08 - Configure Data Loss Prevention Alerts
- Lab 09 - Investigation of Data Loss Prevention Alerts
- Lab 10 - Configure Safe breach simulation
- Lab 11 - Configure Insider Risk Management Policies in Microsoft Purview
- Lab 12 - Investigate insider risk activities
- Lab 13 - Implement and Use Information Barriers
- Lab 14 - Azure Storage in-place data share with Microsoft Purview Data Sharing
- Lab 15 - Explore the Core eDiscovery workflow
- Lab 16 - Configure Retention Policies

### Azure services and related products

- Microsoft Entra ID
- Azure Storage Account
- Azure Purview
