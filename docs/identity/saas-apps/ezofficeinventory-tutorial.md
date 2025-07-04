---
title: Configure EZOfficeInventory for Single sign-on with Microsoft Entra ID
description: Learn how to configure single sign-on between Microsoft Entra ID and EZOfficeInventory.
author: nguhiu
manager: mwongerapk
ms.reviewer: celested
ms.service: entra-id
ms.subservice: saas-apps
ms.topic: how-to
ms.date: 03/25/2025
ms.author: gideonkiratu
ms.custom: sfi-image-nochange
# Customer intent: As an IT administrator, I want to learn how to configure single sign-on between Microsoft Entra ID and EZOfficeInventory so that I can control who has access to EZOfficeInventory, enable automatic sign-in with Microsoft Entra accounts, and manage my accounts in one central location.
---

# Configure EZOfficeInventory for Single sign-on with Microsoft Entra ID

In this article,  you learn how to integrate EZOfficeInventory with Microsoft Entra ID. When you integrate EZOfficeInventory with Microsoft Entra ID, you can:

* Control in Microsoft Entra ID who has access to EZOfficeInventory.
* Enable your users to be automatically signed-in to EZOfficeInventory with their Microsoft Entra accounts.
* Manage your accounts in one central location.

## Prerequisites

The scenario outlined in this article assumes that you already have the following prerequisites:

[!INCLUDE [common-prerequisites.md](~/identity/saas-apps/includes/common-prerequisites.md)]
* EZOfficeInventory single sign-on (SSO) enabled subscription.

## Scenario description

In this article,  you configure and test Microsoft Entra SSO in a test environment.

* EZOfficeInventory supports **SP** initiated SSO.
* EZOfficeInventory supports **Just In Time** user provisioning.

> [!NOTE]
> Identifier of this application is a fixed string value so only one instance can be configured in one tenant.

## Add EZOfficeInventory from the gallery

To configure the integration of EZOfficeInventory into Microsoft Entra ID, you need to add EZOfficeInventory from the gallery to your list of managed SaaS apps.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](~/identity/role-based-access-control/permissions-reference.md#cloud-application-administrator).
1. Browse to **Entra ID** > **Enterprise apps** > **New application**.
1. In the **Add from the gallery** section, type **EZOfficeInventory** in the search box.
1. Select **EZOfficeInventory** from results panel and then add the app. Wait a few seconds while the app is added to your tenant.

 [!INCLUDE [sso-wizard.md](~/identity/saas-apps/includes/sso-wizard.md)]

<a name='configure-and-test-azure-ad-sso-for-ezofficeinventory'></a>

## Configure and test Microsoft Entra SSO for EZOfficeInventory

Configure and test Microsoft Entra SSO with EZOfficeInventory using a test user called **B.Simon**. For SSO to work, you need to establish a link relationship between a Microsoft Entra user and the related user in EZOfficeInventory.

To configure and test Microsoft Entra SSO with EZOfficeInventory, perform the following steps:

1. **[Configure Microsoft Entra SSO](#configure-azure-ad-sso)** - to enable your users to use this feature.
    1. **Create a Microsoft Entra test user** - to test Microsoft Entra single sign-on with B.Simon.
    1. **Assign the Microsoft Entra test user** - to enable B.Simon to use Microsoft Entra single sign-on.
1. **[Configure EZOfficeInventory SSO](#configure-ezofficeinventory-sso)** - to configure the single sign-on settings on application side.
    1. **[Create EZOfficeInventory test user](#create-ezofficeinventory-test-user)** - to have a counterpart of B.Simon in EZOfficeInventory that's linked to the Microsoft Entra representation of user.
1. **[Test SSO](#test-sso)** - to verify whether the configuration works.

<a name='configure-azure-ad-sso'></a>

## Configure Microsoft Entra SSO

Follow these steps to enable Microsoft Entra SSO.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](~/identity/role-based-access-control/permissions-reference.md#cloud-application-administrator).
1. Browse to **Entra ID** > **Enterprise apps** > **EZOfficeInventory** > **Single sign-on**.
1. On the **Select a single sign-on method** page, select **SAML**.
1. On the **Set up single sign-on with SAML** page, select the pencil icon for **Basic SAML Configuration** to edit the settings.

   ![Edit Basic SAML Configuration](common/edit-urls.png)

1. On the **Basic SAML Configuration** section, enter the values for the following fields:

    In the **Sign-on URL** text box, type a URL using the following pattern:
    `https://<SUBDOMAIN>.ezofficeinventory.com/users/sign_in`

	> [!NOTE]
	> The value isn't real. Update the value with the actual Sign-On URL. Contact [EZOfficeInventory Client support team](mailto:support@ezofficeinventory.com) to get the value. You can also refer to the patterns shown in the **Basic SAML Configuration** section.

1. EZOfficeInventory application expects the SAML assertions in a specific format, which requires you to add custom attribute mappings to your SAML token attributes configuration. The following screenshot shows the list of default attributes.

	![image](common/default-attributes.png)

1. In addition to above, EZOfficeInventory application expects few more attributes to be passed back in SAML response which are shown below. These attributes are also pre populated but you can review them as per your requirement.

	| Name | Source Attribute|
	| ---------------| --------------- |
	| first_name | user.givenname |
	| last_name | user.surname |
	| email | user.mail |

1. On the **Set up single sign-on with SAML** page, in the **SAML Signing Certificate** section,  find **Certificate (Base64)** and select **Download** to download the certificate and save it on your computer.

	![The Certificate download link](common/certificatebase64.png)

1. On the **Set up EZOfficeInventory** section, copy the appropriate URL(s) based on your requirement.

	![Copy configuration URLs](common/copy-configuration-urls.png)

<a name='create-an-azure-ad-test-user'></a>

[!INCLUDE [create-assign-users-sso.md](~/identity/saas-apps/includes/create-assign-users-sso.md)]

## Configure EZOfficeInventory SSO




1. In a different web browser window, sign in to your EZOfficeInventory company site as an administrator

1. On the top-right corner of the page, select **Profile** and then navigate to **Settings** > **Add Ons**.

    ![Screenshot that shows the "Settings" page with the "Add Ons" action selected.](./media/ezofficeinventory-tutorial/settings.png)

1. Scroll down up to the **SAML Integration** section, perform the following steps:

	![EZOfficeInventory configuration](./media/ezofficeinventory-tutorial/integration.png)

	a. Check the **Enabled** option.

	b. In the **Identity Provider URL** text box, Paste the **Login URL** value, which you copied previously.

	c. Open the Base64 encoded certificate in notepad, copy its content and paste it into the **Identity Provider Certificate** text box.

	d. In **Login Button Text** text box, enter the text of login button.

	e. In **First Name** text box, enter **first_name**.

	f. In **Last Name** text box, enter **last_name**.

	g. In **Email** text box, enter **email**.

	h. Select your role as per your requirement from the **EZOfficeInventory Role By default** option.

	i. Select **Update**.

### Create EZOfficeInventory test user

In this section, a user called Britta Simon is created in EZOfficeInventory. EZOfficeInventory supports just-in-time user provisioning, which is enabled by default. There's no action item for you in this section. If a user doesn't already exist in EZOfficeInventory, a new one is created after authentication.

## Test SSO

In this section, you test your Microsoft Entra single sign-on configuration with following options. 

* Select **Test this application**, this option redirects to EZOfficeInventory Sign-on URL where you can initiate the login flow. 

* Go to EZOfficeInventory Sign-on URL directly and initiate the login flow from there.

* You can use Microsoft My Apps. When you select the EZOfficeInventory tile in the My Apps, this option redirects to EZOfficeInventory Sign-on URL. For more information about the My Apps, see [Introduction to the My Apps](https://support.microsoft.com/account-billing/sign-in-and-start-apps-from-the-my-apps-portal-2f3b1bae-0e5a-4a86-a33e-876fbd2a4510).

## Related content

Once you configure EZOfficeInventory you can enforce session control, which protects exfiltration and infiltration of your organization’s sensitive data in real time. Session control extends from Conditional Access. [Learn how to enforce session control with Microsoft Defender for Cloud Apps](/cloud-app-security/proxy-deployment-aad).
