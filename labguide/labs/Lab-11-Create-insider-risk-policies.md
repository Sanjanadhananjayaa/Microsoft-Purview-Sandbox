# Lab 11 - Configure Insider Risk Management Policies in Microsoft Purview

## Lab Overview

Enabling permissions for Insider Risk Management by adding users to the Insider Risk Management role group. This step ensures that designated users have access to and can effectively manage insider risk management features. It's important to note that the application of role group permissions may take up to 30 minutes to propagate across the organization. This process grants the necessary authority to oversee and respond to potential insider risks, such as IP theft and data leakage, enhancing the organization's security posture.

## Lab scenario
In this lab, you will explore the capabilities of Insider Risk Management to identify, mitigate, and respond to potential risks posed by individuals within the organization

## Lab objectives

In this lab, you will complete the following tasks:

+ Task 1: Process of setting up an insider risk policy.
+ Task 2: Apply to all insider risk management policies.
+ Task 3: Create policy.

## Architecture diagram
![](../media/risk.png)

### Task 1: Process of setting up an insider risk policy
In this task you, as the global administrator, will enable permissions for Insider Risk Management.  Specifically, you will add users to the Insider Risk Management role group to ensure that designated users can access and manage insider risk management features.  It may take up to 30 minutes for the role group permissions to apply to users across the organization. 

1. If you not already login to admin center, the address bar of Microsoft edge enter **admin.microsoft.com**.

1. On **Sign in** blade, you will see a login screen, in that enter the following email/username 
 
    * Email/Username: **<inject key="AzureAdUserEmail"></inject>** and then click on **Next**.
        
1. On **Enter Password** blade, enter the following password

    * Password: **<inject key="AzureAdUserPassword"></inject>** and then click on **signin**

1. From the left navigation pane of the Microsoft 365 admin center, select **Show all**.

    ![](../media/sc-900-lab15-1-01.png)

1. Under Admin centers, select **Security**.  A new browser page opens to the welcome page of the Microsoft 365 Defender portal.

    ![](../media/sc-900-lab15-1-02.png)

1. From the left navigation pane of the Microsoft 365 Defender portal, select **Permissions**.  You may need to scroll down to see this option.

1. From the Permissions page, under **Email & collaboration roles** select **Roles**.

    ![](../media/lab11-image1.png)

1. In the search bar, enter **Insider risk** then select the search icon (magnifying glass).  Notice the five roles that show up.  Each of these has different access levels.  Select **Insider risk management**.

    ![](../media/lab11-image2.png)

1. In the window that opens, next to where it says Members, select **Edit**. you may need to scroll to find it.

     ![](../media/lab11-image3.png)

1. On **Edit members of the role group** page To add members to this role group, click on **Choose users**, select **<inject key="AzureAdUserEmail"></inject>** and then 
   click on **select**.

     ![](../media/lab11-image4.png)

1. Back on **Edit members of the role group** page, click **Next**.
   
    ![](../media/lab11-image5.png)

1. Verify the added members is correct then select **Save**.

    ![](../media/lab11-image6.png)

1. From the bottom of the Insider Risk Management window, click on **Done**.

1. Close all the tabs except the **admin.microsoft.com** and then sign out from the admin center page and sign-in back again to reflect the permissions added for users faster.

### Task 2: Apply to all insider risk management policies
In this task you will walk through the settings associated with the Insider Risk Management solution.  Insider risk management settings apply to all insider risk management policies, regardless of the template you choose when creating a policy. 

1. You should be on the Microsoft 365 compliance center home page. If not, Open the browser tab **Home - Microsoft 365 compliance**. 
    https://compliance.microsoft.com/insiderriskmgmt

1. From the left navigation panel under Solutions, select **Insider risk management**.

1. Before getting started with setting up a policy, there are some settings that need to be configured.  From the Insider Risk Management page, select the **setting cog icon** on the top-right corner of the page to access Insider Risk settings.

     ![](../media/sc-900-lab14-T3-1.png)
   
    i. Privacy tab:  for users who perform activities matching your insider risk policies, this setting will determine whether to show their actual names or use anonymized versions to mask their identities.  Select **Do not show anonymized versions of usernames** then select **Save**.  Select the  **Policy indicators** tab.

      ![](../media/sc-900-lab14-T3-2.png)
    
    ii. Policy indicators tab: Once a policy triggering event occurs, activities that map to the selected indicators are used in determining the risk score, for the user. Policy indicators selected here are included the Insider risk policy templates.  Scroll to view all the indicators available and any associated information. Under **Office indicators**, select **Select all**, scroll down and then select **Save**.  Select the **Policy timeframes** tab.

      ![](../media/sc-900-lab14-T3-3.png)
   
   iii. Policy timeframes tab:  The timeframes you choose here go into effect for a user when they trigger a match for an insider risk policy.   The Activation window determines how long policies will actively detect activity for users and is triggered when a user performs the first activity matching a policy. Past activity detection Determines how far back a policy should go to detect user activity and is triggered when a user performs the first activity matching a policy.  Leave the default values.  Select the **Intelligent detections** tab.

      ![](../media/sc-900-lab14-T3-4.png)
   
    iv. Intelligent detections tab:  Review the options here.  Note the domains settings and how they relate to the indicators.

      ![](../media/sc-900-lab14-T3-5.png)
   
    v. Other items listed in the settings are in preview.  Explore these at will and note that as a preview, they are subject to change.

1. To return to the Insider risk management overview, select **Insider risk management** from the top-left corner of the page, above where it says Settings.

    ![](../media/sc-900-lab14-T3-6.png)

1. Keep this browser tab open, as you will use it in the next task.

### Task 3: Create policy
In this task, you will walk through the creation of a policy.

1. You should be on the Insider risk management page.  If not already there, open the browser tab labeled, **Insider risk management - Microsoft 365 compliance**.

1. From the Insider risk management overview page, select the **Policies** tab then select **+ Create**.  Configure each of the following policy tabs.

    ![](../media/lab11-image9.png)

1. Policy template:  From the list of categories, select **Data leaks**. Read the details associated with this template, then select **Next**.

    ![](../media/lab11-image10.png)
    
1. On **Name your policy** page, enter **InsiderRiskPolicy**, then select **Next**.

    ![](../media/lab11-image11.png)
    
1. On **Choose users and groups** page, select **Include all users and groups** and click on **Next**.

   ![](../media/lab11-image12.png)
         
1. On **Decide whether to prioritize content** page, read the description and select **I dont't want to prioritize content right now**, then select **Next**.

   ![](../media/lab11-image13.png)
               
1. On **Choose triggering event for this policy** page, select **User performs an exfiltration activity** and click **Next**.

   ![](../media/lab11-image14.png)
   
   >**Note** Triggering event: Review the detailed information. The policy is triggered by either the user performing an exfiltration activity as as defined (select the information icons for each bullet point for more detailed information) OR a match to an existing Data Loss Prevention (DLP) policy.  Since you don’t have any DLP policy configured as part of this exercise, select **User performs an exfiltration activity**.  Scroll down to see what is automatically selected.  Note that the policy indicators you enabled in the previous task are checked.   Recall that these indicators will only be activated once the policy is triggered and any activities that map to these indicators  will be used in calculating a risk score for the user.  In addition, Sequence detection is enabled.  If a sequence of activities, as defined, is detected then it suggests greater risk.  Select the information icon for detailed information on which indicators are required.  This selection requires that certain indicators be selected and that devices be onboarded. Scroll down and Leave the defaults

1. On **Choose thresholds for triggering events**  page, select **choose your own thresholds**  and click **Next**.

   ![](../media/lab11-image15.png)
   
   >**Note**: Triggering Thresholds: here you can specify default or custom thresholds associated with the indicators.  Recall the indicators are activated only after the policy trigger occurs so these thresholds do not influence when the policy is triggered. Select **choose your own thresholds**, By selecting this option, you can see the current default values. Leave the defaults.

    
1. On **Indicators** page, review the detailed information. Leave the default setting, Select **Next**.    

   ![](../media/lab11-image16.png)
    
1. On **Detection options** page, review the information, Select **Next**.   
   
    ![](../media/lab11-image17.png)
    
1. On **Choose threshold type for indicators** page, review the information. Select **Choose your own thresholds** then Select **Next**.  

   ![](../media/lab11-image18.png)
    
1. On **Review settings and finish** page, review the settings and select **Submit**.

   ![](../media/lab11-image19.png)
  
1. Click on **Done**.
 
1. You are back on the Policies tab of the Insider risk management page.  The policy you just created will be listed.

    ![](../media/lab11-image20.png)

1. In the policy you just created, the "Users in scope" field represents users that are currently being assigned risk scores by the policy.  Assigning users a risk scores occurs when the policy is triggered which is why the value shows 0.  An admin can configure a policy to start assigning risk scores to specific users, based on activity detected by the policies you selected, AND which bypasses the requirement that a triggering event is detected first.  To do this, select the policy next to the policy name to select the policy, then select **Start scoring activity for users**, which is shown above the policy table.

    ![](../media/lab11-image21.png)  
  
1. On **Start score activity for users** window, provide the following information:

   - Reason for scoring activity : Provide any reason.

   - Score activity for this many days: 5

   - Score activity for these users: **<inject key="AzureAdUserEmail"></inject>** 

   - select **Start scoring activity**.  It can take 24 hours for the users to appear on the 'Users' tab. After that time, you can select the users from that tab to review detected activities.

    ![](../media/lab11-image(22).png)


     >**Note**: Enabling permissions for Insider Risk Management is crucial to ensure that authorized users can effectively manage and respond to insider risk incidents. By assigning specific roles, the organization can control access and empower designated individuals to handle insider risk-related tasks.

### Conclusion:
The completion of this task ensures that the necessary permissions are granted for Insider Risk Management. By adding users to the Insider Risk Management role group, the organization establishes a foundation for managing insider risk effectively.

### Review
In this lab, you have completed:
+ Process of setting up an insider risk policy.
+ Apply to all insider risk management policies.
+ Create policy.

## You have successfully completed the lab