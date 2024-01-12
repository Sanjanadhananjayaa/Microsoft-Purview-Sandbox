# Lab 03 - Configure Message Encryption  

## Lab Overview
The task guides users through the steps of creating an encryption rule using the Exchange admin center. Users are instructed to navigate to the Mail flow section, add a new rule, set rule conditions, and define actions for message security, including the application of Microsoft 365 Message Encryption and rights protection.

## Lab scenario

In this lab, you'll configure Microsoft Purview Message Encryption which enables organizations to securely share protected emails across any device. Users can send encrypted messages not only within Microsoft 365 organizations but also with external parties using services like Outlook.com, Gmail, and other email platforms.

## Lab objectives

In this lab, you will complete the following task:

+ Task 1: Create a Mail Flow Encryption Rule using the Exchange admin center

## Estimated timing: 60 minutes

## Architecture diagram

![](../media/part1lab3.png)

### Task 1: Create a Mail Flow Encryption Rule using the Exchange admin center

In this task, you will create a Mail Flow Encryption Rule within the Exchange admin center to secure messages within the Exchange Online environment. The objective is to establish a rule that encrypts emails under specific conditions, contributing to enhanced data security.

1. In the [admin microsoft com](https://admin.microsoft.com/) portal 

1. From the left navigation pane select **Show all** > **Exchange**. This will open the Exchange admin center.

1. In the **[Exchange admin center](https://admin.exchange.microsoft.com/)**, select **Mail flow (1)** > **Rules (2)** > **+ Add a rule (3)** > **Create a new rule (4)**.

    ![Picture 1](../media/image1-lab3.png)

1. In the **Set rule conditions** window, in the **Name** box, enter **Encrypt mail** as the name of this rule.

1. Select the drop-down arrow in the **Apply this rule if** condition box. In the drop-down menu, select **The recipient (1)** and **is this 
    person (2)** and on **Select members (3)** blade select <inject key="AzureAdUserEmail"></inject> click on **Save (4)**.

   ![Picture 1](../media/image2-lab3.png)

   ![Picture 1](../media/image3-lab(3).png)

1. You need to add more conditions, so next to **is this person** click the **+** to the right.

   ![Picture 1](../media/image4-lab3-4-(2).png)

1. Under **And** select **The recipient (1)** and **is external/internal (2)**. In the blade that opens to the right, select **Outside the organization (3)** > **Save (4)**.

   ![Picture 1](../media/image4-lab3-4.png)

   ![Picture 1](../media/image4-lab3-4-(1).png)

1. You now need to define an action to perform when this rule is applied. Under **Do the following**, select **Modify the message security (1)** and **Apply Microsoft 365 Message Encryption and rights protection (2)**

   ![Picture 1](../media/image4-lab3.png)

1. In the **select RMS template** dialog box, select **Encrypt (1)** > **Save (2)**. Click **Next**.

   ![Picture 1](../media/image5-lab3.png)

1. On the **Set rule settings** window, click the checkbox next to **Activate this rule on (1)**. That should automatically populate a date and time that will make the rule take effect immediately upon completion.

   ![Picture 1](../media/image6-lab3.png)

1. Click **Next** > **Finish** > **Done**.

1. In the **Rules** window, click the name of the rule under the **Rules** column. In the window that opens to the right, click the toggle under Enable or disable rule to **Enabled** the rule. Close the window.

   ![Picture 1](../media/image8-lab3.png)

   >**Note**: Creating a Mail Flow Encryption Rule is essential for organizations seeking to enhance the security of their email communication. By defining conditions and actions, such as encrypting messages for external recipients, organizations can safeguard sensitive information and ensure that communication remains confidential, especially when shared outside the organizational boundaries.

### Conclusion:
The conclusion emphasizes the completion of the Mail Flow Encryption Rule creation process. By activating the rule, organizations can immediately apply encryption to relevant messages, reinforcing their commitment to data protection. The conclusion also highlights the user's ability to enable or disable the rule as needed, providing flexibility in managing encryption policies.

### Review

During this lab, you've gained knowledge on the process of creating a Mail Flow Encryption Rule using the Exchange admin center.

### You have successfully completed the lab

### Click on Next to continue with the next lab
