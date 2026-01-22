# Lab 15: Explore eDiscovery

## Lab Overview
In this lab you will go through the steps required for setting up Core eDiscovery and then go through the Core eDiscovery workflow, by creating an eDiscovery hold, creating a search query, and then exporting the results of the search.  Note:  Licensing for Core eDiscovery requires the appropriate organization subscription and per-user licensing. If you aren’t sure which licenses support core eDiscovery, visit Get started with Core eDiscovery.

## Lab Objectives

In this lab, you will complete the following tasks:

+ **Task 1:** Add specific users as members of the eDiscovery Manager role group
+ **Task 2:** Create a case to start using Core eDiscovery
+ **Task 3:** Create an eDiscovery hold
+ **Task 4:** Create a search query

## Estimated timing: 60 Minutes

## Architecture diagram

![](../Images/sc900lab15.png)

## Task 0: Create sample data for eDiscovery search

1. On the Lab VM click **Microsoft edge** shortcut on the desktop and in the new browser, enter the URL below to Microsoft 365 Copilot and click on Sign in.

     ```
     https://www.office.com/
     ```

     ![](../Images/lab15-l0.png)

1. You'll see the **Sign in** tab. Here, enter your credentials:
 
    * **Email/Username:** <inject key="AzureAdUserEmail"></inject>

      ![](../Images/lab15--l2.png)

1. Next, provide your password:

    * Enter **Temporary Access Pass:** <inject key="AzureAdUserPassword"></inject>
  
      ![](../Images/lab15--l3.png)

1. When prompted to stay signed in, select **Yes**. This takes you to the Microsoft 365 admin center page.

1. On Welcome to Copilot Chat window, click **Apps (1)**, then select **word (2)**.

     ![](../Images/lab15--l1.png)

1. On word document select **Blank document** to create a new blank document and then enter the content **(1)** and enter name as **Sales Report Q1 (2)** 

    ```
    This document contains the Sales performance details for Q1.

    The Sales team achieved good growth this quarter.
    Future Sales targets and projections will be discussed in the next review meeting.

    This file is created for testing Microsoft Purview eDiscovery search using the keyword "Sales".
    ```

    ![](../Images/lab15--l4.png)


## Task 1: Add specific users as members of the eDiscovery Manager role group

To access Core eDiscovery or be added as a member of a Core eDiscovery case, a user must be assigned the appropriate permissions. In this task, you as the global admin, will add specific users as members of the eDiscovery Manager role group.

1. If you not already login to admin center, in the address bar of Microsoft edge enter **[admin.microsoft.com](https://admin.microsoft.com)**.

1. On **Sign in** blade, you will see a login screen, in that enter the following email/username 
 
    * Email/Username: **<inject key="AzureAdUserEmail"></inject>** and then click on **Next**.

    * Password: **<inject key="AzureAdUserPassword"></inject>** and then click on **signin**

1. From the left navigation pane of the Microsoft 365 admin center, select **Show all**.

    ![](../Images/lab12-l1.png)

1. Under Admin centers, select **Microsoft Purview**.  A new browser page opens to the welcome page of the Microsoft Purview portal. 

     ![](../Images/lab12-l2.png)

1. On **Welcome to the new Microsoft Purview portal!**, select **Get started**.

     ![](../Images/lab12-l3.png)

1. From the left navigation panel, select **Settings (1)**, expand **Roles & scopes (2)** then select **Role groups (3)**.

    ![](../Images/lab15-l1.png)

1. In the search field, on the top, right of the page, enter **eDiscovery (1)** then hit Enter on your keyboard.  Select **eDiscovery Manager (2)**.

    ![Picture 1](../Images/lab15-l2.png)
    
1. Select **Edit**. For the purpose of this lab, you'll set yourself as MOD administrator as the eDiscovery Manager and administrator.  In practice, you would designate specific users for specific roles.

    ![Picture 1](../Images/lab15-l3.png)

1. The "Manage eDiscovery Manager" page allows you to add users to the role of eDiscovery manager.

1. On **Manage eDiscovery Manager** page, click **Choose users (1)**. Search for and select **ODL_User<inject key="DeploymentId"></inject> (2)** then press **Select (3)**
    
    ![Picture 1](../Images/lab15-l4.png)

1. On **eDiscovery Manager** page, select **Next** on  **Manage eDiscovery Manager**.

   ![Picture 1](../Images/lab15-l5.png)

1. On **Manage ediscovery Administrator**, click on **Choose User (1)** and select **ODL_User<inject key="DeploymentId"></inject> (2)** from the list and click on **Select (3)** and **Next**.

    ![Picture 1](../Images/lab15-l6.png)

    ![Picture 1](../Images/lab15-l7.png)

1. On **Review and finish** page, select **Save**.

    ![Picture 1](../Images/lab15-l8.png)

1. On **You successfully updated the role group** window, click **Done**.

     ![Picture 1](../Images/lab15-l9.png)

1. Close all the tabs except the **[admin.microsoft.com](https://admin.microsoft.com)** and then **sign out** from the admin center page and **sign-in** back again to reflect the permissions added for users faster.

1. Keep this browser tab open, as you'll use it in the next task.

## Task 2: Create a case to start using Core eDiscovery
In this task you, as an eDiscovery Administrator (ODL admin is an eDiscovery administrator), will create a case to start using eDiscovery (Standard).

1. You should still be on the compliance portal roles page. If you closed the browser tab from the previous task, open a new browser tab and enter **https://purview.microsoft.com/** to get to the Microsoft Purview portal.

1. From the left navigation panel, under **Solutions (1)**, expand **eDiscovery** then select **Cases (2)** click on **Create case (3)**. If you select the down arrow you will open the window to create a search and in the process of creating a search will create a case.

     ![Picture 1](../Images/lab15-l10.png)
   
1. In the New case window, enter a Case name, **SC900 Test Case** then select the **Create** at the bottom of the page.

     ![Picture 1](../Images/lab15-l11.png)

1. The case should now appear on the list.

    ![Picture 1](../Images/lab15-l12.png)

1. As the creator of the case and because you have eDiscovery Administrator privileges, you can begin to work with it.  

1. Keep this browser tab open, as you will use it in the subsequent task.

## Task 3: Create a search query

With a case created, you can begin to work with the case. This includes creating a search query to find data and content that is relevant to your case, applying a hold policy, creating a review set, and exporting data. In this task you'll explore some of these options.

1. Open the SC900 Test Case tab on your browser.

2. From the SC900 Test Case page, select  **Create a search**. 

     ![Picture 1](../Images/lab15-l13.png)

3. In the name field, enter **SC900 case search (1)** then select **Create (2)**.

    ![Picture 1](../Images/lab15-l14.png)

4. Select **Add sources**. Note the filter options and default settings. In the search box, enter **ODL-User-<inject key="DeploymentID" enableCopy="false" /> (1)** then select **Search**. From the search results select **ODL-User-<inject key="DeploymentID" enableCopy="false" /> (2)**, then select **Save and close (3)**. 

     ![Picture 1](../Images/lab15-l15.png)

     ![Picture 1](../Images/lab15-l16.png)

5. The Condition builder allows you to build a search query based on specific Keywords or Conditions that are satisfied, In the keyword box, enter **Sales (1)**. From here you can select to **Run query (2)**

     ![Picture 1](../Images/lab15-l17.png)

6. From the Choose search results window. For the lab tenant, only the statistics view of the search results is available. Note the options to arrange by top indicators. Select **Run query**. This may take several minutes.

     ![Picture 1](../Images/lab15-l18.png)

     ![Picture 1](../Images/search.png)

7. With query results returned in the form of statistics, you can export results. Select **Export** to vew available options then select **Cancel**.

     ![Picture 1](../Images/lab15--l19.png)

5. You can add to a review set for further processing.  Select **Add to review set (1)**. Enter a name for the new review set, **`SC900-review-set` (2)**, leave the default settings, then select **Add to review set (3)**. This can take several minutes to complete. Once the review set results are presented, you can explore the different options, which include Analytics, Query, Actions, Tag files, and Manage.

    ![Picture 1](../Images/lab15-l27.png)
    
6. You can also create a hold policies to preserve content relevant to your case. From the Review set window, select the **Hold** tab.  This takes to you the Hold policies window. Select **New policy**.  Enter a Policy name, **`SC900-hold`**, and select **Create**.  As in the search, you need to add data sources for the hold and you can add keywords and conditions to use in the hold policy, then you can select **Apply hold**.  Actions you can take on a hold policy include retry, turn off a policy, and deleting a hold policy.


## Review
In this lab, you have completed:
- Added specific users as members of the eDiscovery Manager role group
- Created a case to start using Core eDiscovery
- Created an eDiscovery hold
- Created a search query
  
## You have successfully completed the lab
