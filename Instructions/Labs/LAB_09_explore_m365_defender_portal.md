# Lab 09: Explore the Microsoft Defender portal

## Lab Overview

In this lab, you will explore the Microsoft 365 Defender portal by walking through the content displayed on the landing page. You will also explore the options on the navigation panel, which provide quick access to functionality that is part of Microsoft’s Extended Detection and Response (XDR) solution: Microsoft Defender for Endpoints, and Microsoft Defender for Office 365 (email and collaboration).  Lastly, you will also explore how Microsoft Secure Score can help an organization improve its security posture.

## Lab Objectives

In this lab, you will complete the following tasks:

+ Task 1: Explore the Microsoft 365 Defender landing page
+ Task 2: Explore Microsoft Secure Score

## Estimated timing: 30 Minutes

## Architecture diagram

![](../Images/sc900lab9.png)

## Task 1:  Explore the Microsoft 365 Defender landing page

In this task, you will explore the Microsoft 365 Defender landing page, review and customize dashboard cards, and become familiar with navigation options across Microsoft’s XDR security features.

1. Open Microsoft Edge. In the address bar, enter **admin.microsoft.com**

1. In the Sign-in window, enter the following **Email/Username** and click on **Next**.

    * **Email/Username:** <inject key="AzureAdUserEmail"></inject>

1. Now enter the **Password** and click on **Sign in**.
   
   * **Password:** <inject key="AzureAdUserPassword"></inject>
  
1. When prompted to **Stay signed-in?**, select **Yes**. This takes you to the Microsoft 365 admin center page.

1. From the left navigation pane of the Microsoft 365 admin center, select **Show all (1)**. 

     ![Picture 1](../Images/lab09-t1p1.png)

1. Then under **Admin centers** select **Security (2)**. 

     ![Picture 1](../Images/lab09-t1p1(1).png)

1. If this is your first visit to the Microsoft Defender portal, a **Meet your improved security center** pop-up may appear. You can either **Take the quick tour** or click **X** to close it.

     ![Picture 1](../Images/lab08-57.png)

1. The welcome page of the Microsoft 365 Defender portal shows many of the common cards that security teams need. The composition of cards and data is dependent on the user role. Scroll through the page to view the default set of cards for your role as a global admin.

     ![Picture 1](../Images/lab09-t1p3.png)

1. The cards displayed can be customized to your preference.  Select **+ Add cards (1)**. A Window opens, indicating that you already have all the cards on your home page.  Close the window by selecting the **X (2)** on top-right corner of the window.
   
     ![Picture 1](../Images/lab09-t1p4.png)
   
     ![Picture 1](../Images/lab09-t1p5.png)
   
1. Selecting the **ellipsis (...) (1)** on the top-right of any card will provide the option to **Remove (2)**.  

     ![Picture 1](../Images/lab09-t1p6.png)

1. You can also move the cards around. Hover your mouse cursor over the title bar of any card,  and you will get a cross-shaped cursor. Select the card and move it to your desired location.
   
     ![Picture 1](../Images/lab09-t1p7.png)

1. Selecting the title of a card will take you to additional information for that topic. You'll explore this in the next task.

1. The left navigation panel provides links/access to information that is part of Microsoft’s Extended Detection and Response (XDR solution), which includes incidents & alerts, hunting, action center, threat analytics, secure score, and more.  It also includes quick access to Microsoft Defender for Endpoint (the links listed under Endpoints, Defender for Office 365 (the links listed under Email and Collaboration), and Microsoft Defender for Cloud Apps (the links under Cloud apps).  Explore these options by selecting some of the links.   To return to the home page of the Microsoft 365 Defender portal, select **Home** on the left navigation panel.

     ![Picture 1](../Images/lab09-t1p8.png)

1. Keep the browser window open.

## Task 2: Explore Microsoft Secure Score

In this task, you will explore how Microsoft Secure Score can help an organization improve its security posture.

1. From the Welcome page of the Microsoft Defender portal, select **Microsoft Secure Score (1)**, from the title bar of the card (the text will turn blue).  Alternatively, you can select **Secure score** from the left navigation panel.
 
     ![Picture 1](../Images/lab09-t2p1.png)

     ![Picture 1](../Images/lab09-t2p2.png)

1. The Microsoft Secure Score page opens to the Overview tab. Microsoft Secure Score is a measurement of an organization's security posture. Your organization’s secure score is shown as a percentage, along with the number of points you've achieved out of the total possible points and broken down by category. Select **Include (1)**, next to where it says Your secure score. A small window opens that allows you to include the achievable score, Planned score, and Current license score in the breakdown of your organization's secure score **(2)**. Select **Include** again to close the window.

     ![Picture 1](../Images/lab09-t2p3.png)

1. The **Overview** page also includes **Top recommended actions**, **Comparison**, **History**, and additional resources.

     ![Picture 1](../Images/lab09-t2p4.png)

1. Select **Recommended actions (1)** from the top of the page. Notice the information available in the table. Select the **first items (2)** from the list and review the available information in the window that opens.

     ![Picture 1](../Images/lab09-t2p5.png)

1. Select **Edit status & action plan**. In the window that opens, note the status options available. Select the **X** at the top right corner to close this window.

   > **Note :** Skip this step if the **Edit status & action plan** option is not clickable.

     ![Picture 1](../Images/L9-T2-S5a.png)

     ![Picture 1](../Images/L9-T2-S5b.png)

1. Now, select the **Implementation (1)** tab to view the information related to implementation. Select the **X (2)** at the top right corner to close this window.

     ![Picture 1](../Images/lab09-t2p6.png)

1. Select the **History (1)** tab from the top of the page. Select an **item (2)** from the history table. 

     ![Picture 1](../Images/lab09-t2p7.png)

     >**Note:** If no data is visible, skip ahead to step 9 and continue.

1. When a detailed page for the selected item opens, explore the options available. To exit the details page and return to the History page, select the **X** on the top-right corner of the page.

     ![Picture 1](../Images/L9-T2-S8.png)

1. From the top of the page, select **Metrics & trends (1)**.  Note the available information. From the top-right corner of the page, select the **calendar icon (2)**. You can narrow down the view to a custom date range.

     ![Picture 1](../Images/lab09-t2p8.png)

1. Select the **filter** icon present beside the Calendar icon to filter the view by Identity, Apps, Devices, and Data. To return to the Microsoft 365 Defender home page, select the **X** in the top-right corner. Choose **Home** from the left navigation panel.

    ![Picture 1](../Images/L9-T2-S10.png)
    
    
    >**Note:** If you can't see details on the **History** and **Metrics & treads** tabs, this is because after making configuration changes. It will take about 24 hours to update.
    
    >**Note:** For more details visit: https://learn.microsoft.com/en-us/microsoft-365/security/defender/microsoft-secure-score?view=o365-worldwide
    
1. Close the browser page.

## Review

In this lab, you completed:

* Explored the Microsoft 365 Defender landing page
* Explored Microsoft Secure Score

### You have successfully completed the lab
