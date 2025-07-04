---
title: Configure TOPdesk - Secure for Single sign-on with Microsoft Entra ID
description: Learn how to configure single sign-on between Microsoft Entra ID and TOPdesk - Secure.
author: nguhiu
manager: mwongerapk
ms.reviewer: celested
ms.service: entra-id
ms.subservice: saas-apps
ms.topic: how-to
ms.date: 03/25/2025
ms.author: gideonkiratu
ms.custom: sfi-image-nochange
# Customer intent: As an IT administrator, I want to learn how to configure single sign-on between Microsoft Entra ID and TOPdesk - Secure so that I can control who has access to TOPdesk - Secure, enable automatic sign-in with Microsoft Entra accounts, and manage my accounts in one central location.
---
# Configure TOPdesk - Secure for Single sign-on with Microsoft Entra ID

In this article,  you learn how to integrate TOPdesk - Secure with Microsoft Entra ID. When you integrate TOPdesk - Secure with Microsoft Entra ID, you can:

* Control in Microsoft Entra ID who has access to TOPdesk - Secure.
* Enable your users to be automatically signed-in to TOPdesk - Secure (Single Sign-On) with their Microsoft Entra accounts.
* Manage your accounts in one central location.

## Prerequisites
The scenario outlined in this article assumes that you already have the following prerequisites:

[!INCLUDE [common-prerequisites.md](~/identity/saas-apps/includes/common-prerequisites.md)]
* A TOPdesk - Secure single sign-on (SSO)-enabled subscription.

## Scenario description

In this article,  you configure and test Microsoft Entra single sign-on in a test environment.

* TOPdesk - Secure supports **SP** initiated SSO.

## Add TOPdesk - Secure from the gallery

To configure the integration of TOPdesk - Secure into Microsoft Entra ID, you need to add TOPdesk - Secure from the gallery to your list of managed SaaS apps.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](~/identity/role-based-access-control/permissions-reference.md#cloud-application-administrator).
1. Browse to **Entra ID** > **Enterprise apps** > **New application**.
1. In the **Add from the gallery** section, type **TOPdesk - Secure** in the search box.
1. Select **TOPdesk - Secure** from results panel and then add the app. Wait a few seconds while the app is added to your tenant.

 Alternatively, you can also use the [Enterprise App Configuration Wizard](https://portal.office.com/AdminPortal/home?Q=Docs#/azureadappintegration). In this wizard, you can add an application to your tenant, add users/groups to the app, assign roles, and walk through the SSO configuration as well. [Learn more about Microsoft 365 wizards.](/microsoft-365/admin/misc/azure-ad-setup-guides)

<a name='configure-and-test-azure-ad-sso-for-topdesk---secure'></a>

## Configure and test Microsoft Entra SSO for TOPdesk - Secure

In this section, you configure and test Microsoft Entra single sign-on with TOPdesk - Secure based on a test user called **Britta Simon**.
For single sign-on to work, a link relationship between a Microsoft Entra user and the related user in TOPdesk - Secure needs to be established.

To configure and test Microsoft Entra single sign-on with TOPdesk - Secure, you need to perform the following steps:

1. **[Configure Microsoft Entra SSO](#configure-azure-ad-sso)** - to enable your users to use this feature.
    1. **Create a Microsoft Entra test user** - to test Microsoft Entra single sign-on with Britta Simon.
    2. **Assign the Microsoft Entra test user** - to enable Britta Simon to use Microsoft Entra single sign-on.
2. **[Configure TOPdesk - Secure SSO](#configure-topdesk---secure-sso)** - to configure the Single Sign-On settings on application side.
    1. **[Create TOPdesk - Secure test user](#create-topdesk---secure-test-user)** - to have a counterpart of Britta Simon in TOPdesk - Secure that's linked to the Microsoft Entra representation of user.
1. **[Test SSO](#test-sso)** - to verify whether the configuration works.

<a name='configure-azure-ad-sso'></a>

## Configure Microsoft Entra SSO

In this section, you enable Microsoft Entra single sign-on.

To configure Microsoft Entra single sign-on with TOPdesk - Secure, perform the following steps:

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](~/identity/role-based-access-control/permissions-reference.md#cloud-application-administrator).
1. Browse to **Entra ID** > **Enterprise apps** > **TOPdesk - Secure** application integration page, select **Single sign-on**.

1. On the **Select a Single sign-on method** dialog, select **SAML/WS-Fed** mode to enable single sign-on.

1. On the **Set up Single Sign-On with SAML** page, select pencil icon to open **Basic SAML Configuration** dialog.

	![Edit Basic SAML Configuration](common/edit-urls.png)

1. On the **Basic SAML Configuration** section, perform the following steps:

    a. In the **Identifier URL** box, fill in the TOPdesk metadata URL that you can retrieve from the TOPdesk configuration. It should use the following pattern:
    `https://<companyname>.topdesk.net/saml-metadata/<identifier>`

    b. In the **Reply URL** text box, type a URL using the following pattern:
    `https://<companyname>.topdesk.net/tas/secure/login/verify`

    c. In the **Sign-on URL** text box, type a URL using the following pattern:
    `https://<companyname>.topdesk.net`

	> [!NOTE]
	> These values aren't real. Update these values with the actual Identifier,Reply URL and Sign on URL. Contact [TOPdesk - Secure Client support team](https://www.topdesk.com/en/services/support/) to get these values. You can also refer to the patterns shown in the **Basic SAML Configuration** section.

1. On the **Set up Single Sign-On with SAML** page, in the **SAML Signing Certificate** section, select **Download** to download the **Federation Metadata XML** from the given options as per your requirement and save it on your computer.

	![The Certificate download link](common/metadataxml.png)

6. On the **Set up TOPdesk - Secure** section, copy the appropriate URL(s) as per your requirement.

	![Copy configuration URLs](common/copy-configuration-urls.png)

<a name='create-an-azure-ad-test-user'></a>

[!INCLUDE [create-assign-users-sso.md](~/identity/saas-apps/includes/create-assign-users-sso.md)]

## Configure TOPdesk - Secure SSO

1. Sign on to your **TOPdesk - Secure** company site as an administrator.

2. In the **TOPdesk** menu, select **Settings**.

	![Settings](./media/topdesk-secure-tutorial/menu.png "Settings")

3. Select **Login Settings**.

	![Login Settings](./media/topdesk-secure-tutorial/overview.png "Login Settings")

4. Expand the **Login Settings** menu, and then select **General**.

	![General](./media/topdesk-secure-tutorial/navigator.png "General")

5. In the **Secure** section of the **SAML login** configuration section, perform the following steps:

	![Technical Settings](./media/topdesk-secure-tutorial/configuration.png "Technical Settings")

    a. Select **Download** to download the public metadata file, and then save it locally on your computer.

    b. Open the metadata file, and then locate the **AssertionConsumerService** node.

    ![Assertion Consumer Service](./media/topdesk-secure-tutorial/service.png "Assertion Consumer Service")

    c. Copy the **AssertionConsumerService** value, paste this value in the Reply URL textbox in **TOPdesk - Secure Domain and URLs** section.

6. To create a certificate file, perform the following steps:

    ![Certificate](./media/topdesk-secure-tutorial/file.png "Certificate")

    a. Open the downloaded metadata file from Azure portal.

    b. Expand the **RoleDescriptor** node that has a **xsi:type** of **fed:ApplicationServiceType**.

    c. Copy the value of the **X509Certificate** node.

    d. Save the copied **X509Certificate** value locally on your computer in a file.

7. In the **Public** section, select **Add**.

    ![Add](./media/topdesk-secure-tutorial/secure.png "Add")

8. On the **SAML configuration assistant** dialog page, perform the following steps:

    ![SAML Configuration Assistant](./media/topdesk-secure-tutorial/metadata.png "SAML Configuration Assistant")

    a. To upload your downloaded metadata file from Azure portal, under **Federation Metadata**, select **Browse**.

    b. To upload your certificate file, under **Certificate (RSA)**, select **Browse**.

    c. For **Private key(RSA, PKCS8, DER)**, you can upload your own private key or you can contact [TOPdesk - Secure Client support team](https://www.topdesk.com/en/services/support/) to get the private key.

    d. To upload the logo file you got from the TOPdesk support team, under **Logo icon**, select **Browse**.

    e. In the **User name attribute** textbox, type `http://schemas.xmlsoap.org/ws/2005/05/identity/claims/emailaddress`.

    f. In the **Display name** textbox, type a name for your configuration.

    g. Select **Save**.

### Create TOPdesk - Secure test user

In order to enable Microsoft Entra users to log into TOPdesk - Secure, they must be provisioned into TOPdesk - Secure.  
In the case of TOPdesk - Secure, provisioning is a manual task.

### To configure user provisioning, perform the following steps:

1. Sign on to your **TOPdesk - Secure** company site as administrator.

2. In the menu on the top, select **TOPdesk** > **New** > **Support Files** > **Operator**.

    ![Operator](./media/topdesk-secure-tutorial/support-files.png "Operator")

3. On the **New Operator** dialog, perform the following steps:

    ![New Operator](./media/topdesk-secure-tutorial/details.png "New Operator")

    a. Select the **General** tab.

    b. In the **Surname** textbox, type Surname of the user like **Simon**.

    c. Select a **Site** for the account in the **Location** section.

    d. In the **Login Name** textbox of the **TOPdesk Login** section, type a login name for your user.

    e. Select **Save**.

> [!NOTE]
> You can use any other TOPdesk - Secure user account creation tools or APIs provided by TOPdesk - Secure to provision Microsoft Entra user accounts.

## Test SSO

In this section, you test your Microsoft Entra single sign-on configuration with following options. 

* Select **Test this application**, this option redirects to TOPdesk - Secure Sign-on URL where you can initiate the login flow. 

* Go to TOPdesk - Secure Sign-on URL directly and initiate the login flow from there.

* You can use Microsoft My Apps. When you select the TOPdesk - Secure tile in the My Apps, you should be automatically signed in to the TOPdesk - Secure for which you set up the SSO. For more information about the My Apps, see [Introduction to the My Apps](https://support.microsoft.com/account-billing/sign-in-and-start-apps-from-the-my-apps-portal-2f3b1bae-0e5a-4a86-a33e-876fbd2a4510).

## Related content

Once you configure TOPdesk - Secure you can enforce session control, which protects exfiltration and infiltration of your organization’s sensitive data in real time. Session control extends from Conditional Access. [Learn how to enforce session control with Microsoft Defender for Cloud Apps](/cloud-app-security/proxy-deployment-any-app).
