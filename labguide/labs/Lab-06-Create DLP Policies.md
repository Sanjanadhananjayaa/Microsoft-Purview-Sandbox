# Lab 06 - Create a Data Loss Prevention (DLP) policy

## Lab Overview

This lab is designed to guide users through the process of creating a Data Loss Prevention (DLP) policy in the Microsoft Purview portal. The DLP policy aims to protect sensitive data, specifically Credit Card information, from being shared by users. The policy is configured to notify users when attempting to share such information, This lab provides hands-on experience in setting up a customized DLP policy tailored to the organization's data protection needs.

## Lab scenario

In this lab, you will create a Data Loss Prevention policy in the Microsoft Purview portal to protect sensitive data from being shared by users.

In Microsoft Purview, you implement data loss prevention by defining and applying DLP policies. With a DLP policy, you can identify, monitor, and automatically protect sensitive items across:

- Microsoft 365 services such as Teams, Exchange, SharePoint, and OneDrive
- Office applications such as Word, Excel, and PowerPoint
- Windows 10, Windows 11, and macOS (Catalina 10.15 and higher) endpoints
- Non-Microsoft cloud apps
- On-premises file shares and on-premises SharePoint

## Lab objectives

In this lab, you will complete the following tasks:
+ Task 1: Create a Data Loss Prevention (DLP) policy

## Architecture diagram
![](../media/purview-lab6.png)

### Task 1: Create a Data Loss Prevention (DLP) policy

In this task, you will create a Data Loss Prevention policy in the Microsoft Purview portal to protect sensitive data from being shared by users.

1. In **Microsoft Edge**, navigate to **https://compliance.microsoft.com** 

1. In the **Microsoft Purview** portal, in the left navigation pane, expand **Data loss prevention** and select **Policies**.

   ![](../media/lab6-image1.png)

1. On **Policies** page, select **+ Create policy** to start the wizard for creating a new data loss prevention policy.

    ![](../media/lab6-image2.png)

1. On the **Start with a template or create a custom policy** page, scroll down and select **Custom** under **Categories** and **Custom policy** under **Regulations**. By default, both  options should already be selected , select **Next**.

   ![](../media/lab6-image3.png)
   
1. On the **Name your DLP policy** page, type **Credit Card Policy** in the **Name** field and **Protect credit card numbers from being shared** in the **Description** field. Select **Next**.

   ![](../media/cc1.png)

1. On Assign admin units page, click **Next**.

   ![](../media/cc2.png)

1. On the **Choose where to apply the policy** page, select only **Exchange email** and uncheck other option and click **Next**. 

     ![](../media/cc3.png)
   
1. On the **Define policy settings** page, select **Create or customize advanced DLP rules** and select **Next**.

   ![](../media/cc4.png)

1. On the **Customize advanced DLP rules** page, select **+ Create rule**.

    ![](../media/cc5.png)

1. On the **Create rule** page, type **Credit card information** in the **Name** field.

1. Under **Conditions**, select **+ Add Condition** and then select **Content contains** from the dropdown menu.

   ![](../media/cc6.png)

1. In the new **Content contains** area, select **Add** and select **Sensitive info types** from the dropdown menu. On the **Sensitive info types** page, select **Credit Card Number** and select **Add**.

   ![](../media/cc7.png)

1. Under **Action** click **Add an actions** and select **Restrict access or encrypt the content in Microsoft 365 locations** fron the dropdowm menu.

    ![](../media/cc8.png)

1. Under **Restrict access or encrypt the content in Microsoft 365 locations** select **Block everyone**.

    ![](../media/cc9.png)

1. Unser **User notifications** select toggle for **Use notifications to inform your user and help educate them on the proper use of sensitive info** and enable check box for **Show the policy tip as a dialog for the end user before send**.

   ![](../media/cc11.png)

1. Under **Incident reports** select **severity level** as **Medium** click on  the toggle for **Under send an alert to admins when a rule match occurs** and click on **Save**.

    ![](../media/cc12.png)

1. Back on **Customize advanced DLP rules** page, and click on **Next**.

    ![](../media/cc13.png)

1. On **Policy mode** select **Turn the policy on immediately** and click **Next**.
  
1. On the Review and finish review the information and click **submit**. 

     ![](../media/cc15.png)

   >**Note**: You have now created a DLP policy that scans for Credit Card numbers in Microsoft outlook and allows users to provide a business justification to override the policy.

   >**Note**: Data Loss Prevention policies are critical for organizations to prevent inadvertent sharing of sensitive information. In this scenario, the focus is on protecting Credit Card numbers. The lab ensures that users are informed and prompted to provide justifications before sharing such data. This proactive approach helps in securing sensitive information and ensures that users are aware of the policy requirements.

### Conclusion

By completing this lab, users acquire practical knowledge of configuring DLP policies in the Microsoft Purview portal. The created DLP policy, specifically targeting Credit Card information, demonstrates how organizations can customize policies to align with their data protection and compliance requirements. The lab underscores the importance of user awareness and engagement in maintaining data security.

## Review
In this lab, you have completed:
+ Create a Data Loss Prevention (DLP) policy

## You have successfully completed the lab
