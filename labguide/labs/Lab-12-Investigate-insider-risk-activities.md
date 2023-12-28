# Lab 12 - Investigate insider risk activities

## Lab scenario

## Lab objectives

In this lab, you will complete the following tasks:
+ Task 1 : Create Insider Risk Management Investigators
+ Task 2 : Investigate insider risk activities


## Architecture diagram
![](../media/archi-7.png)


### Task 1 : Create Insider Risk Management Investigators

In this task you, as the global administrator, will enable permissions for Insider Risk Management Investigators.  Specifically, you will add users to the Insider Risk Management Investigators role group to ensure that designated users can access and manage insider risk management Investigators features.

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

1. In the search bar, enter **Insider risk** then select the search icon (magnifying glass).  Notice the five roles that show up.  Each of these has different access levels.  Select **Insider Risk Management Investigators**.

    ![](../media/lab12-image1.png)

1. In the window that opens, next to where it says Members, select **Edit**. you may need to scroll to find it.

    ![](../media/lab12-image2.png)

1. On **Insider Risk Management Investigators** page, select choose users and select **<inject key="AzureAdUserEmail"></inject>** and then click on **select**.

    ![](../media/lab12-image3.png)

1. Back on **Insider Risk Management Investigators** page and click on **Next**.
   
    ![](../media/lab12-image4.png)

1. Review the role group and finish page click on **save**.
   
   ![](../media/lab12-image5.png)
  
1. On **You successfully updated the role group** page, click on **Done**.
  
### Task 2 : Investigate insider risk activities

In this task, you'll Investigate insider risk activities

1. Navigate to **Insider risk management** page, and select to user tab where you can view user activity

    ![](../media/lab12-image7.png)
   
   >**Note**: Review the settings for your insider risk policy. The policy will take effect immediately after you create it, but may take up to 24 hours to start generating alerts. User productivity won't be impacted in any way. 

   >**Note**: Investigating insider risk activities allows organizations to monitor user behavior, detect potential risks, and take timely actions to mitigate any threats. Understanding the policy settings ensures a comprehensive review of user activities.


### Conclusion:
By completing these tasks, the organization sets up a team of investigators with the appropriate roles, empowering them to handle insider risk incidents efficiently. Simultaneously, users can actively monitor and investigate insider risk activities, aligning with a proactive security strategy.

### Review
In this lab, you have completed:

+ Create Insider Risk Management Investigators
+ Investigate insider risk activities

## You have successfully completed the lab





