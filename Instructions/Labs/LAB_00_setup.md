# Lab: Setup

### Lab scenario

In this lab, you will redeem your Azure pass using the same credentials as your Microsoft 365 tenant.  This will make for a seamless experience when moving between Microsoft 365 and Azure. As part of the setup, you will also enable the audit log capability, in your Microsoft 365 tenant, as it can take some time take effect. Microsoft 365 uses audit logs for user insights and activities identified in policies and analytics insights.

**Estimated Time**: 5-10 minutes

#### Setup part 1 - Redeem Azure Pass
In this setup task, you will redeem your Azure pass using the same credentials as your Microsoft 365 tenant.  This will make for a more seamless experience when moving between Microsoft 365 and Azure.

1. If you have any open browser windows, it is recommended you close all browsers.

1. Right click on the Microsoft Edge icon and and select **New InPrivate window** to open a new In-Private Browser session. Other 

1. In the address bar enter **www.microsoftazurepass.com**.  

1. Select the **start** button to get started.

    1. In the Sign in window, enter the email  **admin@WWLxZZZZZZ.onmicrosoft.com** (where ZZZZZZ is your unique tenant ID provided by your lab hosting provider) then select **Next**.
    1. Enter the admin password which should be provided by your lab hosting provider. Select **Sign in**.  If prompted to stay signed in, select **Yes**.
    1. Select **Confirm Microsoft Account** if the correct email address is listed.
    1. Enter your promo code in the Promo code box and click **Claim Promo Code**.  
    1. In the "Your profile" page, leave all the default information, select **I agree to the subscription agreement, offer details, and privacy statement.** then select **Sign up**.
    1. If a survey window open, you choose to close it by selecting the **X** or respond as appropriate and select **Submit**.

1. It may take a few minutes to activate your account.  Once activated you are directed to the Azure portal Home page. A Welcome to Microsoft Azure window opens, select **Maybe later** . You may get a pop-up window "Optimize your cloud workloads with personalized recommendations", select **X** on the top right corner of the window.

1. Leave the browser tab to the Azure portal home page open, you will come back to it in the next demo.

#### Setup part 2 - Enable Microsoft 365 audit log
In this setup task, you will enable the Audit log capability in Microsoft 365.  Although documentation indicates that audit log is turned on by default, most lab tenants do not have this feature enabled and it can take several hours for this to take effect.  It is beneficial to enable this feature, as Microsoft 365 uses audit logs for user insights and activities identified in policies and analytics insights.

1. Open Microsoft Edge. In the address bar enter **admin.microsoft.com**.

1. Sign in with your admin credentials.
    1. In the Sign in window enter **admin@WWLxZZZZZZ.onmicrosoft.com** (where ZZZZZZ is your unique tenant ID provided by your lab hosting provider) then select **Next**.
    1. Enter the admin password which should be provided by your lab hosting provider. Select **Sign in**.
    1. When prompted to stay signed- in, select **Yes**. This takes you to the Microsoft 365 admin center page.

1. From the left navigation pane of the Microsoft 365 admin center, select **Show all**.

1. Under Admin centers, select **Compliance**.  A new browser page opens to the welcome page of the Microsoft 365 compliance center.  

1. From the left navigation panel of the Microsoft 365 compliance center, select **Show all**.

1. In the left navigation panel, under solutions, select **Audit**.  Note: the audit functionality is also accessible through the Microsoft 365 Defender home page (previously referred to as the Microsoft 365 security center).

1. Verify that the **Search** tab is selected (underlined).

1. Once you land on the Audit page, wait 2-3 minutes.  If Auditing is NOT enabled, you will see a blue bar on the top of the page that says start recording user and admin activity.  Select **Start recording user and admin activity**.  Once auditing is enabled, the blue bar disappears.  If the blue bar is not present then auditing is already enabled, and no further action is required.  Another way to check if auditing is enabled is through PowerShell, but that is outside the scope of this course.

1. Return to the home page of the Microsoft 365 compliance center by selecting **Home** from the left navigation panel.

#### Review

In this setup you redeemed your Azure pass, using the same credentials as your Microsoft 365 tenant.  You also enabled the audit log capability in Microsoft 365.
