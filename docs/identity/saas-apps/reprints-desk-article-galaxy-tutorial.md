---
title: Configure Reprints Desk - Article Galaxy for Single sign-on with Microsoft Entra ID
description: Learn how to configure single sign-on between Microsoft Entra ID and Reprints Desk - Article Galaxy.

author: nguhiu
manager: mwongerapk
ms.reviewer: celested
ms.service: entra-id
ms.subservice: saas-apps

ms.topic: how-to
ms.date: 05/20/2025
ms.author: gideonkiratu

# Customer intent: As an IT administrator, I want to learn how to configure single sign-on between Microsoft Entra ID and Reprints Desk - Article Galaxy so that I can control who has access to Reprints Desk - Article Galaxy, enable automatic sign-in with Microsoft Entra accounts, and manage my accounts in one central location.
---

# Configure Reprints Desk - Article Galaxy for Single sign-on with Microsoft Entra ID

In this article,  you learn how to integrate Reprints Desk - Article Galaxy with Microsoft Entra ID. When you integrate Reprints Desk - Article Galaxy with Microsoft Entra ID, you can:

* Control in Microsoft Entra ID who has access to Reprints Desk - Article Galaxy.
* Enable your users to be automatically signed-in to Reprints Desk - Article Galaxy with their Microsoft Entra accounts.
* Manage your accounts in one central location.

## Prerequisites

To get started, you need the following items:

* A Microsoft Entra subscription. If you don't have a subscription, you can get a [free account](https://azure.microsoft.com/free/).
* Reprints Desk - Article Galaxy single sign-on (SSO) enabled subscription.
* Along with Cloud Application Administrator, Application Administrator can also add or manage applications in Microsoft Entra ID.
For more information, see [Azure built-in roles](~/identity/role-based-access-control/permissions-reference.md).

## Scenario description

In this article,  you configure and test Microsoft Entra SSO in a test environment.

* Reprints Desk - Article Galaxy supports **IDP** initiated SSO.

* Reprints Desk - Article Galaxy supports **Just In Time** user provisioning.

## Add Reprints Desk - Article Galaxy from the gallery

To configure the integration of Reprints Desk - Article Galaxy into Microsoft Entra ID, you need to add Reprints Desk - Article Galaxy from the gallery to your list of managed SaaS apps.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](~/identity/role-based-access-control/permissions-reference.md#cloud-application-administrator).
1. Browse to **Entra ID** > **Enterprise apps** > **New application**.
1. In the **Add from the gallery** section, type **Reprints Desk - Article Galaxy** in the search box.
1. Select **Reprints Desk - Article Galaxy** from results panel and then add the app. Wait a few seconds while the app is added to your tenant.

 Alternatively, you can also use the [Enterprise App Configuration Wizard](https://portal.office.com/AdminPortal/home?Q=Docs#/azureadappintegration). In this wizard, you can add an application to your tenant, add users/groups to the app, assign roles, and walk through the SSO configuration as well. [Learn more about Microsoft 365 wizards.](/microsoft-365/admin/misc/azure-ad-setup-guides)

<a name='configure-and-test-azure-ad-sso-for-reprints-desk---article-galaxy'></a>

## Configure and test Microsoft Entra SSO for Reprints Desk - Article Galaxy

Configure and test Microsoft Entra SSO with Reprints Desk - Article Galaxy using a test user called **B.Simon**. For SSO to work, you need to establish a link relationship between a Microsoft Entra user and the related user in Reprints Desk - Article Galaxy.

To configure and test Microsoft Entra SSO with Reprints Desk - Article Galaxy, perform the following steps:

1. **[Configure Microsoft Entra SSO](#configure-azure-ad-sso)** - to enable your users to use this feature.
   1. **Create a Microsoft Entra test user** - to test Microsoft Entra single sign-on with B.Simon.
   1. **Assign the Microsoft Entra test user** - to enable B.Simon to use Microsoft Entra single sign-on.
1. **[Configure Reprints Desk - Article Galaxy SSO](#configure-reprints-desk---article-galaxy-sso)** - to configure the single sign-on settings on application side.
   1. **[Create Reprints Desk - Article Galaxy test user](#create-reprints-desk---article-galaxy-test-user)** - to have a counterpart of B.Simon in Reprints Desk - Article Galaxy that's linked to the Microsoft Entra representation of user.
1. **[Test SSO](#test-sso)** - to verify whether the configuration works.

<a name='configure-azure-ad-sso'></a>

## Configure Microsoft Entra SSO

Follow these steps to enable Microsoft Entra SSO.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](~/identity/role-based-access-control/permissions-reference.md#cloud-application-administrator).
1. Browse to **Entra ID** > **Enterprise apps** > **Reprints Desk - Article Galaxy** > **Single sign-on**.
1. On the **Select a single sign-on method** page, select **SAML**.
1. On the **Set up single sign-on with SAML** page, select the pencil icon for **Basic SAML Configuration** to edit the settings.

   ![Screenshot shows to edit Basic S A M L Configuration.](common/edit-urls.png "Basic Configuration")

1. On the **Basic SAML Configuration** section, the application is pre-configured and the necessary URLs are already pre-populated with Azure. The user needs to save the configuration by selecting the **Save** button.

1. Reprints Desk - Article Galaxy application expects the SAML assertions in a specific format, which requires you to add custom attribute mappings to your SAML token attributes configuration. The following screenshot shows the list of default attributes.

	![Screenshot shows the image of Reprints Desk application.](common/default-attributes.png "Image")

1. In addition to above, Reprints Desk - Article Galaxy application expects few more attributes to be passed back in SAML response which are shown below. These attributes are also pre populated but you can review them as per your requirements.

	| Name | Source Attribute|
	| ------------ | --------- |
	| firstname | user.givenname |
	| lastname | user.surname |

1. On the **Set up single sign-on with SAML** page, in the **SAML Signing Certificate** section,  find **Federation Metadata XML** and select **Download** to download the certificate and save it on your computer.

	![Screenshot shows the Certificate download link.](common/metadataxml.png "Certificate")

1. On the **Set up Reprints Desk - Article Galaxy** section, copy the appropriate URL(s) based on your requirement.

	![Screenshot shows to copy configuration appropriate U R L.](common/copy-configuration-urls.png "Metadata")  

<a name='create-an-azure-ad-test-user'></a>

[!INCLUDE [create-assign-users-sso.md](~/identity/saas-apps/includes/create-assign-users-sso.md)]

## Configure Reprints Desk - Article Galaxy SSO

To configure single sign-on on **Reprints Desk - Article Galaxy** side, you need to send the downloaded **Federation Metadata XML** and appropriate copied URLs from the application configuration to [Reprints Desk - Article Galaxy support team](mailto:customersupport@reprintsdesk.com). They set this setting to have the SAML SSO connection set properly on both sides.

### Create Reprints Desk - Article Galaxy test user

In this section, a user called B.Simon is created in Reprints Desk - Article Galaxy. Reprints Desk - Article Galaxy supports just-in-time user provisioning, which is enabled by default. There's no action item for you in this section. If a user doesn't already exist in Reprints Desk - Article Galaxy, a new one is created after authentication.

## Test SSO 

In this section, you test your Microsoft Entra single sign-on configuration with following options.

* Select **Test this application**, and you should be automatically signed in to the Reprints Desk - Article Galaxy for which you set up the SSO.

* You can use Microsoft My Apps. When you select the Reprints Desk - Article Galaxy tile in the My Apps, you should be automatically signed in to the Reprints Desk - Article Galaxy for which you set up the SSO. For more information, see [Microsoft Entra My Apps](/azure/active-directory/manage-apps/end-user-experiences#azure-ad-my-apps).

## Related content

Once you configure Reprints Desk - Article Galaxy you can enforce session control, which protects exfiltration and infiltration of your organization’s sensitive data in real time. Session control extends from Conditional Access. [Learn how to enforce session control with Microsoft Cloud App Security](/cloud-app-security/proxy-deployment-aad).
