---
title: Configure TextExpander for Single sign-on with Microsoft Entra ID
description: Learn how to configure single sign-on between Microsoft Entra ID and TextExpander.

author: nguhiu
manager: mwongerapk
ms.reviewer: celested
ms.service: entra-id
ms.subservice: saas-apps

ms.topic: how-to
ms.date: 05/20/2025
ms.author: gideonkiratu

# Customer intent: As an IT administrator, I want to learn how to configure single sign-on between Microsoft Entra ID and TextExpander so that I can control who has access to TextExpander, enable automatic sign-in with Microsoft Entra accounts, and manage my accounts in one central location.
---

# Configure TextExpander for Single sign-on with Microsoft Entra ID

In this article,  you learn how to integrate TextExpander with Microsoft Entra ID. When you integrate TextExpander with Microsoft Entra ID, you can:

* Control in Microsoft Entra ID who has access to TextExpander.
* Enable your users to be automatically signed-in to TextExpander with their Microsoft Entra accounts.
* Manage your accounts in one central location.

## Prerequisites
The scenario outlined in this article assumes that you already have the following prerequisites:

[!INCLUDE [common-prerequisites.md](~/identity/saas-apps/includes/common-prerequisites.md)]
* TextExpander single sign-on (SSO) enabled subscription.

## Scenario description

In this article,  you configure and test Microsoft Entra SSO in a test environment.

* TextExpander supports **IDP** initiated SSO.
* TextExpander supports **Just In Time** user provisioning.

## Add TextExpander from the gallery

To configure the integration of TextExpander into Microsoft Entra ID, you need to add TextExpander from the gallery to your list of managed SaaS apps.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](~/identity/role-based-access-control/permissions-reference.md#cloud-application-administrator).
1. Browse to **Entra ID** > **Enterprise apps** > **New application**.
1. In the **Add from the gallery** section, type **TextExpander** in the search box.
1. Select **TextExpander** from results panel and then add the app. Wait a few seconds while the app is added to your tenant.

 Alternatively, you can also use the [Enterprise App Configuration Wizard](https://portal.office.com/AdminPortal/home?Q=Docs#/azureadappintegration). In this wizard, you can add an application to your tenant, add users/groups to the app, assign roles, and walk through the SSO configuration as well. [Learn more about Microsoft 365 wizards.](/microsoft-365/admin/misc/azure-ad-setup-guides)

<a name='configure-and-test-azure-ad-sso-for-textexpander'></a>

## Configure and test Microsoft Entra SSO for TextExpander

Configure and test Microsoft Entra SSO with TextExpander using a test user called **B.Simon**. For SSO to work, you need to establish a link relationship between a Microsoft Entra user and the related user in TextExpander.

To configure and test Microsoft Entra SSO with TextExpander, perform the following steps:

1. **[Configure Microsoft Entra SSO](#configure-azure-ad-sso)** - to enable your users to use this feature.
    1. **Create a Microsoft Entra test user** - to test Microsoft Entra single sign-on with B.Simon.
    1. **Assign the Microsoft Entra test user** - to enable B.Simon to use Microsoft Entra single sign-on.
1. **[Configure TextExpander SSO](#configure-textexpander-sso)** - to configure the single sign-on settings on application side.
    1. **[Create TextExpander test user](#create-textexpander-test-user)** - to have a counterpart of B.Simon in TextExpander that's linked to the Microsoft Entra representation of user.
1. **[Test SSO](#test-sso)** - to verify whether the configuration works.

<a name='configure-azure-ad-sso'></a>

## Configure Microsoft Entra SSO

Follow these steps to enable Microsoft Entra SSO.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](~/identity/role-based-access-control/permissions-reference.md#cloud-application-administrator).
1. Browse to **Entra ID** > **Enterprise apps** > **TextExpander** > **Single sign-on**.
1. On the **Select a single sign-on method** page, select **SAML**.
1. On the **Set up single sign-on with SAML** page, select the pencil icon for **Basic SAML Configuration** to edit the settings.

   ![Edit Basic SAML Configuration](common/edit-urls.png)

1. On the **Basic SAML Configuration** section, if you wish to configure the application in **IDP** initiated mode, perform the following steps:

    a. In the **Identifier** text box, type a URL using the following pattern:
    `https://app.textexpander.com/acs/<ORGID>`

    b. In the **Reply URL** text box, type a URL using the following pattern:
    `https://app.textexpander.com/acs/<ORGID>`

	> [!NOTE]
	> These values aren't real. Update these values with the actual Identifier and Reply URL. Contact [TextExpander Client support team](mailto:support@smilesoftware.com) to get these values. You can also refer to the patterns shown in the **Basic SAML Configuration** section.

1. TextExpander application expects the SAML assertions in a specific format, which requires you to add custom attribute mappings to your SAML token attributes configuration. The following screenshot shows the list of default attributes.

	![image](common/default-attributes.png)

1. In addition to above, TextExpander application expects few more attributes to be passed back in SAML response which are shown below. These attributes are also pre populated but you can review them as per your requirements.
	
	| Name | Source Attribute|
	| ---- | --------------- |
	| email | user.email |
	| firstName | user.givenname |
	| lastName | user.surname |

1. On the **Set up single sign-on with SAML** page, in the **SAML Signing Certificate** section,  find **Federation Metadata XML** and select **Download** to download the certificate and save it on your computer.

	![The Certificate download link](common/metadataxml.png)

1. On the **Set up TextExpander** section, copy the appropriate URL(s) based on your requirement.

	![Copy configuration URLs](common/copy-configuration-urls.png)

<a name='create-an-azure-ad-test-user'></a>

[!INCLUDE [create-assign-users-sso.md](~/identity/saas-apps/includes/create-assign-users-sso.md)]

## Configure TextExpander SSO

To configure single sign-on on **TextExpander** side, you need to send the downloaded **Federation Metadata XML** and appropriate copied URLs from the application configuration to [TextExpander support team](mailto:support@smilesoftware.com). They set this setting to have the SAML SSO connection set properly on both sides.

### Create TextExpander test user

In this section, a user called Britta Simon is created in TextExpander. TextExpander supports just-in-time user provisioning, which is enabled by default. There's no action item for you in this section. If a user doesn't already exist in TextExpander, a new one is created after authentication.

## Test SSO 

In this section, you test your Microsoft Entra single sign-on configuration with following options.

* Select **Test this application**, and you should be automatically signed in to the TextExpander for which you set up the SSO.

* You can use Microsoft My Apps. When you select the TextExpander tile in the My Apps, you should be automatically signed in to the TextExpander for which you set up the SSO. For more information about the My Apps, see [Introduction to the My Apps](https://support.microsoft.com/account-billing/sign-in-and-start-apps-from-the-my-apps-portal-2f3b1bae-0e5a-4a86-a33e-876fbd2a4510).

## Related content

Once you configure TextExpander you can enforce session control, which protects exfiltration and infiltration of your organization’s sensitive data in real time. Session control extends from Conditional Access. [Learn how to enforce session control with Microsoft Defender for Cloud Apps](/cloud-app-security/proxy-deployment-aad).
