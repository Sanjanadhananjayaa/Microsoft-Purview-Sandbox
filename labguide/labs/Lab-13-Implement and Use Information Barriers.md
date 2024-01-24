# Lab 13 - Implement and Use Information Barriers

## Lab Overview

Information Barriers in Microsoft 365 serve as a critical tool for controlling communication and collaboration between different segments or groups within an organization. The configured Information Barriers establish a virtual barrier to prevent specific users or groups from interacting, thereby ensuring compliance, preventing conflicts of interest, and protecting sensitive information.

## Lab scenario

In this lab, you'll configure and manage Information Barriers in Microsoft 365. Information Barriers play a critical role in maintaining clear boundaries and preventing unauthorized communication between specific groups or individuals within your organization. By implementing Information Barriers, you ensure compliance with regulations, protect sensitive information, and minimize conflicts of interest. This setup will create a secure work environment, safeguarding data confidentiality and supporting 
organization commitment to compliance.

## Lab objectives

In this lab, you will complete the following tasks:

+ Task 1: Modifying the attribute and assigning a license for the user named *Johndoe*.
+ Task 2: Creating segments for Information Barriers
+ Task 3: Create Information barrier policies
+ Task 4: Enable Scoped Directory Search on Microsoft Teams
+ Task 5: Apply Information barrier policies
+ Task 6: Assess Information Barriers functionality within Microsoft Teams.

## Estimated timing: 60 minutes

## Architecture diagram

![](../media/archi-8.png)

### Task 1: Modifying the attribute and assigning a license for the user named *Johndoe*.

In this task, you'll set the department attribute and assign a license to the user Johndoe.

1. Within **cvm-<inject key="DeploymentID" enableCopy="false"/>** RDP session, double click on the **Azure Portal** shortcut, and sign in with following credentials:
   
    * Email/Username: <inject key="AzureAdUserEmail"></inject>
   
    * Password: <inject key="AzureAdUserPassword"></inject>

      ![](../media/azureportal.png)
  
1. On Azure Portal page, in **Search resources, services and docs** box at the top of the portal, enter **Microsoft Entra ID (1)**, and then select **Microsoft Entra ID (2)** under services.

   ![](../media/MicrosoftentraID.png)

1. On **Overview** page, Under **Manage** section select **Users**.

   ![](../media/microsoftentraid1.png)
   
1. Choose **ODL_User <inject key="DeploymentID" enableCopy="false"/> (1)** user, then click on the **Edit properties (2)** tab.

   ![](../media/odluser1.png)

   ![](../media/editproperties.png)

1. Scroll down and select **Job Information (1)**. Under the **Job information** tab for the **Department** field, enter **HR (2)**, then click **Save (3)**.

   ![](../media/b-image10.png)
   
1. On the **ODL_User <inject key="DeploymentID" enableCopy="false"/>**, select **Users**. Back on user blade, select **+ New user (1)** from drop down choose **Create new user (2)**.

   ![](../media/users.png)

   ![](../media/entraid.png)

1. Create a new user on the **Basics** tab with the following settings (leave others with their defaults) and select **Next: properties > (6)**.

    | Setting | Value |
    | --- | --- |
    | User principal name | **Johndoe (1)**  |
    | Display Name | **Johndoe (2)** |
    | Auto-generate password | **unchecked (3)**  |
    | Password | **Provide a secure password (4)** |
    | Account enabled | **Checked (5)** |

    ![](../media/newuser.png)
        
1. On  the **Properties** tab specify the following settings (leave others with their defaults):  

    | Setting | Value |
    | --- | --- |
    | Department | **Finance** |
    | Usage location | **United States** |
       
1. Click on **Review + create** and then **Create**.

1. In the list of users, click the newly created user account to display its blade.

   ![](../media/johndoe.png)

1. Under **Manage**, select **Licenses**.

   ![](../media/licenses.png)

1. On **Johndoe | Licenses** page, select the **+ Assignments** button.

   ![](../media/licenses1.png)

1. On the Update license assignments page, select the check box for the **Office 365 E5** license.

    ![](../media/b-image9.png)

1. When complete, select **Save**.

1. Now navigate to the user profile of **John doe**, from the left navigation pane select **Licenses**.

1. Notice that the license has been assigned.

   >**Note**: If you're not able to view the assigned license kindly refresh the page.

   ![](../media/licenses2.png)

### Task 2: Create segments for Information Barriers

In this task, you'll create organization segments for the **HR** and **Finance** departments.

>**Note**: Segments are nothing but a grouping of users

1. In **Microsoft Edge**, navigate to **[Microsoft Purview](https://compliance.microsoft.com/homepage)**

1. From the left-navigation pane, select **Information barrier (1)** drop-down, select **Segment (2)** and  click on **+ New segment (3)**.

   ![](../media/segments.png)

   ![](../media/segmentnew.png)

1. On the **Provide a segment name** page enter **HR (1)** in name field and click **Next (2)**.

    ![](../media/lab13-image21.png)

1. On the **Add user group filter** page click **+ Add (1)** from the dropdown select **Department (2)** and under **Department**. For **group operation** make sure **Equal (3)** is selected and in the Group name enter **HR (4)** and click on **Next (5)**.

    ![](../media/lab13-image22.png)

    ![](../media/lab13-image(23).png)
   
1. On the Summary page, click on **Submit**. Once, the segment created, select **Done**.

   ![](../media/submit1.png)

1. Repeat the last 4 steps to create another segment with the name **Finance**. 

   ![](../media/finance-hr.png)

## Task 3: Create Information barrier policies

In this task, you'll create Information barrier policies to block communication between the  **HR** and **Finance** departments.

1. From the left navigation pane of Microsoft Purview, expand the Information Barrier and select **Policies**.

   ![](../media/policies.png)

1. Click on **+ Create policy**.

   ![](../media/createpolicy.png)

1. On **Provide a policy name** page, enter **Block communication from HR to Finance (1)** and click on **Next (2)**.

     ![](../media/lab13-image24.png)

1. On the Add assigned segment details page, select **+ Choose segment**.

   ![](../media/choosesegment.png)
   
1. On Select assigned segment for this policy window select **HR (1)** and click on **Add (2)**.

   ![](../media/lab13-image25.png)

1. Back on **Add assigned segment details** page and click **Next**.

   ![](../media/next3.png)

1. On the **Configure communication and collaboration details** page, enter or select the following details:

   - **Communication and collaboration**: **Blocked (1)**
   
   - **+ Choose segment**: Select **Finance (2)** and click **Add**
   
   - Click **Next (3)**

   ![](../media/blocked.png)

1. On the **Configure policy status** page turn on the toggle for Set your policy to active state.

   ![](../media/lab13-image26.png)

1. On the Summary page click on **Submit** and **Done**.

1. Back on **Policies** page.

   ![](../media/policypage.png)

1. Click on **+ Create policy**.

   ![](../media/policypage1.png)

1. On the **Provide a policy name** page, enter **Block communication from Finance to HR (1)** and click on **Next (2)**.

   ![](../media/blockfinance.png)
   
1. On the Add assigned segment details page, select **+ Choose segment**.

   ![](../media/choosesegment1.png)

1. On Select assigned segment for this policy window select **Finance** and click on **Add**.

   ![](../media/financeadd.png)
    
1. Back on **Add assigned segment details** page and click **Next**.

   ![](../media/financeadd1.png)

1. On the **Configure communication and collaboration details** page, enter or select the following information:

   - **Communication and collaboration**: **Blocked (1)**
   
   - **+ Choose segment**: select **HR (2)** and click **Add**
   
   - Click **Next (3)**

      ![](../media/blocked1.png)

1. On the Configure Policy Status page, **turn on the toggle (1)** to set your policy to an active state. Select **Next (2)**.

    ![](../media/lab13-image26.png)

1. On Summary page click on **Submit** and **Done**.

   ![](../media/policies1.png)

### Task 4: Enable Scoped Directory Search on Microsoft Teams

In this task, you'll learn how to Enable Scoped Directory Search on Microsoft Teams

1. In **Microsoft Edge**, open a new browser tab, navigate to [Microsoft 365](https://www.office.com/) portal. 

   >**Note:** If it asks you for the **Sign in**, enter the following * Email/Username: **<inject key="AzureAdUserEmail"></inject>** and then click on **Next**. On **Enter Password** blade, enter the following * Password: **<inject key="AzureAdUserPassword"></inject>** and then click on **Sign in**.

1. Select **Admin** from left pane.

   ![](../media/admin.png)

1. On **Microsoft 365 admin center** portal, select **Show all**.

   ![](../media/microsoft365admincenter.png)
   
1. Under **Admin center** section, select **Teams**.

   ![](../media/teams.png)

1. On **Microsoft Teams admin center**, from the left navigation pane, expand **Teams (1)** select **Teams settings (2)** and scroll down under search by name  then turn on the toggle for **Scope directory search using an Exchange address book policy (3)**. Click on **Save (4)**. Select **Confirm** on the **Changes might take some time to take effect** pop-up.

     ![](../media/teamssettings.png)

## Task 5: Apply Information barrier policies

In this task, you will apply the active Information barrier policies and check their application status.

1. Naviagte back to the **Microsoft Purview** portal. From the left Navigation Pane, expand **Information Barrier (1)** and select **Policy application (2)**.

    ![](../media/lab13-image27.png)

1. On the Policy Application page, click on **Apply all policies**.

     ![](../media/lab13-image28.png)
   
1. Once the policy is applied, the **Status** will update from **NotStarted** to **Completed**.

     ![](../media/lab13-image29.png)

   >**Note**: Kindly **Refresh** page and Wait for the status to transition from **NotStarted** to **Completed**; this process may take 5 to 10 minutes.

### Task 6: Assess Information Barriers functionality within Microsoft Teams.

In this task, you'll test the Use Information Barriers policy which blocks users from sending messages in teams.

1. From the start menu type and select **Teams** and log in with the following credentials:

   * Email/Username: <inject key="AzureAdUserEmail"></inject>
   
   * Password: <inject key="AzureAdUserPassword"></inject>

1. After logging in to Microsoft Teams search and try to send some message to **John doe**.

1. Observe that **Administrator has disabled chat for this user**, you are not allowed to send messages to **John doe** as he is from **Finance** department.

     ![](../media/b-image14.png)

   >**Note** Kindly wait for 2 - 3 hours as the policy needs some time to take effect. Meanwhile, feel free to proceed with the next exercise.
    
1. Sign out as odl user and log in as **John doe** to Microsoft Teams.

1. Search and attempt to send a message to **ODL user** and observe that **Administrator has disabled chat for this user**, you are not allowed to send a message to **ODL user** as he is from **HR** department.

     ![](../media/b-image15.png)

    >**Note** Kindly wait for 2 - 3 hours as the policy needs some time to take effect. Meanwhile, feel free to proceed with the next exercise.

    >**Note**: If the users conducting these activities in Microsoft Teams are included in an IB policy to prevent the activity, they won't be able to proceed. In addition, everyone included in an IB policy can be potentially blocked from communicating with other users in Microsoft Teams. When users affected by IB policies are part of the same team or group chat, they may be removed from those chat sessions and further communication with the group may not be allowed.

   > **Congratulations** on completing the task! Now, it's time to validate it. Here are the steps:
   > - Navigate to the Lab Validation Page, from the upper right corner in the lab guide section.
   > - Hit the Validate button for the corresponding task. If you receive a success message, you can proceed to the next task. 
   > - If not, carefully read the error message and retry the step, following the instructions in the lab guide.
   > - If you need any assistance, please contact us at labs-support@spektrasystems.com. We are available 24/7 to help you out.
   
### Conclusion:
By completing these tasks, you successfully configured Information Barriers, assigned attributes and licenses, created segments and policies, and tested their functionality in Microsoft Teams. This ensures data security, compliance, and controlled communication within the organisation.

### Review 
During this lab, you've gained knowledge on the following:
+ Modifying the attribute and assigning a license for the user named *Johndoe*.
+ Creating segments for Information Barriers
+ Create Information barrier policies
+ Apply Information barrier policies
+ Assess Information Barriers functionality within Microsoft Teams.

## You have successfully completed the lab. Click on Next >>.
