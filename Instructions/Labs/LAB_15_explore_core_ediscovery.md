# Lab: Explore the Core eDiscovery workflow

## Lab scenario
In this lab you will go through the steps required for setting up Core eDiscovery and then go through the Core eDiscovery workflow, by creating an eDiscovery hold, creating a search query, and then exporting the results of the search.  Note:  Licensing for Core eDiscovery requires the appropriate organization subscription and per-user licensing. If you aren’t sure which licenses support core eDiscovery, visit Get started with Core eDiscovery.


**Estimated Time**: 20-25 minutes

#### Task 1:  To access Core eDiscovery or be added as a member of a Core eDiscovery case, a user must be assigned the appropriate permissions. In this task, you as the global admin, will add specific users as members of the eDiscovery Manager role group.

1.	Open Microsoft Edge. In the address bar enter **admin.microsoft.com**.

      ![](../Images/module4/lab12/main-1.png)

1. Sign in with your admin credentials.
    1. In the Sign in window, Get the user credentials provided in the environment details page and paste the value in the username section and then select **Next**.
     
        ![](../Images/98.png)
     
        ![](../Images/module4/lab12/main-2.png)
    
    1. Enter the admin password which should be provided by your lab hosting provider. Select **Sign in**.
    
        ![](../Images/module4/lab12/main-3.png)
     
    1. When prompted to protect the account, Please select **Skip for now**.

        ![](../Images/module4/lab12/main-4.png)
     
    1. When prompted to stay signed- in, select **Yes**. This takes you to the Microsoft 365 admin center page.

1. From the left navigation pane of the Microsoft 365 admin center, select **Show all**.

    ![](../Images/module4/lab14/new1.png)

1. Under Admin centers, select **Security**.  A new browser page opens to the welcome page of the Microsoft 365 Defender portal.

    ![](../Images/module4/lab14/new2.png)

1. From the left navigation pane of the Microsoft 365 Defender portal, select **Permissions & roles**.  You may need to scroll down to see this option.

1. From the Permissions & roles page, under **Email & collaboration roles** select **Roles**.

    ![](../Images/module4/lab14/new3.png)

1. In the search bar, enter **eDiscovery** then select the search icon (magnifying glass).  Select **eDiscovery Manager**.

    ![](../Images/module4/lab15/1.png)
    
    ![](../Images/module4/lab15/1-1.png)

1. In the window that opens, notice how there are two sub-groups, eDiscovery Manager and eDiscovery Administrator.  Read the description of each.  For this lab lab, we will add members to the eDiscovery Administrator sub-group. Select **Edit**, next to eDiscovery Administrator.  As a general best practice, users should be assigned the least privilege required for their role.

    ![](../Images/module4/lab15/2.png)

1. To add members to this role group, make sure you are in the  **Choose eDiscovery Administrator** tab then select **Choose eDiscovery Administrator**.

    ![](../Images/module4/lab15/3.png)

1. Select **+ Add** from the top of the page.

    ![](../Images/module4/lab15/4.png)

1. From the list of names, select **ODL Administrator**, **Megan Bowen** and your account ie. name with **ODL_User uniqueID** then select **Add** at the bottom of the page, then select **Done** at the bottom of the page.

    ![](../Images/module4/lab15/5.png)
    
    ![](../Images/module4/lab15/5-1.png)

1. Verify the added members is correct then select **Save**.

    ![](../Images/module4/lab15/6.png)

1. From the bottom of the eDiscovery window, select **Close**.

    ![](../Images/module4/lab15/7.png)

1. Close all the tabs except the **admin.microsoft.com** and then sign out from the admin center page and sign-in back again to reflect the permissions added for users faster.

#### Task 2:  In this task you, as an eDiscovery Administrator (ODL admin is an eDiscovery administrator), will create a case to start using Core eDiscovery.

1. Open the Microsoft 365 admin center tab on your browser.

1. From the left navigation panel, under Admin Centers, select **Compliance**.

    ![](../Images/module4/lab15/8.png)

1. You are now in the Microsoft 365 compliance center. From the left navigation panel, select **Show all**.

1. From the left navigation panel, under Solutions, select **eDiscovery** then select **Core**.

1. From the top of the Core eDiscovery page, select **+ Create a case**.

    ![](../Images/module4/lab15/9.png)

1. In the New case window, enter a Case name, **SC900 Test Case** then select the **Save** at the bottom of the page.

    ![](../Images/module4/lab15/10.png)

1. The case should now appear on the list.

    ![](../Images/module4/lab15/11.png)

1. As the creator of the case and because you have eDiscovery Administrator privileges, you can begin to work with it.  

1. Keep this browser tab open, as you will use it in the subsequent task.

#### Task 3:  Now that you have created a Core eDiscovery case, you can begin to work with the case.  In this task, you will create an eDiscovery hold for the case for you just created.  Specifically, you will crate a hold for the the exchange mailbox belonging to Adele Vance.

1. Open the Core eDiscovery tab on your browser.

1. From the Core eDiscovery page, select the case you created in the previous tab, **SC900 Test Case**. 

1. From the Home page of the case, select the **Hold** tab then select **+Create**.

    ![](../Images/module4/lab15/12.png)

1. In the name field, enter **Test hold** then select Next.

    ![](../Images/module4/lab15/13.png)

1. In the Choose locations page, select toggle switch next to Exchange email to set the status to **On**, select **Choose users, groups, or teams**.

1. From the Choose locations page, select **Next**.  For expediency with the lab, no other locations will be included in this hold.

    ![](../Images/module4/lab15/14.png)

1. The Query conditions page enables you to create a hold, based on specific Keywords or Conditions that are satisfied, select **+Add condition** to view the available options.  Select **Next**. Without any conditions, the hold will preserve all content in the specified location.

    ![](../Images/module4/lab15/15.png)
    
    ![](../Images/module4/lab15/15-1.png)

1. Review your settings and select **Submit**, it may take a minute, then select **Done**.  The Test hold should appear on the list.  If you don't immediately see it, select **Refresh**

    ![](../Images/module4/lab15/16.png)

1. Keep this browser tab open, as you will use it in the subsequent task.

#### Task 4:  With a hold in place, you will create a search query.  Once your search is complete you will go export and download the results for future investigation.   Note:  Searches associated with a Core eDiscovery case are not listed on the Content search page in the Microsoft 365 compliance center. These searches are listed only on the Searches page of the associated Core eDiscovery case.

1. Open the SC900 Test case tab on your browser.

1. From the Holds page of the case, select **Searches**.

1. From the Search page, select **+ New Search**.

    ![](../Images/module4/lab15/17.png)

1. In the Name field, enter **Test Hold – Sales Search**, then select **Next** from the bottom of the page.

    ![](../Images/module4/lab15/18.png)

1. In the Choose locations page, select toggle switch next to Exchange email to set the status to **On**, select **Choose users, groups, or teams**. then select **Next**.  No other locations will be included in this search

    ![](../Images/module4/lab15/19.png)

1. The Query conditions page enables you to create a search, based on specific Keywords or Conditions that are satisfied, In the keyword field enter **Sales** select **Next**.

    ![](../Images/module4/lab15/20.png)

1. Review your settings and select **Submit**, it may take a minute, then select **Done**.  The search should appear on the list.  If you don't immediately see it, select **Refresh**

    ![](../Images/module4/lab15/21.png)

1. From the Searches window, select the search you just created, **Test Hold - Sales Search**.  A window that opens with the Summary tab selected.  Once the search is complete the status will indciate that the search is completed.  You will see a Search statistics tab (if you don't see the Search statistics tab, the search may still be running and may take a few minutes to complete).  Select the **Search statistics** tab and select the drop-down next to Search content.  You can also view more information for the Condition report and Top locations.  

    ![](../Images/module4/lab15/22.png)

1. From the bottom of the page, select **Actions**.  Note the available options. By selecting **Export results**, search results can be downloaded. 

      ![](../Images/module4/lab15/24.png)
    
      ![](../Images/module4/lab15/25.png)
      
    1. From the Export results window, leave the defaults and select **Export** from the bottom of the page. You will automatically be returned to the "Test Hold - Sales search" window. Select **close** on the bottom of the page.

         ![](../Images/module4/lab15/26.png)  
    
    1. From the SC900-Test case page, select **Exports** from the top of the page.
    1. Select **Test Hold - Sales Search_Export**

         ![](../Images/module4/lab15/27.png)
    1. In the window that opens, "Test Hold - Sales Search_Export", you will see an Export key, select **Copy to clipboard**.

         ![](../Images/module4/lab15/28.png)
    1. From the top of the window, select **Download results.***(**Note**: You must use Microsoft Edge or Internet Explorer to download). A new browser page opens and a pop-up window displays asking if you want to open this file, select **Open**.

         ![](../Images/module4/lab15/29.png)
         
         ![](../Images/module4/lab15/30.png)
    1. If this is the first time you do a download of a content search, you will be prompted to install the Microsoft Office 365 eDiscovery Export tool.  Select **Install**.

         ![](../Images/module4/lab15/31.png)
         
    1. Once the install is completed, the eDiscovery export tool window opens.  In the first field, paste the export key that you copied to your clipboard, paste it in now (Control V on your keyboard or right-click on your mouse and select paste).  
    1. In the second field, select the location where you want to store the export file, then select **Start**.  Once the download process is completed, select **Close** and close this browser tab.

         ![](../Images/module4/lab15/32.png)
    1. You are back on the "Test Hold - Sales Search_Export" window.  Select **Close**.
    1. Check the location of your download to verify the download was successfully completed. 

#### Review

In this lab you went through the steps required to get started with core eDiscovery, including setting up the role permissions for eDiscovery and creating an eDiscovery case.  With the case, created you went through the Core eDiscovery workflow, by creating an eDiscovery hold, creating a search query and then you read on the process of exporting the results of the search to use further investigation.
