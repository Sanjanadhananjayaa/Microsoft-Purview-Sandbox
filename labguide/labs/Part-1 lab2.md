# Part-1 lab 2 - Explore sensitivity labels and policies in Microsoft Purview


## Lab scenario
In this lab, you will explore the capabilities of sensitivity labels.  You will go through the settings for existing sensitivity labels that have been created and the corresponding policy to publish the label.   Then you will see how to apply a label and the impact of that label, from the perspective of a user.

## Lab objectives

In this lab, you will complete the following tasks:

+ Task 1: Explore the capabilities of sensitivity labels

## Architecture Diagram

 ![Picture 1](../media/image2.png)

## Task 1: Explore the capabilities of sensitivity labels
In this task you will gain an understanding of what sensitivity labels can do by going through the settings for an existing sensitivity label that have been created and the corresponding policy to publish the label.

1. If you not already login to admin center, the address bar of Microsoft edge enter **admin.microsoft.com**.

1. Sign in with your admin credentials.
   
1. In the Sign in window you will see a login screen, in that enter the following email/username and then click on **Next**. 

    * Email/Username: <inject key="AzureAdUserEmail"></inject>

1. Now enter the password and click on Sign in.
   
   * Password: <inject key="AzureAdUserPassword"></inject>
  
1. When prompted to stay signed-in, select **Yes**. This takes you to the Microsoft 365 admin center page.

1. From the left navigation pane of the Microsoft 365 admin center, select **Show all**.

    ![](../media/sc-900-lab15-1-01.png)

1. Under Admin centers, select **Compliance**.  A new browser page opens to the welcome page of the Microsoft Purview.  

    ![](../media/sc-900-lab15-1-2.png)
    
    ![](../media/sc-900-lab13-01.png)

1. From the left navigation panel of the Microsoft Purview, under Solutions, Expand **Information protection** and in the dropdown select **labels** and click on **Turn on now**.

1. In the yellow information box, indicates that Your organization has not turned on the ability to process content in Office online files that have encrypted sensitivity labels applied and are stored in OneDrive and SharePoint.  Select Turn on now.  Once you do this, there can be a delay for the setting to propagate through the system.

    ![](../media/sc-900-lab13-001.png)

1. On **Labels** tab from the dropdown and then select **Create a label**

    ![](../media/sc-900-lab13-2.png)

1. Provide a name and description for your label. Select **Next** at the bottom of the page.

    | Setting | Action |
    | -- | -- |
    | **Name** text box | Enter **Confidential-Finance** |
    | **Display name** text box | Enter **Confidential-Finance** |
    | **Description for users** text box | Enter **Confidential-Finance Demo** | 

    ![](../media/sc-900-lab13-3.png)

1. Note the scope for this label.  The scope is set to **Items**.  Read the description but don’t change anything.  Select **Next** at the bottom of the page.

      ![](../media/sc-900-lab13-4.png)

1. On the Choose protection settings for labeled items select the **Apply or remove encryption** and **Apply content marking**, then select **Next**.

    ![](../media/sc-900-lab13-5.png)
    
1. The Encryption window shows the configuration for the encryption settings. Review the information box under Configure encryption settings and review the configured settings. Notice how the user access to content is set to never expire.  You can also assign permissions to specific users and groups By clicking on the **Assign permission**.
    
    ![](../media/sc-900-lab13-6.png)
  
1. Click on **+Add Users or Groups**, select your **user name**  and click on **Add** then back to Assign permission page, Click on **Save**.and so only they can interact with content that has this label applied.  Under users and groups, the tenant is defined so all users in your tenant can view content that has this label.  The finance team is also listed and they have co-author permissions.  Don’t change any settings.  Select **Next** on the bottom of the page.

      ![](../media/sc-900-lab13-7.png)
      
      ![](../media/sc-900-lab13-8.png)
      
      ![](../media/sc-900-lab13-9.png)
      
      ![](../media/sc-900-lab13-10.png)
      

1. On the content markings page, take note of the information box on the top of the page. Turn on the Content Making and select **Add a watermark**, **Add a header**, & **Add a footer**, and click on **Customize text** on each and provide the text to it and click on **Save**.  Content markings will be applied to documents but only headers and footers will be applied to email messages. In other words, watermarks are not applied to emails.  The content marking associated with this label is a watermark. Select **Next** on the bottom of the page.

      ![](../media/sc-900-lab13-11.png)

1. You are now in the Auto-labeling for files and emails window. Turn on the **Auto-labeling for files and emails** and Read the description of auto-labeling on the top of the page and the information box below it. Select **Next** on the bottom of the page.

      ![](../media/sc-900-lab13-12.png)

1. This next window defines protection settings for groups, and sites that have this label applied. This is not enabled, select **Next** on the bottom of the page.

      ![](../media/sc-900-lab13-13.png)

1. This next window is a preview feature to automatically apply this label to Azure database columns (such as SQL, Synapse, and more) that contain the sensitive info types you choose.  This features is not enabled. Select **Next** on the bottom of the page.

      ![](../media/sc-900-lab13-14.png)
       
      
1.  Review the settings and click on **Create label**.

      ![](../media/sc-900-lab13-15.png)
      
1. Click on **Done** on next window.   

      ![](../media/lab13-1-1.png)
      
1. Click on **Publish label** from the **Label** Window.

      ![](../media/lab13-1-(2).png)     
    
1. Select **Choose sensitivity labels to publish**. A window opens that provides information about the policy. This policy serves to publish the IT-Department-Demo. Select **Confidential-Finance** from label and select **Add** on the bottom of the page. And then click on **Next**.

     ![](../media/border.png)
     
1. Under the Sensitivity labels to publish.  Don’t change any settings.  Select **Next** on the bottom of the page.

     ![](../media/sc-900-lab13-18.png)
     
1. Click on **Next** on Assign Admin Units(Preview) page.

     ![](../media/lab13-1-4.png)   

1. Read the description under “Publish to users and groups”.  Notice the this label is available to all users.  Don’t change any settings.  Select **Next** on the bottom of the page.

    ![](../media/sc-900-lab13-19.png)

1. Under the policy settings.  Don’t change any settings.  Select **Next** on the bottom of the page.

    ![](../media/sc-900-lab13-20.png)

1. Under the **Apply a Default label to documents**.  Don’t change any settings.  Select **Next** on the bottom of the page.

    ![](../media/sc-900-lab13-21.png)
1. Under the **Apply a Default label to emails**.  Don’t change any settings.  Select **Next** on the bottom of the page.

    ![](../media/sc-900-lab13-22.png)
    
1. Under the **Apply a default label to meetings and calendar events**.  Don’t change any settings.  Select **Next** on the bottom of the page.    

    ![](../media/sc-900-lab13-23.png)
    
1. Under the **Apply a default label to Power BI content**.  Don’t change any settings.  Select **Next** on the bottom of the page.

    ![](../media/sc-900-lab13-24.png)
    
1. The last configuration option is to name your policy. Enter the policy name as **Confidential-Finance Policy**.  Select **Next** on the bottom of the page to exit the policy configuration and return to the Information protection page.

    ![](../media/sc-900-lab13-25.png)
    
1. Review the settings and click on **Submit** and then select **Done**.

    ![](../media/sc-900-lab13-26.png)
    
    ![](../media/sc-900-lab13-27.png)    
    

1. From the left navigation panel, select Home to return to the Microsoft Purview.

1. Keep this page open, you will use it in the next task.

1. It can take up to 24 hours to publish the labels to the selected users apps

