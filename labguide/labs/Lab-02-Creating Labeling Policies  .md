# Lab 02 - Publish sensitivity labels 

## Lab Overview 

The task aims to provide a streamlined method for publishing sensitivity labels to users. Users are guided through a series of steps within Microsoft Purview, specifically under Label policies. The objective is to make the selected labels, such as Confidential-Finance and Highly-Confidential, available to all users, ensuring consistent and standardized data protection measures.

## Lab scenario

In this lab, you need to publish them to make them available to people and services in your organization.  After you create your sensitivity labels, The sensitivity labels can then be applied to Office documents and emails, and other items that support sensitivity labels.

## Lab objectives

In this lab, you will complete the following tasks:

+ Task 1: Publish the sensitivity label to user
  
## Architecture diagram

![](../media/purview-lab2.png)

### Task 1 : Publish the sensitivity label to user

In this task, you'll focus on publishing existing sensitivity labels in Microsoft Purview. The process involves navigating through the Information Protection section and selecting specific labels to be published. This step is crucial for making the defined sensitivity labels accessible and applicable to all users within the organization.

1. On the Microsoft Purview, under Solutions, Expand **Information protection** and in the dropdown select **Label policies** and click on **Publish label**.

   ![](../media/lab2-image1.png)    

    
1. Select **Choose sensitivity labels to publish**. A window opens that provides information about the policy. Select **Confidential-Finance**  and **Highly-Confidential** from label and select **Add**

    ![](../media/lab1-image19.png)    

1. Back on **Choose sensitivity labels** blade, click on **Next**.

     ![](../media/lab2-image3.png)    
     
1. Under the Sensitivity labels to publish.  Don’t change any settings.  Select **Next** on the bottom of the page.

     
1. Click on **Next** on Assign Admin Units(Preview) page.

     ![](../media/lab2-image4.png)    

1. Read the description under “Publish to users and groups”.  Notice the this label is available to all users.  Don’t change any settings.  Select **Next** on the bottom of the page.

    ![](../media/lab2-image5.png)   

1. Under the policy settings.  Don’t change any settings.  Select **Next** on the bottom of the page.

    ![](../media/lab2-image6.png)   

1. Under the **Apply a Default label to documents**.  Don’t change any settings.  Select **Next** on the bottom of the page.

    ![](../media/lab2-image7.png)   

1. Under the **Apply a Default label to emails**.  Don’t change any settings.  Select **Next** on the bottom of the page.

     ![](../media/lab2-image8.png)   
    
1. Under the **Apply a default label to meetings and calendar events**.  Don’t change any settings.  Select **Next** on the bottom of the page.    

   ![](../media/lab2-image9.png)   
    
1. Under the **Apply a default label to Power BI content**.  Don’t change any settings.  Select **Next** on the bottom of the page.

     ![](../media/lab2-image10.png)   
    
1. The last configuration option is to name your policy. Enter the policy name as **Confidential-Policy**.  Select **Next** on the bottom of the page to exit the policy configuration and return to the Information protection page.

   ![](../media/lab1-image20.png)   
    
1. Review the settings and click on **Submit** and then select **Done**.

   ![](../media/lab2-image12.png)   
    
   ![](../media/lab2-image13.png)   

1. Back to **Label policies** blade and notice newly publish label.


>**Note**: Publishing sensitivity labels is essential for ensuring uniform data protection across the organization. By making these labels available to all users, organizations can enforce consistent policies for handling sensitive information. This step contributes to a cohesive approach to data security and compliance, as it ensures that established sensitivity labels are effectively communicated and applied throughout the user base.


### conclusion

The conclusion emphasizes the importance of publishing sensitivity labels as a critical step in the overall data protection strategy. By making labels available to all users, organizations can enforce standardized security measures, fostering a culture of responsible data handling. The conclusion also highlights the user's ability to review and confirm the published labels, ensuring the successful implementation of the publishing process.


## Review
In this lab, you have completed:
+ Explore on how to Publish sensitivity labels

## You have successfully completed the lab
