# Lab 12: Explore the Microsoft Purview portal and Compliance Manager

## Lab Overview

In this lab, you will explore the Microsoft Purview compliance center home page and ways in which the capabilities of Compliance manager can help organizations improve their compliance posture.

## Lab Objectives

In this lab, you will complete the following tasks:

+ **Task 1:** Explore the Microsoft Purview compliance center
+ **Task 2:** Compliance posture through Compliance Manager

## Estimated timing: 60 Minutes

## Architecture diagram

![](../Images/sc900lab12.png)


## Task 1: Explore the Microsoft Purview compliance center
 In this task  you will Explore the Microsoft Purview compliance center home page and learn to customize the card view and the navigation panel.

1. On the Lab VM click **Microsoft edge** shortcut on the desktop and enter **admin.microsoft.com**.

     ![](../Images/lab12-0.png)

2. Sign in with your admin credentials.
   
3. In the Sign in window enter you will see a login screen, in that enter the following email/username and then click on **Next**. 

    * Email/Username: <inject key="AzureAdUserEmail"></inject>

4. Now enter the password and click on Sign in.
   
   * Password: <inject key="AzureAdUserPassword"></inject>
  
5. When prompted to stay signed-in, select **Yes**. This takes you to the Microsoft 365 admin center page

6. From the left navigation pane of the Microsoft 365 admin center, select **Show all**.

     ![](../Images/lab12-l1.png)

7. Under Admin centers, select **Microsoft Purview**.  A new browser page opens to the welcome page of the Microsoft Purview portal.

     ![](../Images/lab12-l2.png)
   
9. On **Welcome to the new Microsoft Purview portal!**, select **Get started**.

     ![](../Images/lab12-l3.png)
     
10. The card section on the home page shows you, at a glance, how your organization is doing with your compliance posture, what solutions are available for your organization, available trials and recommendations, and more.

11. View the information on the landing page. Scroll down to see your compliance posture status, information related to **Know your data**, and more.

     ![](../Images/lab12-l3b.png)
   
12. Scroll up and select the tile that says **View all solutions**.
    
     ![](../Images/lab12-l4.png)
     
13. Leave the browser tab open.

## Task 2: Compliance posture through Compliance Manager

In this tak you will learn about your organization’s compliance posture through Compliance Manager.

1. From the left navigation panel of the Microsoft Purview portal, select **Solutions (1)** and select **Compliance Manager (2)**. Alternatively, you could select the tile for Compliance Manager, under Risk and Compliance.

      ![](../Images/lab12-l5.png)

2. You are on the Overview page. Scroll down to see all the information available on the page. Information on this page includes your compliance score, your points achieved, and Microsoft managed points achieved. You'll see Key improvement actions, Solutions that affect your score and compliance score breakdown by categories.

     >**Note:** If the Compliance Score is shown as zero percentage, try refreshing the page or sign-out and sign-in again.
 
3. From the left navigation pane, select **Improvement actions**.  These are actions that can improve the organization’s compliance score, points may take up to 24 hours to update.  Notice the available filters.

     ![](../Images/lab12-l6.png)

4. From the list of improvement actions, search for **Enable self-service password reset (1)**, then select **Enable self-service password reset (2)**.  Each improvement action has an overview section along with the details page from which you can select implementation, testing, the related standards and regulatory requirements, and documents.

     ![](../Images/lab12-7a.png)

     ![](../Images/lab12-7.png)

5. Exit out of this improvement action by selecting **Improvement Actions** from the breadcrumb on the top left of the page. You are now back on the improvement actions page.

     ![](../Images/lab12-l8.png)

6. From the left navigation pane, select **Solutions**. On this page, you'll see how solutions contribute to your score and their remaining opportunity for improvement.

      ![](../Images/lab12-l9.png)

7. From the left navigation pane, select **Assessments (1)**. On this page you will see the Data Protection Baseline for Microsoft 365. This is a default assessment Microsoft provides in Compliance Manager for the Microsoft 365 data protection baseline.  This baseline assessment has a set of controls for key regulations and standards for data protection and general data governance. Compliance Manager becomes more helpful as you build and manage your own assessments to meet your organization's particular needs.

     ![](../Images/lab12-l10.png)

8. Select **Data Protection Baseline for Microsoft 365 (2)**. Notice the information available on the progress tab. You can also view status of controls for this assessment, your improvement actions, Microsoft actions.

     ![](../Images/lab12-l11.png)

9. From the left navigation pane, select **Regulations**.  This page lists the regulations available to your organization. Select any regulation listed. You will see specific information about that regulation including controls, your improvement actions, and Microsoft action.

     ![](../Images/lab12-l12.png)
 
10. From the left navigation pane, select **Policies (1)**. Here is where you'll see the list of policies to help you monitor and get notified about events in Compliance Manager that are of importance to you. You can create or modify policies, change their activation status, and control alert frequency and severity. Select the **Compliance Manager Default Alert Policy (2)** to view details about the policy.  Select **Actions (3)** to view available options (explore at will).

     ![](../Images/lab12-l14.png)

11. From the left navigation pane, select **Alerts**. Here you can view and manage alerts for events that can affect your organization's compliance score. Since this is a newly created lab tenant, you should not be seeing any alerts.

     ![](../Images/lab12-l15.png)

12. From the left navigation panel, select **Home** to return to the landing page of the Microsoft Purview portal.

13. Close the open browser tabs.

## Review
In this lab, you have completed:
- Explored the Microsoft Purview compliance center
- Compliance posture through Compliance Manager
  
## You have successfully completed the lab
