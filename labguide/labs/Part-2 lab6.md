# Part:2 lab 6 - Safe breach simulation

## Lab scenario
In this lab, you will explore how the simulations are benign cyberattacks that you run in your organization. These simulations test your security policies and practices, as well as train your employees to increase their awareness and decrease their susceptibility to attacks.

## Lab objectives

In this lab, you will complete the following task:

+ Task : Insights and reports on the Overview tab of Attack simulation training 

## Task 1: Insights and reports on the Overview tab of Attack simulation training

To explore on Simulation Insights, go to the **Overview** tab, open the Microsoft Defender portal at **https://security.microsoft.com**, go to **Email & collaboration** > **Attack simulation training**, and verify that the **Overview tab** is selected (it's the default). To go directly to the Overview tab on the **Attack simulation training** page, use **https://security.microsoft.com/attacksimulator?viewid=overview**, The rest of this section describes the information that's available on the Overview tab of Attack simulation training.


1. The **Recent simulations** card on the **Overview tab** shows the last three simulations that you've created or run in your organization.

1. You can select a simulation to view details.

1. Selecting **View all simulations** takes you to the **Simulations** tab.

1. Selecting **Launch a simulation** starts the new simulation wizard. For more information, see Simulate a phishing attack in Defender for Office 365.

## Attack simulation report

1. You can open the **Attack simulation** report from the **Overview tab** by clicking on the **View Report**

2. On the **Attack simulation report** page, the **Training efficacy tab** is selected by **default**.

3. On the **User coverage tab**, the chart shows the **Simulated users** and **Non-simulated users**. If you hover over a data point in the chart, the actual values are shown.

   **The details table below the chart shows the following information**:

```
      1) Username
      2) Email address
      3) Included in simulation
      4) Date of last simulation
      5) Last simulation result
      6) Count of clicked
      7) Count of compromised
```

## Training completion

1. On the **Training completion tab**, the chart shows the number of **Completed**, **In progress**, and **Incomplete**.

   **The details table below the chart shows the following information**:

```
     1)  Username
      2) Email address
      3) Included in simulation
      4) Date of last simulation
      5) Last simulation result
      6) Name of most recent training completed
      7) Date completed
      8) All trainings
```

## Repeat offenders

1. A **repeat offender** is a user who was compromised by **consecutive simulations**.

2. On the **Repeat offenders tab**, the chart organizes repeat offender data by simulation type:

```
      1) All
      2) Credential Harvest
      3) Malware Attachment
      4) Link in Attachment
      5) Link to Malware
      6) Drive-by URL
```
3. If you **hover** over a **data point** in the chart, the actual **values** are shown.

4. The details table below the chart shows the following information:

```
      1) User
      2) Repeat count
      3) Simulation types
      4) Simulations
```

5. If you select the **Export report button**, report generation progress is shown as a **percentage** of complete. In the dialog that opens, you can choose to open the **.csv file**, **save the .csv file**, and remember the selection.

## Review
In this lab, you will complete the following task:
+ Insights and reports on the Overview tab of Attack simulation training 
