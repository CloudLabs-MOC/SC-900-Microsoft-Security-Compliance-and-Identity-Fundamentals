 
# Lab 01: Explore Microsoft Entra ID User Settings

## Lab Overview

In this lab, you'll explore Microsoft Entra ID, perform essential tasks such as user and group management, licensing, and first-time user sign-in. You will create a user, configure group assignments, manage licenses, and explore some of the available services in Microsoft Entra ID.

## Lab Objectives

In this lab, you will complete the following tasks:

+ Task 1: Accessing Microsoft Entra ID through the Microsoft 365 Admin portal
+ Task 2: Creating a basic group
+ Task 3: Create a new user in the Microsoft Entra ID and explore some of the services
+ Task 4: Sign in to the user first time

## Estimated timing: 30 Minutes

## Architecture diagram

![](../Images/sc900lab1.png)

## Task 1: Accessing Microsoft Entra ID through the Microsoft 365 Admin portal and through the Azure portal

In this task, you will walk through accessing Microsoft Entra ID through the Microsoft 365 Admin portal.

1. Open another tab in Microsoft Edge, in the address bar enter **[admin.microsoft.com](https://admin.microsoft.com/)** to access the Microsoft 365 admin center.

1. Sign in with the following credentials.
    
    -  In the Sign in window enter following email then select **Next**.

       * Email : **<inject key="AzureAdUserEmail"></inject>**
     
    -  Enter the admin following password and select **Sign in**.

       * Password : **<inject key="AzureAdUserPassword"></inject>** 
          
1. From the left navigation pane of the Microsoft 365 admin center, select **Show all**.

    ![](../Images/id1.png)

1. Under Admin centers, select **Identity** (you may need to scroll down).  

    ![](../Images/id2.png)

1. From the left navigation pane, under favorites select **Entra ID**. In the main window, you will see another navigation panel that lists all the services that are available in Microsoft Entra ID. To the right, you will see information about the tenant and links to identity types you can create and featured services.  

    ![](../Images/id3.png)    


## Task 2: Creating a basic group

In this task, you will create a Microsoft 365 group in Microsoft Entra ID, assign a group name and description, and manage group settings.

1. From left navigation pane select **Groups (1)** under the **Entra ID** section and then select **New group (2)**.

    ![](../Images/sc3.png)

1. Populate the **New Group** fields as follows and select **Create (4)**

    - Group type: **Microsoft 365 (1)**.

    - Group name: **Operations (2)**.

    - Group email address: **Leave Default**.

    - Group description: **Add an optional description to your group (3)**.

        ![](../Images/sc4.png)

         > **Note:** Kindly refresh the screen if the newly created group is not visible in **All groups** section.

> **Congratulations** on completing the task! Now, it's time to validate it. Here are the steps:
> - Hit the Validate button for the corresponding task. If you receive a success message, you can proceed to the next task.
> - If not, carefully read the error message and retry the step, following the instructions in the lab guide. 
> - If you need any assistance, please contact us at cloudlabs-support@spektrasystems.com. We are available 24/7 to help you out.

 <validation step="6be841cf-5bd0-4c51-9b70-a308b628beb9" />

## Task 3: Create a new user in the Microsoft Entra ID and explore some of the services

In this task, you’ll learn how to create a new user in the Microsoft Entra ID and explore some of the services that can be managed at the user level.

1. From the left navigation pane, select **Users (1)**.  This takes you to the  users page. **All users (2)** should already be selected. Notice that your tenant is already configured with users **(3)**.

    ![](../Images/sc1.png)

1. Select **+ New user (1)** then from the drop-down box, select **Create new user (2)**.

    ![](../Images/sc2.png)
   
1. Populate the **Identity** fields as follows and select **Next: Properties > (5)**.

    - User principal name: **sara (1)**

    - Display Name : **Sara Perez (2)**

    - Uncheck **Auto-generate password (3)**

    - Password:  **Enter a temporary password (4)** that adheres to the password requirements and make note of it, as you will need it to complete the subsequent task.
  
      ![](../Images/sc5.png)

       >**Note** : When Sara signs in for the first time, she will be prompted to change her password.

1. On the **Properties** tab under settings specify the following and select **Next: Assignments > (2)**

    - Usage location: **United States (1)** (select the drop-down then scroll down to find this option). Configuring usage location is required for assigning licenses.

      ![](../Images/sc6.png)
   
1. In the **Assignments** tab :

    - Click **+ Add Group**, this displays the available groups.  Notice the list of available groups.

        ![](../Images/sc56.png)

    - Select **Operations (1)**, you may need to scroll down, then press **Select (2)**. Notice how the text next to groups has been updated to reflect 1 group selected.  

       ![](../Images/sc7.png)

1. Next to Roles, select **+ Add role (1)**. The list of Directory roles appears.  Scroll down to view the various built-in roles, to view the various roles, but don’t change the user role.  Close out of this window by selecting the **X (2)** on the top right-hand corner of the page.

    ![](../Images/sc8.png)

1. From the bottom of the page, select the **Next: Review + create >**.

    ![](../Images/sc9.png)

1. Then **Create** button.

    ![](../Images/sc10.png)

1. You are returned to the users page.  After a few seconds, **Sara Perez (2)** will be listed.  You may need to select the **refresh (1)** icon on the top of the page.

    ![](../Images/sc11.png)

1. From the user list, select the user you created, **Sara Perez**.  The **Overview** page opens.

    ![](../Images/sc12.png)

1. The left navigation panel shows the various options that can be configured for the user. View the available options.

1. From the left navigation panel, select **Licenses (1)**.  Notice that there are no license assignments found for this user, also note the warning icon that says, `Adding, removing, and reprocessing licensing assignments is only available within the M365 Admin Center.`  To add a license, click on **Go to the Microsoft 365 admin center (2)** from the alert message.

    ![](../Images/sc14.png)

1. If prompted, log in to the **Microsoft 365 admin center**. Since you are already signed in as <inject key="Username" enableCopy="false" />, you will be automatically logged in when you access the portal.

     ![](../Images/T3-S12a.png)
    
1. From the left navigation panel, under **Users (1)**, select **Active users (2)**.

     ![](../Images/T3-S13.png)

1. From the list of users, select **Sara Perez**.

     ![](../Images/T3-S14.png)

1. A window will open displaying the user's information. Select the **Licenses and apps (1)** tab. Check the box for **Office 365 E3 (no Teams) license (2)** and click **Save changes (3)**. A notification at the top of the screen will confirm that the license assignment was successful. Close the window by clicking the **X (4)** in the top-right corner.

     ![](../Images/T3-S15a.png) 

1. You have successfully assigned a license to the user.

1. Copy and paste the username of **Sara** as you will use it to sign in for the next task.

     ![](../Images/sc16.png) 

1. Sign out of all the open browser tabs. Sign out by selecting the user icon next to the email address on the top right corner of the screen then selecting **Sign out**. Close all the browser windows.

     ![](../Images/sc17.png) 


> **Congratulations** on completing the task! Now, it's time to validate it. Here are the steps:
> - Hit the Validate button for the corresponding task. If you receive a success message, you can proceed to the next task.
> - If not, carefully read the error message and retry the step, following the instructions in the lab guide. 
> - If you need any assistance, please contact us at cloudlabs-support@spektrasystems.com. We are available 24/7 to help you out.
     
<validation step="23fc9a6d-edce-49f8-99f4-7f3727e3124f" />

## Task 4: Sign in to the user first time

In this task, you will sign in as Sara Perez, for the first time.

1. Open Microsoft Edge.

1. In the address bar, enter **`https://login.microsoft.com`**.

1. Sign in using the email address **sara@xxxx.onmicrosoft.com** that you copied in step 18 of Task 3.

   ![](../Images/sc900-image18.png)

   >**Note** : You can retrieve the email ID from the Entra ID Users page.

1. Enter the temporary password that you have provided earlier.

    ![](../Images/sc900-image19.png)

1. You are now prompted to Update your password. In the Current password field, enter the temporary password that you have provided earlier.

1. In the New password field enter, **SC900-Lab**.  In the Confirm your password field enter **SC900-Lab**, then select **Sign in**.
   >**Note** : As a best practice, a more secure password should be used. This password is chosen, for expediency and only for the purpose of this lab.

     ![](../Images/sc900-image20.png)

1. Since this is the first time you are logging in as Sara Perez, you may be prompted to setup MFA. Follow the prompts on the screen to setup MFA.

1. In **android**, go to the play store and Search for **Microsoft Authenticator** and Tap on **Install**. 

   ![](../Images/mfa1.png)

   > **Note:** For IOS, Open the app store and repeat the steps.

   > **Note:** Skip if already installed.

1. On **Set up your account in app**, click **Next**.

    ![](../Images/mfa2.png)

1. Scan the QR code visible on the screen and click on **Next**.

   ![QR code](../Images/mfa3.png)

1. Enter the digit displayed on the Screen in the Authenticator app on mobile and tap on **Yes**.

    ![QR code](../Images/mfa4.png)

1. Once the notification is approved, click on **Next**.

1. Click on **Done**.

    ![](../Images/mfa5.png)

1. If prompted to stay signed in, you can click **"No"**.

1. You should now be successfully signed in to **Microsoft 365**.

     ![](../Images/sc18.png)

1. **Sign out** from all the browser tabs by clicking on the user icon next to the email address on the top right corner of the screen. Then close all the browser windows.

## Review

In this lab, you started your initial exploration of Microsoft Entra ID. Since subscribers to Microsoft 365 are automatically using Microsoft Entra ID, you found that you access Microsoft Entra ID features and services through either the Microsoft 365 admin portal or through the Azure portal.  Whichever approach you prefer to get to the same place.  You also walked through the process of creating a new user and the different setting that can be configured, including groups to which the user can be assigned, the availability of roles, and assigning of user licenses.

## You have successfully completed the lab

