---
title: Configure Egnyte for Single sign-on with Microsoft Entra ID
description: Learn how to configure single sign-on between Microsoft Entra ID and Egnyte.
author: nguhiu
manager: mwongerapk
ms.reviewer: celested
ms.service: entra-id
ms.subservice: saas-apps
ms.topic: how-to
ms.date: 03/25/2025
ms.author: gideonkiratu
ms.custom: sfi-image-nochange
# Customer intent: As an IT administrator, I want to learn how to configure single sign-on between Microsoft Entra ID and Egnyte so that I can control who has access to Egnyte, enable automatic sign-in with Microsoft Entra accounts, and manage my accounts in one central location.
---
# Configure Egnyte for Single sign-on with Microsoft Entra ID

In this article,  you learn how to integrate Egnyte with Microsoft Entra ID. When you integrate Egnyte with Microsoft Entra ID, you can:

* Control in Microsoft Entra ID who has access to Egnyte.
* Enable your users to be automatically signed-in to Egnyte with their Microsoft Entra accounts.
* Manage your accounts in one central location.

## Prerequisites
The scenario outlined in this article assumes that you already have the following prerequisites:

[!INCLUDE [common-prerequisites.md](~/identity/saas-apps/includes/common-prerequisites.md)]
* Egnyte single sign-on (SSO) enabled subscription.

## Scenario description

In this article,  you configure and test Microsoft Entra single sign-on in a test environment.

* Egnyte supports **SP** initiated SSO.

> [!NOTE]
> Identifier of this application is a fixed string value so only one instance can be configured in one tenant.

## Add Egnyte from the gallery

To configure the integration of Egnyte into Microsoft Entra ID, you need to add Egnyte from the gallery to your list of managed SaaS apps.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](~/identity/role-based-access-control/permissions-reference.md#cloud-application-administrator).
1. Browse to **Entra ID** > **Enterprise apps** > **New application**.
1. In the **Add from the gallery** section, type **Egnyte** in the search box.
1. Select **Egnyte** from results panel and then add the app. Wait a few seconds while the app is added to your tenant.

 Alternatively, you can also use the [Enterprise App Configuration Wizard](https://portal.office.com/AdminPortal/home?Q=Docs#/azureadappintegration). In this wizard, you can add an application to your tenant, add users/groups to the app, assign roles, and walk through the SSO configuration as well. [Learn more about Microsoft 365 wizards.](/microsoft-365/admin/misc/azure-ad-setup-guides)

<a name='configure-and-test-azure-ad-sso-for-egnyte'></a>

## Configure and test Microsoft Entra SSO for Egnyte

Configure and test Microsoft Entra SSO with Form.com using a test user called **B.Simon**. For SSO to work, you need to establish a link relationship between a Microsoft Entra user and the related user in Form.com.

To configure and test Microsoft Entra SSO with Form.com, perform the following steps:

1. **[Configure Microsoft Entra SSO](#configure-azure-ad-sso)** - to enable your users to use this feature.
    1. **Create a Microsoft Entra test user** - to test Microsoft Entra single sign-on with B.Simon.
    1. **Assign the Microsoft Entra test user** - to enable B.Simon to use Microsoft Entra single sign-on.
1. **[Configure Egnyte SSO](#configure-egnyte-sso)** - to configure the single sign-on settings on application side.
    1. **[Create Egnyte test user](#create-egnyte-test-user)** - to have a counterpart of B.Simon in Egnyte that's linked to the Microsoft Entra representation of user.
1. **[Test SSO](#test-sso)** - to verify whether the configuration works.

<a name='configure-azure-ad-sso'></a>

## Configure Microsoft Entra SSO

Follow these steps to enable Microsoft Entra SSO.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](~/identity/role-based-access-control/permissions-reference.md#cloud-application-administrator).
1. Browse to **Entra ID** > **Enterprise apps** > **Egnyte** > **Single sign-on**.
1. On the **Select a single sign-on method** page, select **SAML**.
1. On the **Set up single sign-on with SAML** page, select the pencil icon for **Basic SAML Configuration** to edit the settings.

   ![Edit Basic SAML Configuration](common/edit-urls.png)

1. On the **Basic SAML Configuration** section, perform the following steps:

    a. In the **Sign-on URL** text box, type a URL using the following pattern:
    `https://<companyname>.egnyte.com`

    b. In the **Reply URL** text box, type a URL using the following pattern:
    `https://<companyname>.egnyte.com/samlconsumer/AzureAD`
	
	> [!NOTE]
	> These values aren't real. Update the value with the actual Sign-On URL and Reply URL. Contact [Egnyte Client support team](https://www.egnyte.com/corp/contact_egnyte.html) to get the value. You can also refer to the patterns shown in the **Basic SAML Configuration** section.

4. On the **Set up Single Sign-On with SAML** page, in the **SAML Signing Certificate** section, select **Download** to download the **Certificate (Base64)** from the given options as per your requirement and save it on your computer.

	![The Certificate download link](common/certificatebase64.png)

5. On the **Set up Egnyte** section, copy the appropriate URL(s) as per your requirement.

	![Copy configuration URLs](common/copy-configuration-urls.png)

<a name='create-an-azure-ad-test-user'></a>

[!INCLUDE [create-assign-users-sso.md](~/identity/saas-apps/includes/create-assign-users-sso.md)]

## Configure Egnyte SSO

1. In a different web browser window, sign in to your Egnyte company site as an administrator.

2. Select **Settings**.
   
    ![Settings 1](./media/egnyte-tutorial/settings-tab.png "Settings")

3. In the menu, select **Settings**.

    ![Menu 1](./media/egnyte-tutorial/menu-tab.png "Menu")

4. Select the **Configuration** tab, and then select **Security**.

	![Security](./media/egnyte-tutorial/configuration.png "Security")

5. In the **Single Sign-On Authentication** section, perform the following steps:

	![Single Sign On Authentication](./media/egnyte-tutorial/authentication.png "Single Sign On Authentication")   
	
    1. As **Single sign-on authentication**, select **SAML 2.0**.

    1. As **Identity provider**, select **Microsoft Entra ID**.

    1. Paste **Login URL** into the **Identity provider login URL** textbox.

    1. Paste **Microsoft Entra Identifier** which you have into the **Identity provider entity ID** textbox.

    1. Open your base-64 encoded certificate in notepad downloaded from Azure portal, copy the content of it into your clipboard, and then paste it to the **Identity provider certificate** textbox.

    1. As **Default user mapping**, select **Email address**.

    1. As **Use domain-specific issuer value**, select **disabled**.

    1. Select **Save**.

### Create Egnyte test user

To enable Microsoft Entra users to sign in to Egnyte, they must be provisioned into Egnyte. In the case of Egnyte, provisioning is a manual task.

**To provision a user accounts, perform the following steps:**

1. Sign in to your **Egnyte** company site as administrator.

2. Go to **Settings** > **Users & Groups**.

3. Select **Add New User**, and then select the type of user you want to add.
   
    ![Users](./media/egnyte-tutorial/add-user.png "Users")

4. In the **New Power User** section, perform the following steps:
    
    ![New Standard User](./media/egnyte-tutorial/new-user.png "New Standard User")   

	a. In **Email** text box, enter the email of user like **Brittasimon\@contoso.com**.

	b. In **Username** text box, enter the username of user like **Brittasimon**.

	c. Select **Single Sign-On** as **Authentication Type**.
   
	d. Select **Save**.
    
	>[!NOTE]
    >The Microsoft Entra account holder will receive a notification email.
    >

>[!NOTE]
>You can use any other Egnyte user account creation tools or APIs provided by Egnyte to provision Microsoft Entra user accounts.
>

## Test SSO

In this section, you test your Microsoft Entra single sign-on configuration with following options. 

* Select **Test this application**, this option redirects to Egnyte Sign-on URL where you can initiate the login flow. 

* Go to Egnyte Sign-on URL directly and initiate the login flow from there.

* You can use Microsoft My Apps. When you select the Egnyte tile in the My Apps, this option redirects to Egnyte Sign-on URL. For more information about the My Apps, see [Introduction to the My Apps](https://support.microsoft.com/account-billing/sign-in-and-start-apps-from-the-my-apps-portal-2f3b1bae-0e5a-4a86-a33e-876fbd2a4510).

## Related content

Once you configure Egnyte you can enforce session control, which protects exfiltration and infiltration of your organization’s sensitive data in real time. Session control extends from Conditional Access. [Learn how to enforce session control with Microsoft Defender for Cloud Apps](/cloud-app-security/proxy-deployment-any-app).
