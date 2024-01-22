# Lab 15 - Explore the Core eDiscovery workflow

## Lab Overview
Microsoft Purview eDiscovery (Standard) in Microsoft Purview provides a basic eDiscovery tool that organizations can use to search and export content in Microsoft 365 and Office 365. You can also use eDiscovery (Standard) to place an eDiscovery hold on content locations, such as Exchange mailboxes, SharePoint sites, OneDrive accounts, and Microsoft Teams. Nothing is needed to deploy eDiscovery (Standard), but there are some prerequisite tasks that an IT admin and eDiscovery manager have to complete before your organization can start using eDiscovery (Standard) to search, export, and preserve content.

## Lab scenario
In this lab you will go through the steps required for setting up Core eDiscovery and then go through the Core eDiscovery workflow, by creating an eDiscovery hold, creating a search query, and then exporting the results of the search. Note: Licensing for Core eDiscovery requires the appropriate organization subscription and per-user licensing. If you aren’t sure which licenses support Core eDiscovery, visit Get Started with Core eDiscovery.

## Lab objectives

In this lab, you will complete the following tasks:

+ Task 1: Add specific users as members of the eDiscovery Manager role group
+ Task 2: Create a case to start using Core eDiscovery
+ Task 3: Create an eDiscovery hold
+ Task 4: Create a search query

## Estimated timing: 60 minutes

## Architecture diagram

![](../media/lab11.png)

## Task 1: Add specific users as members of the eDiscovery Manager role group

To access Core eDiscovery or be added as a member of a Core eDiscovery case, a user must be assigned the appropriate permissions. 
In this task, you as the global admin, will add specific users as members of the eDiscovery Manager role group.

1. Within **cvm-<inject key="DeploymentID" enableCopy="false"/>** RDP session, navigate back to the **Microsoft 365 admin center** portal.

1. On **Sign in** blade, you will see a login screen, in which you enter the following email/username 
 
    * Email/Username: **<inject key="AzureAdUserEmail"></inject>** and then click on **Next**.
        
1. On **Enter Password** blade, enter the following password   

    * Password: **<inject key="AzureAdUserPassword"></inject>** and then click on **sign in**

1. From the left navigation pane of the Microsoft 365 admin center, select **Show all**.

    ![](../media/sc-900-lab15-1-01.png)

1. Under Admin centers, select **Security**. A new browser page opens to the welcome page of the Microsoft 365 Defender portal.

    ![](../media/sc-900-lab15-1-02.png)

1. From the left navigation pane of the Microsoft Defender portal, select **Permissions**. You may need to scroll down to see this option.

1. From the Permissions page, under **Email & collaboration roles (1)** select **Roles (2)**.

    ![](../media/newone5.png)
   
1. In the search bar, enter **eDiscovery (1)** then select the search icon (magnifying glass). Select **eDiscovery Manager (2)**.

    ![](../media/lab15-image1.png)
     
1. In the window that opens, notice how there are two sub-groups, eDiscovery Manager and eDiscovery Administrator. Read the description of each. For this lab, we will add members to the eDiscovery Administrator sub-group.

1. Select **Edit**.

    ![](../media/lab15-image2.png)

1. On **eDiscovery Manager** page select **Next** on **Manager eDiscovery Manager**.

   ![](../media/lab15-image3.png)

1. On **Manage ediscovery Administrator**, click on **Choose users (1)** and select **ODL_User <inject key="DeploymentID" enableCopy="false"/> (2)** from the list and click on **Select (3)** and **Next**.

   ![](../media/lab15-image4.png)

1. Back on **Manage ediscovery Administrator** page, click on **Next**.
   
    ![](../media/lab15-image5.png)
   
1. On **Review the role group and finish** page, select **Save**.

    ![](../media/lab15-image6.png)

1. On **You successfully updated the role group** page, select **Done**.
 
1. Close all the tabs except the **Microsoft 365 admin center** and then **Sign out** from the admin center page and **Sign in** back again to reflect the permissions added for users faster.

## Task 2: Create a case to start using Core eDiscovery

In this task, you as an eDiscovery Administrator (ODL admin is an eDiscovery administrator), will create a case to start using Core eDiscovery.

1. Open the Microsoft 365 admin center tab on your browser.

1. From the left navigation panel, under Admin Centers, select **Compliance**.

1. From the left navigation panel, under Solutions, expand **eDiscovery (1)** then select **Standard (2)**.

     ![](../media/lab15-image9.png)
   
1. From the top of the Core eDiscovery page, select **+ Create a case**.

    ![](../media/lab15-image10.png)

1. In the New case window, enter a Case name, **Test Case (1)** then select the **Save (2)** at the bottom of the page.

     ![](../media/lab15-image11.png)

1. The case should now appear on the list.

     ![](../media/lab15-image12.png)

1. As the creator of the case and because you have eDiscovery Administrator privileges, you can begin to work with it.  

1. Keep this browser tab open, as you will use it in the subsequent task.

## Task 3: Create an eDiscovery hold

Now that you have created a Core eDiscovery case, you can begin to work with the case.

In this task, you will create an eDiscovery hold for the case you just created.  Specifically, you will create a hold for the exchange mailbox belonging to ODL-User.

1. Open the Core eDiscovery tab on your browser.

1. From the Core eDiscovery page, select the case you created in the previous tab, **Test Case**. 

1. From the Home page of the case, select the **Hold (1)** tab then select **+ Create (2)**.

   ![](../media/lab15-image13.png)

1. In the name field, enter **Test hold (1)** then select **Next (2)**.

    ![](../media/lab15-image14.png)

1. On **Choose locations** page, select toggle switch next to Exchange mailboxes to set the Status to **On (1)**, select **Choose users, groups, or teams (2)** and select the **ODL_User <inject key="DeploymentID" enableCopy="false" /> (3)** user and click on **Done (4)**, select **Next**, for expediency with the lab, no other locations will be included in this hold.
    
    ![](../media/lab15-image15.png)
   
    ![](../media/lab15-image16.png)

1. Back on **Choose locations** page, click **Next**.

   ![](../media/lab15-image17.png)

1. The Query conditions page enables you to create a hold, based on specific Keywords or Conditions that are satisfied, select **+ Add condition** to view the available options. Select **Next**. Without selecting any conditions, the hold will preserve all content in the specified location.

    ![](../media/lab15-image18.png)
    
1. On **Review your settings** page, select **Submit**, it may take a minute, then select **Done**. The Test hold should appear on the list. If you don't immediately see it, select 
   **Refresh**

    ![](../media/lab15-image19.png)

1. The Test hold should appear on the list. If you don't immediately see it, select **Refresh**

   ![](../media/lab15-image21.png)

1. Keep this browser tab open, as you will use it in the subsequent task.

## Task 4: Create a search query

In this task, you will create a search query. Once your search is complete you will export and download the results for future investigation.   

>**Note**: Searches associated with a Core eDiscovery case are not listed on the Content search page in the Microsoft 365 compliance center. These searches are listed only on the Searches page of the associated Core eDiscovery case.

1. Open the Test Case tab on your browser.

1. From the Holds page of the case, select **Searches (1)** and from the Search page, select **+ New Search (2)**.

     ![](../media/lab15-image22.png)

1. In the Name field, enter **Test Hold – Sales Search (1)**, then select **Next (2)** from the bottom of the page.

     ![](../media/lab15-image23.png)

1. On **Choose locations** page, select toggle switch next to Exchange mailbox to set the status to **On (1)**, select **Choose users, groups, or teams (2)** and select the **ODL_User <inject key="DeploymentID" enableCopy="false" />** user and click on **Done**, select **Next**.  

    ![](../media/lab15-image24.png)
   
    ![](../media/lab15-image25.png)

1. Back on **Choose locations** page, click **Next**.

    ![](../media/lab15-image26.png)

1. The Query conditions page enables you to create a search, based on specific Keywords or Conditions that are satisfied, In the keyword field enter **Sales (1)** and select **Next (2)**.

    ![](../media/lab15-image27.png)

1. On **Review your search and create it** page, select **Submit**, it may take a minute, then select **Done**. The search should appear on the list. If you don't immediately see it, select **Refresh**.

    ![](../media/lab15-image28.png)

1. The search should appear on the list. If you don't immediately see it, select **Refresh**.

    ![](../media/lab15-image39.png)
 
1. From the Searches window, select the search you just created, **Test Hold - Sales Search**. A window that opens with the Summary tab selected.  Once the search is complete the status will indicate that the search is completed. You will see a Search statistics tab (if you don't see the Search statistics tab, the search may still be running and may take a few minutes to complete). Select the **Search statistics** tab and select the drop-down next to Search content.  You can also view more information for the Condition report and Top locations.  

    ![](../media/lab15-image30.png)

    ![](../media/lab15-image31.png)

1. Select the **Summary** tab and from the bottom of the page, select **Actions (1)**. Note the available options. By selecting **Export results (2)**, search results can be downloaded. 

      ![](../media/lab15-image32.png)
          
1. From the Export results window, leave the defaults and select **Export** from the bottom of the page. You will automatically be returned to the **Test Hold - Sales search** window. Select **Close** at the bottom of the page.

      ![](../media/lab15-image33.png)
    
1. From the **Test case** page, select **Exports (1)** tab and select **Test Hold - Sales Search_Export (2)**, the window that opens, **Test Hold - Sales Search_Export**, you will see an Export key, select **Copy to clipboard (3)**.

      ![](../media/lab15-image35.png)

1. From the top of the window, select **Download results**.

   >**Note**: You must use Microsoft Edge or Internet Explorer to download. A new browser page opens and a pop-up window displays asking if you want to open this file, select **Open**.

   ![](../media/lab15-image36.png)

   ![](../media/lab15-image37.png)
        
1. If this is the first time you do a download of a content search, you will be prompted to install the Microsoft Office 365 eDiscovery Export tool. Select **Install**.

1. Once the installation is completed, the eDiscovery export tool window opens.
   
   - In the first field, paste the export key that you copied to your clipboard, **paste (1)** it in now 
 
   - In the second field, Click on **Browse (2)** and set the location to C:\LabFiles to store the downloaded file , then select **Start (3)**. Once the download process is completed, select **Close** and close this browser tab.

      ![](../media/lab15-image38.png)
      
1. You are back on the "Test Hold - Sales Search_Export" window. Select **Close**.

1. Check the location of your download to verify the download was successfully completed. 

### Conclusion
By completing the tasks outlined in this lab, users gain practical insights into the Core eDiscovery workflow. The ability to add users, create cases, implement holds, and execute search queries demonstrates proficiency in leveraging Microsoft 365 tools for eDiscovery purposes. This knowledge is essential for organizations aiming to streamline their eDiscovery processes and maintain compliance with legal requirements.

### Review
During this lab, you've gained knowledge on the following:
- Add specific users as members of the eDiscovery Manager role group
- Created a case to start using Core eDiscovery
- Created an eDiscovery hold
- Created a search query
  
## You have successfully completed the lab. Click on Next >>.
