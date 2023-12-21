# Lab 08 - Configure DLP Alerts

## Lab scenario

DLP triggers an alert if a user takes an action that aligns with a DLP policy, and you have configured Incident reports to generate alerts. The alert is then posted in the DLP Alerts dashboard for further investigation.

## Lab objectives

In this lab, you will complete the following tasks:

1. In **Microsoft Edge**, navigate to **https://compliance.microsoft.com** 

1. In the **Microsoft Purview** portal, in the left navigation pane, expand **Data loss prevention** and select **Policies**.

   ![](../media/lab6-image1.png)

1. Select the **Credit card policy** and click **Edit**.

1. Navigate to **Customize advanced DLP rules** page and select **Edit** icon.

1. Under **Investigate** notice the setting and here you can change Serverity on alerts as per your requirement.

1. For now keep as it is and select cancel.
   
    >**Note**: This configuration allows you to see these options when you create or edit a DLP policy. Use this option to create an alert that's raised every time a DLP rule match happens.

1. In the **Microsoft Purview** portal, in the left navigation pane, expand **Data loss prevention** and select **Alerts**.

   ![](../media/cc22.png)

1. From the Microsoft Purview home page, select the **app launcher icon**, and **right click on the Outlook icon** and select **Open in new tab**.

   ![](../media/lab5-image5.png) 

1. Select **New Email** from the top left corner of the screen.

1. Add email address of outside organization people and provide subject, enter some demo credit card number and try to send this mail.
   ![](../media/cc17.png)

   >**Note**: Notice policy tip.

1. Notice that email is restricted by policy and you receive mail as showed below.
    
    ![](../media/cc18.png)

