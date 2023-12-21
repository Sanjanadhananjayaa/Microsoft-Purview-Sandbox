# Lab  07 - Implement data lose preventention browser extension 

## Lab scenario

## Lab objectives

In this lab, you will complete the following tasks:


### Task 1 – Prerequisties

### Configure the proxy server manually using "netsh" command

>**Note**: If you're onboarding Windows 10 or Windows 11 devices, to make sure that the device can communicate with the cloud DLP service.

1. From start menu Start and type cmd right-click **Command prompt** and select **Run as administrator**.

1. Enter the following command and press Enter:
    ```
    netsh winhttp set proxy 10.0.0.6:8080
    ```

   >**Note**: This will affect all applications including Windows services which use WinHTTP with default proxy.


1. In **Microsoft Edge**, navigate to **https://compliance.microsoft.com** 

1. In the **Microsoft Purview** portal, in the left navigation pane, expand **Data loss prevention** and select **Policies**.

   ![](../media/lab6-image1.png)

1. On **Policies** page, select **settings** icon at top right conner and expland **Browser and domain restrictions to sensitive data** and under **Unallowed browsers** click on **+ Add or edit unallowed browsers** select Firefox and Google Chrome, click on **Add**.

    ![](../media/lab6-image6.png)

1. Back on **Policies** page, select **+ Create policy** to start the wizard for creating a new data loss prevention policy.

    ![](../media/lab6-image2.png)

1. On the **Start with a template or create a custom policy** page, scroll down and select **Custom** under **Categories** and **Custom policy** under **Regulations**. By default, both  options should already be selected , select **Next**.

   ![](../media/lab6-image3.png)
   
1. On the **Name your DLP policy** page, type **Endpoint-dlp-policy** in the **Name** field and select **Next**.

   ![](../media/lab7-image1.png)

1. On Assign admin units page, click **Next**.

   ![](../media/cc2.png)

1. On the **Choose where to apply the policy** page, select only **Devices** and uncheck other option and click **Next**. 

     ![](../media/lab7-image2.png)
   
1. On the **Define policy settings** page, select **Create or customize advanced DLP rules** and select **Next**.

   ![](../media/cc4.png)

1. On the **Customize advanced DLP rules** page, select **+ Create rule**.
   ![](../media/cc5.png)

1. On the **Create rule** page, type **Endpoint-rule** in the **Name** field.

1. Under **Conditions**, select **+ Add Condition** and then select **Content contains** from the dropdown menu.
   ![](../media/cc6.png)

1. In the new **Content contains** area, select **+ Add** and select **Sensitive info types** from the dropdown menu. On the **Sensitive info types** page, select **Credit Card Number** and select **Add**.

   ![](../media/cc7.png)

1. In the new **Content contains** area, select **+ Add** and select **Sensitive labels** from the dropdown menu. On the **Sensitive label** page, select **Confidential_Finance** and select **Add**.

1. Under **Action** click **Add an actions** and select **Audit or restrict activities on devices** fron the dropdowm menu.

1. Under **Service Domain and Browser Activities**, select checkbox for **upload to a restricted Cloud Service domain or access from an unallowed browser** and from the dropdown select **Block**.

   ![](../media/lab7-image3.png)

1. For **Files activities for all apps**, select **Apply restriction to specific activities**  and choose all the activities and from the drop down select **Block** for all. 

   ![](../media/lab7-image4.png)

1.  under Incident report, select the severity to medium and turn on the toggle for **Send an alert to admin when rule matches occur** and select **Send alert every time an alert on an activity matches the rule** and click on save.

   ![](../media/lab7-image5.png)

1. Back on **Customize advanced DLP rules** page, and click on **Next**.


1. On **Policy mode** select **Run the policy in test mode** and click **Next**.
  

1. On the Review and finish review the information and click **submit**. 
    
