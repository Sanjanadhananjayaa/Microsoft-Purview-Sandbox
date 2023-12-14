### Task 1 – Create a DLP policy in test mode

In this exercise, you will create a Data Loss Prevention policy in the Microsoft Purview portal to protect sensitive data from being shared by users. The DLP Policy that you create will inform your users if they want to share content that contains Credit Card information and allow them to provide a justification for sending this information. The policy will be implemented in test mode because you do not want the block action to affect your users yet.

1. In **Microsoft Edge**, navigate to **https://compliance.microsoft.com** 

1. If the **Stay signed in?** dialog box appears, select the **Don’t show this again** checkbox and then select **No**.

3. In the **Microsoft Purview** portal, in the left navigation pane, select **Policies** and under **Data** select **Data loss prevention**.

1. In the **Data loss prevention** window select the **Policies** tab, and then select **+Create policy** to start the wizard for creating a new data loss prevention policy.

1. On the **Start with a template or create a custom policy** page, scroll down and select **Custom** under **Categories** and **Custom policy** under **Templates**. By default, both  options should already be selected , select **Next**.

1. On the **Name your DLP policy** page, type *Credit Card DLP Policy* in the **Name** field and *Protect credit card numbers from being shared.* in the **Description** field. Select **Next**.

1. On the **Choose locations to apply the policy** page, enable the **Teams chat and channel messages** option only and select **Next**. 

1. On the **Define policy settings** page, select **Create or customize advanced DLP rules** and select **Next**.

1. On the **Customize advanced DLP rules** page, select **+ Create rule**.

1. On the **Create rule** page, type *Credit card information* in the **Name** field.

1. Under **Conditions**, select **+ Add Condition** and then select **Content contains** from the dropdown menu.

1. In the new **Content contains** area, select **Add** and select **Sensitive info types** from the dropdown menu.

1. On the **Sensitive info types** page, select **Credit Card Number** and select **Add**.

1. On the **Create rule** page, select **+ Add condition** and select **Content is shared from Microsoft 365** from the dropdown menu.

1. In the new **Content is shared from Microsoft 365** section, select the **Only with people inside my organization** option.

1. On the **Create rule** page, select **+ Add an action** and select **Restrict access or encrypt the content in Microsoft 365 locations**.

1. Check the box in front of **Restrict access or encrypt the content in Microsoft 365 locations** and then select **Block Everyone**.

1. On the **Create rule** page, in the **User notifications** section, select the switch to put it in the **On** position.

1. On the **Create rule** page, in the **User overrides** section, under the **Allow overrides from M365 services**, check the box **Allow overrides from M365 services. Allows users in Exchange, Sharepoint, OneDrive and Teams to override policy restrictions.**

	Note: If you were not able to select the check box of **Allow overrides from M365 services**, enable the check box of **Notify users in Office 365 with a policy tip** which can be found on the **Create rule** page under the **User notification >>  Microsoft 365 services** section from the previous step. Then select the check box of **Allow overrides from M365 services. Allows users in Exchange, Sharepoint, OneDrive and Teams to override policy restrictions.**

1. Check the box **Require a business justification to override**.

1. In the **Incident reports** section, in the **Use this severity level in admin alerts and reports** dropdown, select **Low**.

1. Select **Save**, then select **Next**.

1. On the **Test or turn on the policy** page select **Test it out first** and select **Show policy tips while in test mode**.

1. Select **Next** and review the policy configuration.

1. Select **Submit** to create the policy.

1. Once the policy is created select **Done**.

You have now created a DLP policy that scans for Credit Card numbers in Microsoft Teams chats and channels and allows users to provide a business justification to override the policy.
