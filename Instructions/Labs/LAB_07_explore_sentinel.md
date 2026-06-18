
# Lab 07 : Explore Microsoft Sentinel 

## Lab Overview

In this lab you will walk through the process of creating an  Microsoft Sentinel instance.  You will also set up the permissions to ensure access to the resources that will get deployed to support  Microsoft Sentinel.  Once this basic setup is done you will walk through the steps for connecting Microsoft Sentinel to your data sources, set up a workbook, and do a brief walk-through of some of key capabilities available in Microsoft Sentinel. 

## Lab Objectives

In this lab, you will complete the following tasks:

+ **Task 1:** Create a Microsoft Sentinel instance
+ **Task 2:** Built-in Microsoft Sentinel roles
+ **Task 3:** Data connector to your instance of Microsoft Sentinel
+ **Task 4:** Explore on capabilities available in Sentinel 

## Estimated timing: 90 Minutes

## Architecture diagram

![](../Images/sc900lab7-(1).png)
  
## Task 1:  Create a Microsoft Sentinel instance

To create an instance of Microsoft Sentinel, you first have to create a Log Analytics workspace, used to store data from Microsoft Sentinel.  Once you have a Log Analytics workspace you can create an instance Microsoft Sentinel and add the log analytics workspace to it.  In this task you run through each of these steps.

1. In the Azure portal, in the **Search resources, services, and docs** search for **Log Analytics workspaces (1)** then select **Log Analytics workspaces (2)** from the search results.

   ![Picture 1](../Images/lab7-l1.png)

1. From the Log Analytics Workspace page, select **+ Create**.

   ![Picture 1](../Images/lab7-l2.png)

1. From the basics tab of the Create Log Analytics workspace, enter the following details and then click on **Review + Create (5)**.

    | Setting        | Action                                                                            |
    | ---------------| --------------------------------------------------------------------------------|
    | Subscription   |  **Select the given subscription (1)**  |
    | Resource group | Select **SC900-ResourceGroup (2)** |
    | Name | **SC900-LogAnalytics-workspace-<inject key="DeploymentID" enableCopy="false"/> (3)** |
    | Region | leave this default **(4)** |
   
    ![Picture 1](../Images/sc-lab7-l3.png)

1. Once the Validation is passed, then select **Create**.

   ![Picture 1](../Images/sc-lab7-l18.png)

1. It may take a minute or two for the new workspace to be created. Once it's created, select **Go to resource** to view information about the workspace.

    ![Picture 1](../Images/lab7-l4.png)

1. In the Azure portal, in the **Search resources, services, and docs** search for **Microsoft Sentinel (1)** then select **Microsoft Sentinel (2)** from the search results.

   ![Picture 1](../Images/lab7-02-2.png)

1. From the Microsoft Sentinel page, select **+ Create**.

   ![Picture 1](../Images/lab7-l5.png)

1. On **Add Microsoft Sentinel to a workspace**, If you don’t see the new workspace listed, select **Refresh**. Then select newly created workspace **SC900-LogAnalytics-workspace (1)** and then click on **Add (2)**.

   ![Picture 1](../Images/lab7-l6.png)

1. Once the new workspace is added, the **Microsoft Sentinel | Guides** page will display, including that the Microsoft Sentinel free trial is activated. Select **OK**  Note the three steps listed on the Get started page.

   ![Picture 1](../Images/lab7-l7.png)

1. Keep this page open, as you will use it in the next task.
   
> **Congratulations** on completing the task! Now, it's time to validate it. Here are the steps:
> - Hit the Validate button for the corresponding task. If you receive a success message, you can proceed to the next task.
> - If not, carefully read the error message and retry the step, following the instructions in the lab guide.
> - If you need any assistance, please contact us at cloudlabs-support@spektrasystems.com. We are available 24/7 to help you out.

<validation step="e6ffbb4b-3ecb-42af-9dcd-0c1044de2a66" />

## Task 2: Built-in Microsoft Sentinel roles

With the Microsoft Sentinel instance created, it is important that users that will have responsibility to support Microsoft Sentinel have the necessary permissions.  This is done by assigning the designated user the required role permissions. In this task, you'll view the available, built-in Microsoft Sentinel roles.

1. In the **Search resources, services, and docs** search for **Resource groups (1)** then select **Resource groups (2)** from the search results.

   ![Picture 1](../Images/lab7-l8.png)

1. From the Resource groups page, select the resource group  with Microsoft Sentinel, **SC900-ResourceGroup**.

   ![Picture 1](../Images/lab7-l9.png)
   
   >**Note**: Working at the resource group level will ensure that any role that is selected will apply to all the resources that are part of the Microsoft Sentinel instance that was created in the previous task.
  
   >**Note**:  For the Azure subscription provided to you in this lab environment, a role has been defined that will give you access to manage all necessary resources as shown in the description. It is important, however, to understand the available Sentinel specific roles. Note the current role is Owner.
  
   >**NOTE:**  As a best practice you should assign the least privilege required for the role.  As a reference, review permissions in Azure Sentinel: https://docs.microsoft.com/en-us/azure/sentinel/roles
   
1. Select the **Access Control (IAM) (1)**, select **View my access (2)** to confirm the **Owner (3)** role has been added, then close the window by select the **X (4)** on the top-right corner of the window.

   ![Picture 1](../Images/lab7-02-1.png)

1. From the Access control page, select the **Roles (1)** tab on the top of the page.

   - In the search box, enter **Microsoft Sentinel (2)** to view the built-in roles associated with Microsoft Sentinel.
  
   - From any of the roles listed **(3)**, select **View (4)** to view the details of that role. As a best practice you should assign the least privilege required for 
       the role.

   - Close the window by selecting the **X (5)** on the top-right corner of the window.
  
     ![Picture 1](../Images/lab7-l12.png)

1. From the top left corner of the window, just below the blue bar where it says Microsoft Azure, select **Home** to return to the Azure services home page.

   ![Picture 1](../Images/lab7-l13.png)

1. Keep the Azure tab open on your browser.

> - **Congratulations** on completing the task! Now, it's time to validate it. Here are the steps:
> - Hit the Validate button for the corresponding task. If you receive a success message, you can proceed to the next task.
> - If not, carefully read the error message and retry the step, following the instructions in the lab guide.
> - If you need any assistance, please contact us at Cloudlabs-support@spektrasystems.com.com. We are available 24/7 to help you out.

<validation step="6ef79789-58a4-4dc4-a65e-8b5aacef02c1" />

## Task 3: Data connector to your instance of Microsoft Sentinel

In this task you will walk through the steps involved in setting up a data connector to your instance of Microsoft Sentinel and selecting a built-in workbook templates to allow you to quickly gain insights across your data as soon as you connect a data source. 
   
   >**Note:** Azure lab subscriptions may experience greater than normal delays in connecting to a data source and/or visualizing data.

1. In the **Search resources, services, and docs** search for **Microsoft Sentinel (1)** then select **Microsoft Sentinel (2)** from the search results.

   ![Picture 1](../Images/lab7-02-2.png)

1. From the Microsoft Sentinel page, select the workspace you created with the instance of Microsoft Sentinel, **SC900-LogAnalytics-workspace-<inject key="DeploymentID" enableCopy="false"/>**.

   ![Picture 1](../Images/lab7-02-3.png)

1.  In Microsoft Sentinel page, in the left navigation pane, expand **Content management (2)**, and select **Content hub (3)**. In the search bar, type **Microsoft Defender for Cloud**, then select the checkbox **Microsoft Defender for Cloud (4)** from the results and click **Install (5)**.

    ![Picture 1](../Images/lab7-02-4.png)

    >**Note:** You may need to select the "**>>**" at the far-right side of the window to see the information panel

    >**Note:** If you see the message **This page has been moved to the Defender portal for the optimal, unified SecOps experience**, refresh the page and continue this lab in the Microsoft Azure portal, as the lab environment is configured for the Azure portal and the Microsoft Defender portal experience may take longer to load for this lab.
   
1. Once again, select **Microsoft Defender for Cloud** from the list. From the window on the right, select **Manage**.

   ![Picture 1](../Images/lab7-02-5.png)

1. On the **Microsoft Sentinel | Data connector** page , select **Subscription-based Microsoft Defender for Cloud (Legacy) (1)**. On the **Subscription-based Microsoft Defender for Cloud (Legacy)** window opens. Review the description then Select **Open connector page (2)**.

    ![Picture 1](../Images/lab7-02-6.png)

    >**Note**: You may need to select the "**>>**" at the far-right side of the window to see the information panel

1. From the **Subscription-based Microsoft Defender for Cloud (Legacy)** connector page, review the Description on the left side of the window. 

   ![Picture 1](../Images/lab7-02-7.png)

1. The instructions tab in the main window, provides the prerequisites. Review the instructions and configuration information.

1. From the configuration section, select listed subscription, select your **azure subscription (1)** so that a checkmark appears in a blue box and then select **Connect (2)** (the connect option is shown above the search box).

   ![Picture 1](../Images/lab7-02-8.png)

   >**Note:** If a Connect window appears, select **OK**.

1. In the status column, next to the subscription you should see that status update to Connected. The connector is now enabled, although it may take some time for the connector to show up in the data connectors page.

   ![Picture 1](../Images/lab7-02-9.png)

1. Now view information about the analytics rule. From the top of the page (in the breadcrumb) select **Microsoft Defender for Cloud**. 

    ![Picture 1](../Images/lab7-02-10.png)

1. Select the **Detect CoreBackUp Deletion Activity from related security alerts (1)**. A window that opens on the right, that provides information about the rule and what it does. Select **Create rule (2)**.

   ![Picture 1](../Images/lab7-02-11.png)

1. Although the details of the rule logic are beyond the scope of the fundamentals, go through each tab in the rule creation to view the type of information that can be configured.

1. When you reach the **Review + create (1)** tab, select **Save (2)**.

   ![Picture 1](../Images/lab7-02-12.png)

1. Return to the Sentinel page by selecting Microsoft Sentinel | Content hub from the bread-crumb at the top of the page

   >**Note:** If you see the message **This page has been moved to the Defender portal for the optimal, unified SecOps experience**, refresh the page and continue this lab in the Microsoft Azure portal, as the lab environment is configured for the Azure portal and the Microsoft Defender portal experience may take longer to load for this lab.

1. Keep this page open, as you'll use it in the next task.

## Task 4: Explore on capabilities available in Sentinel

In this task, you'll walk through some of the options available in Sentinel.

1. From the left navigation panel, expand **Threat management (1)** and explore the options listed in threat management.

1. Select **Incidents**, Although no incidents are found, review the **What is it?** section.    

    ![Picture 1](../Images/lab7-02-13.png)

    >**Note:** If you see the message **This page has been moved to the Defender portal for the optimal, unified SecOps experience**, Please refresh the page and continue this lab in the Microsoft Azure portal.

1. Select **Hunting (1)**, then review the information provided in the **Hunts (Preview) (2)** tab.    

    ![Picture 1](../Images/lab7-02-14.png)

    >**Note:** If you see the message **This page has been moved to the Defender portal for the optimal, unified SecOps experience**, Please refresh the page and continue this lab in the Microsoft Azure portal.

1. Select **Notebooks**, and review the **What is it?** section.

     ![Picture 1](../Images/lab7-02-15.png)

     >**Note:** If you see the message **This page has been moved to the Defender portal for the optimal, unified SecOps experience**, Please refresh the page and continue this lab in the Microsoft Azure portal.

1. Select **Threat intelligence** and review the information on the page.    

    ![Picture 1](../Images/lab7-02-16.png)

    >**Note:** If you see the message **This page has been moved to the Defender portal for the optimal, unified SecOps experience**, Please refresh the page and continue this lab in the Microsoft Azure portal.

1. From the left navigation panel, select **MITRE ATT&CK (Preview) (1)**. MITRE ATT&CK is a publicly accessible knowledge base of tactics and techniques that are commonly used by attackers. With Microsoft Sentinel you can view the detections already active in your workspace, and those available for you to configure, to understand your organization's security coverage, based on the tactics and techniques from the MITRE ATT&CK® framework. *Select any cell from the matrix* **(2)** and note the information available on the right side of the screen **(3)**. 

    ![Picture 1](../Images/lab7-02-17.png)
    
    >**Note:** You may need to select the "**>>**" at the far-right side of the window to see the information panel.

    >**Note:** If you see the message **This page has been moved to the Defender portal for the optimal, unified SecOps experience**, Please refresh the page and continue this lab in the Microsoft Azure portal.

1. From the left navigation panel, expand **Content Management (1)**, then select **Community (2)**. The community page includes *Cybersecurity insights and updates from Microsoft Research, a link to a list of Microsoft Sentinel Blogs, a link to Microsoft Sentinel Forums, links the latest editions to the Microsoft Sentinel Hub, and more*. Explore this as well.

    ![Picture 1](../Images/lab7-02-18.png) 

    >**Note:** If you see the message **This page has been moved to the Defender portal for the optimal, unified SecOps experience**, Please refresh the page and continue this lab in the Microsoft Azure portal.

1. From the left navigation panel, select **Automation (2)** under **Configuration (1)**.  Here you can create simple automation rules, integrate with existing playbooks, or create new playbooks.  Select **+ Create (3)** dropdown, and then select **Automation rule (4)**. Note the window that opens on the right side of the screen and the options available to create conditions and actions.  Select **Cancel** from the bottom of the screen.
 
    ![Picture 1](../Images/lab7-02-19.png) 

    ![Picture 1](../Images/lab7-02-20.png) 

    >**Note:** If you see the message **This page has been moved to the Defender portal for the optimal, unified SecOps experience**, Please refresh the page and continue this lab in the Microsoft Azure portal.
    
## Review
In this lab, you have completed:
- Created a Microsoft Sentinel instance
- Built-in Microsoft Sentinel roles
- Data connector to your instance of Microsoft Sentinel
- Explored on capabilities available in Sentinel

## You have successfully completed the lab

