# Lab  14 - Azure Storage in-place data share with Microsoft Purview Data Sharing 

## Lab scenario

With Microsoft Purview Data Sharing, data providers can now share data in-place from Azure Data Lake Storage Gen2 and Azure Storage accounts, both within and across organizations. Share data directly with users and partners without data duplication and centrally manage your sharing activities from within Microsoft Purview.

A data provider creates a share by selecting a data source that is registered in Microsoft Purview, choosing which files and folders to share, and who to share them with. Microsoft Purview then sends an invitation to each data consumer.

## Lab objectives

In this lab, you will complete the following tasks:

### Task 1 : Create Purview account in Azure Portal 

1. Sign in to **Azure Portal**.

1. On Azure Portal page, in **Search resources, services and docs (G+/)** box at the top of the portal, enter **Microsoft Purview**, and then select **Microsoft Purview accounts** under services.
    ![](../media/lab14-image1.png)

1. Select **+ Create** on **Microsoft Purview accounts** page.

1. On the Basics tab specify the following details and click **Review + Create**.

    
     |   **Option**                           | **Value** *                    |
     | ---------------------------------------| ------------------------------ | 
     | Subscription                           | Accept the default             |
     | Resource Group                         | Purview-rg                     | 
     | Microsoft cover your account name      | purview-account1               | 
     |    location                            | West US                        |
     |||

    ![](../media/lab14-image2.png)

1.  Validation is passed. Click on Create.

1. Log out as odl user and log in as **John doe**

1. On Azure Portal page, in **Search resources, services and docs (G+/)** box at the top of the portal, enter **Microsoft Purview**, and then select **Microsoft Purview 
   accounts** under services.
    ![](../media/lab14-image1.png)

1. Select **+ Create** on **Microsoft Purview accounts** page.

1. On the Basics tab specify the following details and click **Review + Create**.

    
     |   **Option**                           | **Value** *                    |
     | ---------------------------------------| ------------------------------ | 
     | Subscription                           | Accept the default             |
     | Resource Group                         | Purview-rg                     | 
     | Microsoft cover your account name      | purview-account2               | 
     |    location                            | West US                        |
     |||

1.  Validation is passed. Click on Create.
   
### Task 2 : Create Storage account in Azure Portal

In this task, you'll create storage account and container 

1. On Azure Portal page, in **Search resources, services and docs (G+/)** box at the top of the portal, enter **Storage accounts**, and then select  **Storage accounts** under services.

1. On the **Storage accounts** page, click on **+ Create**.

1. On the Basics tab specify the following details and click **Adavance**.

    
     |   **Option** | **Value** *        |
     | ------------ | ------------------ | 
     | Subscription | Accept the default     |
     | Resource Group  | Purview-rg     | 
     | Storage account name | storage            | 
     | Region         | West US             |
     | Redundancy    |     Local Redundant Storage LRS|
     |||

    ![](../media/lab14-image3.png)

1. On Advanced tab, select **enable hierarchical namespace** and click on review.

   ![](../media/lab14-image4.png)

1.  Once validation passed click on **Create**.

1. Once storage account is created, click on the storage account which you created.
1. Under Data Storage section, select Containers option and click on **+ container**. Provide some name and click on create.
1. Open the File Explorer and create some text file.
1. Back on **Storage account** window, select the container which you created and click on the upload, select browse for the files and select the text file which you created and click on upload.


### Task 3 : Azure Storage in-place data sharing with Microsoft Purview

In this task, you'll work on Azure Storage in-place data sharing with Microsoft Purview

1. Sign in to Purview(https://purview.microsoft.com/)

1. On **Select a Microsoft Purview account** page, leave default for Microsoft Entra ID and for **Account name** select purview    click on **continue**.
    ![](../media/lab14-image5.png)

1. On Microsoft Purview portal from left navigation Pane,  select **Data Map** and in the Data source click on Register icon.

   ![](../media/lab14-image6.png)

1. On **Register Data Source** window, in the search bar, search and select **Azure Data Lake Storage Gen2** and click on Continue.

     ![](../media/lab14-image7.png)

1. On Registered data source (Azure Data Lake storage Gen2), specify the following  and click on Register.   

     |   **Option** | **Value** *        |
     | ------------ | ------------------ | 
     | Data source name | leave default     |
     |  Azure subscription  | OTU subscription    | 
     | Storage account name | storage            | 
     |||

    ![](../media/lab14-image8.png)

1. In the Azure portal, in the search bar, search for subscription and select Subscription which is listed.

1. Under Settings section, select **Preview features** option.

1. In Search bar search for allow,  select **AllowDataSharingInheroRegion** and **AllowDataSharing**, click on **+ Register**.

1. Under Setting section, select **Resource providers** and in search bar search for storage and select **Microsoft.StorageActions**,  **Microsoft.StorageTasks** and click on **Register**.

1. Return back to **Purview(https://purview.microsoft.com/)** and 

1. Select **Data Map**, Under Data Sharing section  select **Shares** and click on **+ New share**.

     ![](../media/lab14-image9.png)

1. On **New share** window, for type select **Azure Data Lake Storage Gen2** from the drop down and for select a source choose the storage account **storage** and click on Continue.

   ![](../media/lab14-image10.png)

1. On **New share** wndow provide some text to **Share name** and click on **Continue**.

1. On Add assets window expand container and select text file and click on **continue**.

1. Again *click on **continue** on **Add assets** window

1. On **Add recipients** enter your personal email and click on **Create and share**

1. Back on shares notice Sent shares.

    ![](../media/lab14-image12.png)

1. Check your email id  you have received the Invite link.

   >**Note**: If you have your personal purview account you can select Share invites. If you received an email invitation, you can also select the View share invite link in the email to select a Microsoft Purview account.

   >**Note**: When a share is attached, a new asset of type received share is ingested into the Microsoft Purview catalog, in the same collection as the storage account to which you attached the share is registered. You can search or browse for it like any other asset.

# Task 4 : Update received share 

>**Note** : If you have personal purview account you can perform the task.

1. In purview portal, select the Data Map icon from the left navigation. In the new portal, navigate to the Data Catalog application.

1. Select Share invites. If you received an email invitation, you can also select the View share invite link in the email to select a Microsoft Purview account.

1. If you're a guest user of a tenant, you'll be asked to verify your email address for the tenant before viewing share invitation for the first time.

1. After you've selected your data share to edit, you can reattach the share to a new storage account or path in your current storage account by selecting a storage account, providing a path, and providing the folder.

1. If you're updating the target, select Attach to target to save your changes. Attaching can take a couple minutes to complete after the process has been started.
