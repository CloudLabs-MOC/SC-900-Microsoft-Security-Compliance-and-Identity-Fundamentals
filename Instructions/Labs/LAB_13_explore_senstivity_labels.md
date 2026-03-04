# Lab 13: Explore sensitivity labels in Microsoft Purview

## Lab Overview
In this lab, you will explore the capabilities of sensitivity labels.  You will go through the settings for existing sensitivity labels that have been created and the corresponding policy to publish the label.   Then you will see how to apply a label and the impact of that label, from the perspective of a user.

## Lab Objectives

In this lab, you will complete the following tasks:

+ Task 1: Explore the capabilities of sensitivity labels
+ Task 2: How to apply a label
+ Task 3: Impact of that label

## Estimated timing: 60 Minutes

## Architecture diagram

![](../Images/sc900lab13.png)

## Task 1: Explore the capabilities of sensitivity labels
In this task, you will gain an understanding of what sensitivity labels can do by going through the settings for an existing sensitivity label that has been created and the corresponding policy to publish the label.

1. Open Microsoft Edge. In the address bar, enter https://admin.microsoft.com. 
   
1. In the Sign-in window, enter the following **Email/Username** and click on **Next**.

    * **Email/Username:** <inject key="AzureAdUserEmail"></inject>

1. Now enter the password and click on **Sign in**.
   
   * **Password:** <inject key="AzureAdUserPassword"></inject>
  
1. When prompted to stay signed-in, select **Yes**. This takes you to the Microsoft 365 admin center page.

1. From the left navigation pane of the Microsoft 365 admin center, select **Show all**.

    ![](../Images/lab13-t1p1.png)

1. Under **Admin centers**, select **Microsoft Purview**.

    ![](../Images/lab13-t1p2.png)

1. A new browser page will open. Since you are already signed in, your email will be listed. You can select your email address to log in to Microsoft Purview.
    
    ![](../Images/L13-T1-S7.png)

1. Upon logging in to the portal, a **Welcome to the new Microsoft Purview portal!** pop-up window will appear, select **Get started**.

    ![](../Images/lab13-t1p3.png)

1. You are now on the homepage of the New Microsoft Purview portal.

    ![](../Images/lab13-t1p4.png)

1. In the left navigation panel of Microsoft Purview, go to **Solutions (1)**, select **Information Protection (2)**, and then choose **Sensitivity labels (3)**. On the Sensitivity labels page, click **Turn on now (4)** inside the yellow information box to enable processing of encrypted sensitivity labels in Office online files stored in OneDrive and SharePoint.

   > **Note**: There can be a delay for the setting to propagate through the system. Refresh the Page once.

    ![](../Images/lab13-t1p7.png)

    ![](../Images/lab13-t1p8.png)    

1. Now select **+ Create a label**.

    ![](../Images/lab13-t1p9.png)

1. On the new label configuration page, enter the details provided below and click **Next (4)**.

    | Setting | Values |
    | -- | -- |
    | **Name** | **Confidential-Finance (1)** |
    | **Display name** | **Confidential-Finance (2)** |
    | **Description for users** | **Confidential-Finance Demo (3)** | 

    ![](../Images/lab13-t1p10.png)

1. On the **Define the scope for this label** page, read the description but **do not** change any settings. Select **Next** at the bottom of the page.

      ![](../Images/lab13-t1p11.png)

1. On the **Choose protection settings for labelled items** page, check the box **Apply content marking (1)** options and then click **Next (2)**.

    ![](../Images/lab13-t1p12(1).png)

    >**Note:** The **Control access** option is not selected in this lab because it requires **Rights Management (Azure RMS / Microsoft Purview Information Protection)** to be enabled and fully configured in the organisation. Since RM services may not be activated in the newly created lab tenant, this option is intentionally skipped to avoid configuration or policy enforcement issues.

1. On the **content markings** page, take note of the information box at the top of the page. **Turn on (1)** the Content Making and select **Add a watermark (2)**, **Add a header (3)**, & **Add a footer (4)**. Click on **Customize text (5),(6),(7)** on each and provide the text **customize watermark test** and click on **Save**.  Content markings will be applied to the documents, but only headers and footers will be applied to email messages. In other words, watermarks are not applied to emails. The content marking associated with this label is a watermark. Select **Next (8)** at the bottom of the page.

    ![](../Images/lab13-t1p15(1).png)

    ![](../Images/lab13-t1p15.png)

1. You are now in the **Auto-labelling for files and emails** window. Turn on the **Auto-labeling for files and emails (1)** and read the description of auto-labeling on the top of the page and the information box below it. Select **Next (2)** at the bottom of the page.

    ![](../Images/lab13-t1p16.png)

1. This next window **Defines protection settings for groups and sites** that have this label applied. This is not enabled, select **Next** at the bottom of the page.

    ![](../Images/lab13-t1p17.png)
      
1.  Review the settings and click on **Create label**.

      ![](../Images/lab13-t1p18.png)
      
1. Click on **Done** on next window.   

      ![](../Images/lab13-t1p19.png)

1. A new window of **Publish label** will open. Click on **Create new label policy**.

      ![](../Images/lab13-t1p20.png)

1. A new window of Create policy will open. Select **Choose sensitivity labels to publish (1)**. A window opens that provides information about the policy. This policy serves to publish the IT-Department-Demo. Select **Confidential-Finance (2)** from the label and select **Add (3)** at the bottom of the page. And then click on **Next (4)**.

     ![](../Images/lab13-t1p21.png)
     
1. Under the **Sensitivity labels to publish**, do not change any settings.  Select **Next** on the bottom of the page.

     ![](../Images/sc-900-jap23.png)
     
1. Click on **Next** on Assign Admin Units. 

     ![](../Images/sc-900-jap24.png)   

1. Read the description under **Publish to users and groups**.  Notice that this label is available to all users. Do not change any settings.  Select **Next** at the bottom of the page.

    ![](../Images/sc-900-jap25.png)

1. Under the **policy settings**, do not change any settings.  Select **Next** at the bottom of the page.

    ![](../Images/sc-900-jap26.png)

1. Under the **Apply a default label to documents**, do not change any settings.  Select **Next** at the bottom of the page.

    ![](../Images/sc-89.png)

1. Under the **Apply a default label to emails**, do not change any settings.  Select **Next** at the bottom of the page.

    ![](../Images/sc-90.png)
    
1. Under the **Apply a default label to meetings and calendar events**, do not change any settings.  Select **Next** at the bottom of the page.    

    ![](../Images/sc-91.png)
    
1. Under the **Apply a default label to Fabric and Power BI content**, do not change any settings.  Select **Next** at the bottom of the page.

    ![](../Images/sc-92.png)
    
1. The last configuration option is to name your policy. Enter the policy name as **Confidential-Finance Policy (1)**.  Select **Next (2)** at the bottom of the page to exit the policy configuration and return to the Information protection page.

    ![](../Images/sc-93.png)
    
1. Review the settings and click on **Submit** and then select **Done**.

    ![](../Images/sc-900-jap32.png)
    
    ![](../Images/sc-94.png)    
    
    >**Note**- The label created cannot be deleted; it can only be edited. 

1. From the left navigation panel, select Home to return to the Microsoft Purview.

    ![](../Images/sc-900-dec24-lab13-12.png)   

1. Keep this page open; you will use it in the next task.

1. It can take up to 24 hours to publish the labels to the selected users' apps.

1. From the left navigation panel, under **Information protection (1)**, select **Auto-labeling policies (2)**. Then click on **+ Create auto-label policy (3)**.

      ![](../Images/lab13-t1p22.png)

1. In the **What type of auto labeling policy do you want to create?** pop-up, select **Automatically apply labels only**.

      ![](../Images/L13T1S36.png)

1. Note the available options. Select **Medical and health (1)** then select one of the available templates **(2)**. Select **Next (3)**.  

      ![](../Images/sc-96.png)

1. You can name your auto-label policy or use the default name **(1)**. Select **Next (2)**.

      ![](../Images/sc-97.png)

1. Next, you choose a label to auto-apply. Select **+ Choose a label (1)**. Select **Confidential-Finance (2)** label from the list, select **Add (3)**, and then click on **Next (4)**.

    ![](../Images/lab13-t1p23.png)

1. You can assign the admin units to which this policy applies. Leave the default set to full directory and select **Next**.      

      ![](../Images/lab13-t1p24.png)   

1. Note the available **locations where you want to apply the label**. For this exercise, select the box next to **Exchange email (1)**, then select **Next (2)**.  

      ![](../Images/lab13-t1p25.png)   

1. You can **Set up common or advanced rules** that define what the content the label is applied to. Leave the default set to **Common rules** and select **Next**.

      ![](../Images/lab13-t1p26.png)   

1. You can **Define rules for content in all locations**. Leave all the default settings and select **Next**.     

      ![](../Images/lab13-t1p27.png)     

1. **Additional settings can be configured for email**. Leave the defaults and select **Next**.      

      ![](../Images/lab13-t1p28.png)   

1. You can decide to test the policy now or later. Select **Leave policy turned off (1)** then select **Next (2)**.

      ![](../Images/lab13-t1p29.png)   

1. Review the settings. For the purpose of this exercise, you can cancel out without creating the policy. Select **Cancel**.

    ![](../Images/lab13-t1p30(1).png) 

1. On the **Auto-labeling policies** pop-up window, click on **Confirm**.

    ![](../Images/lab13-t1p31.png) 

1. From the left navigation panel, select **Home** to return to the Microsoft Purview portal.            

## Task 2: How to apply a label

In this task, you will go through the process of applying a label from the perspective of the user (in this case, the user is the admin) and view the content marking that is generated by the label.

1. From the Microsoft Purview home page, select the **App launcher (1)** icon, and click on **More apps (2)**.

   ![](../Images/lab13-t2p1.png) 

1. A new tab will open in the browser, taking you to the M365 portal.

1. If the **Welcome to Apps** pop-up appears, click the **X** icon to close it.

    ![](../Images/lab13-t2p2.png)

    >**Note:** Click the **X** icon to close the **All your work in one place, now easier with AI** window.

    ![](../Images/lab13-t2p2(1).png)

1. From the left navigation pane, select **Apps (1)** and then select **Word (2)**.

    ![](../Images/lab13-t2p3.png)

1. A new browser tab will open to the Word homepage. From there, select **+ Create blank document**.

    ![](../Images/lab13-t2p4.png)

1. If a **Your privacy option** pop-up window appears, click on **Close**.

    ![](../Images/lab13-t2p5.png)

1. Under Create new, select **Blank document**, then enter some text on the page. On the top of the page, next to the **Word** icon, select where it says **Document** and rename the file to **Test-label**, then press Enter on your keyboard.

   ![](../Images/L13-T2-S2.png) 

1. On the far right of the top menu bar (also referred to as the ribbon) is a **down arrow (1)**, select it, then select **Classic Ribbon (2)**. This will make it easier to identify the sensitivity icon.

    ![](../Images/lab13-t2p6.png)

1. From the top menu bar, select **Sensitivity (1)**. From the drop-down select **Confidential-Finance (2)**.

    ![](../Images/lab13-t2p7.png)  

    >**Note:** If the option is not available, it will take some time to reflect, and if selecting the label shows error label cannot be added to Word on the web, please try refreshing the page once or sign out and sign in again.   

1. From the top menu bar, select **View (1)**, then select **Reading View (2)**.

    ![](../Images/lab13-t2p8.png)            

1. Notice how the document includes the watermark. 

    ![](../Images/L13-T2-S5.png) 

1. Close the Microsoft Word tabs that are open on your browser to exit from Word.

## Review

In this lab, you completed:

* Explored the capabilities of sensitivity labels
* Learned how to apply a label
* Reviewed the impact of that label

### You have successfully completed the lab

