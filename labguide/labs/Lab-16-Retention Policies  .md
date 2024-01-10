# Lab 16 - Configure Retention Policies

## Lab Overview

Retention policies are crucial components of information governance, allowing organizations to manage the lifecycle of their data, ensure compliance, and meet regulatory requirements. Here's an overview of the process to create and configure retention policies

## Lab scenario

In this lab, you'll use a retention policy to manage the data for your organization by deciding proactively whether to retain content, delete content, or retain and then delete the content. A retention policy lets you do this very efficiently by assigning the same retention settings at the container level to be automatically inherited by content in that container. 

In order to adhere to this law your organization has created a retention plan to retain all items in the organization for 3 months.

>**Note**: When you create and submit a retention policy, it can take up to seven days for the retention policy to be applied.

## Lab objectives

In this lab, you will complete the following tasks:

+ Task 1 – Create Retention Policy with Static mode
+ Task 2 - Create Retention Policy with Adaptive scope

## Estimated timing: 60 minutes

## Architecture diagram
![](../media/archi-10.png)

## Task 1 – Create Retention Policy with Static mode

In this exercise you will create a company-wide retention policy, apply a retention period, and set the locations that the policy will be applied to.

1. In **Microsoft Edge**, navigate to **https://compliance.microsoft.com**.

1. In the **Microsoft Purview** portal, in the left navigation pane, expand **Data lifecycle management** then select **Microsoft 365**.

    ![](../media/lab16-image1.png)

1. On the **Data lifecycle management** page, in the **Retention policies** tab select **+ New retention policy**.

   ![](../media/lab16-image2.png)

1. On the **Name your retention policy** page, for the **Name** enter **Retention policies** and  click **Next**.

      ![](../media/lab16-image3.png)


1. On the **Policy Scope** page select **Next**.

   ![](../media/lab16-image4.png)


1. In the **Choose the type of retention policy to create** area, select **Static** then select **Next**.

   ![](../media/lab16-image5.png)

1. In the **Choose where to apply this policy** enable and select **Next**.

   - **Exchange mailboxes**
   - **SharePoint classic and communication sites**
   - **OneDrive accounts**
   - **Microsoft 365 Group mailboxes & sites**

     ![](../media/lab16-image6.png)

1. On the **Decide if you want to retain content, delete it, or both** page, for the **Retain items for a specific period** section, enter the following information and select **Next**.

   - **Retain items for a specific period**: Choose **Custom** from the dropdown list.
   - Change the years field to **0**, month field to **3** and days to **0**.
   - **Start the retention period based on**: When items were last modified.
   - **At the end of the retention period**: Delete items automatically.

      ![](../media/lab16-image7.png)

      ![](../media/lab16-image8.png)

1. On the **Review and finish** page select **Submit**.

    ![](../media/lab16-image9.png)

1. Once your policy is created select **Done**.

You have successfully created a retention policy for the Exchange email, Microsoft 365 groups, OneDrive, and SharePoint sites locations. This retention policy will retain items in these locations for three years from when the item was last modified date. This policy can take up to 24 hours to be apply in your tenant, but you can proceed to the next step.


## Task 2 – Create Retention Policy with Adaptive scope

In this exercise you will create a retention policy for the finance and legal department. The purpose of the policy is to comply with the law, retaining all legal related documents for 5 years. First you will create an adaptive scope including the legal and the retail department, then you will create a retention policy using this scope.


1. In **Microsoft Edge**, navigate to **https://compliance.microsoft.com**.

1. In the **Microsoft Purview** portal on the left navigation pane expand **Roles & scopes** then select **Adaptive scopes**.

   ![](../media/lab16-image11.png)

1. On the **Adaptive scopes** page select **+ Create scope**.

   ![](../media/lab16-image12.png)

1. On the **Name your adaptive policy scope** page input and select **Next**.

    - **Name**: Legal Documents Retention
    - **Description**: Retention for legal related documents

       ![](../media/lab16-image13.png)

1. On the **Assign admin unit** page select **Next**.

    ![](../media/lab16-image14.png)

1. On the **What type of scope do you want to create?** page select **Users** then select **Next**.

    ![](../media/lab16-image15.png)

1. On the **Create the query to define users** page, under **User attributes** specify the following:
    
    - Select the drop-down menu for **Attribute** then select **Department**.
    - Attribute field select **is equal to** as the operator.
    - Enter **Legal** in the **Value** field.

1. To add a second attribute, select **+ Add attribute** on the **Create the query to define users** page.

    ![](../media/lab16-image16.png)

1. For the **Query operator**, **Attribute**, **Operator**, and **Value** input, ensure the checkboxes are selected next to each attribute then select **Next**.

   - **Query operator**: Or
   - **Attribute**: Department
   - **Operator**: is equal to
   - **Value**: Retail

   ![](../media/lab16-image17.png)

1. Ensure the checkboxes are selected next to each attribute then select **Next**.

   ![](../media/lab16-image29.png)

1. On the **Review and finish** page select **Submit**.

    ![](../media/lab16-image18.png)

1. On the **Your scope was created page** select **Done**.

1. In the **Microsoft Purview** portal, in the left navigation pane, expand **Data lifecycle management** then select **Microsoft 365**.

1. On the **Data lifecycle management** page select the **Retention policies** tab then select **+ New retention policy**.

1. On the **Name your retention policy** page input and select **Next**.

    - **Name**: Legal Data Retention
    - **Description**: Retention of all documents within the legal and retail departments.

      ![](../media/lab16-image21.png)

1. On the **Policy Scope** page select **Next**.

    ![](../media/lab16-image22.png)

1. On the **Choose the type of retention policy to create** page select **Adaptive** then select **Next**.

    ![](../media/lab16-image23.png)

1. On the **Choose adaptive policy scopes and locations** page select **+ Add scopes** and in the right flyout **Choose adaptive policy scopes** page select the checkbox for **Legal Documents Retention** then select the **Add** button.

     ![](../media/lab16-image24.png)

1. Back on the **Choose locations to apply the policy** enable and select **Next**.

    - **Exchange mailboxes**
    - **OneDrive accounts**
    - Leave all other locations disabled.
 
      ![](../media/lab16-image25.png)

1. On the **Decide if you want to retain content, delete it, or both** page, for the **Retain items for a specific period** section input and select **Next**.

    - **Retain items for a specific period**: Choose **Custom** from the dropdown list.
    -  Change the **years** field to **0**, **month** field to **3** and **days** to **0**.
    - **Start the retention period based on**: When items were created
    - **At the end of the retention period**: Do nothing

        ![](../media/lab16-image26.png)

1. On the **Review and finish** page select **Submit**.

    ![](../media/lab16-image27.png)

1. Once your policy is created, select the **Done** button.

1. On the **You successfully created a retention policy** page select **Done**.

   You have successfully applied an adaptive scope to a retention policy.

   >**Note**: Retention policies are crucial for organizations to systematically manage data, comply with legal requirements, and enforce consistent information governance. By creating retention policies, Contoso Ltd. aims to adhere to state laws that specify the deletion of records after one day. 

### Conclusion

By completing the tasks outlined in this lab, users gain practical skills in creating retention policies with both static and adaptive scopes. This knowledge is essential for organizations to implement effective information governance, ensuring compliance with legal regulations. The lab emphasizes the importance of configuring retention policies to meet specific organizational and regulatory needs.


### Review
During this lab, you've gained knowledge on the process of Create Retention Policy with Static mode and Adaptive scope
  
### You have successfully completed the lab
