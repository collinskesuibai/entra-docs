---
title: Configure E2open LSP for Single sign-on with Microsoft Entra ID
description: Learn how to configure single sign-on between Microsoft Entra ID and E2open LSP.

author: nguhiu
manager: mwongerapk
ms.reviewer: CelesteDG
ms.service: entra-id
ms.subservice: saas-apps

ms.topic: how-to
ms.date: 03/25/2025
ms.author: gideonkiratu


# Customer intent: As an IT administrator, I want to learn how to configure single sign-on between Microsoft Entra ID and E2open LSP so that I can control who has access to E2open LSP, enable automatic sign-in with Microsoft Entra accounts, and manage my accounts in one central location.
---

# Configure E2open LSP for Single sign-on with Microsoft Entra ID

In this article,  you learn how to integrate E2open LSP with Microsoft Entra ID. When you integrate E2open LSP with Microsoft Entra ID, you can:

* Control in Microsoft Entra ID who has access to E2open LSP.
* Enable your users to be automatically signed-in to E2open LSP with their Microsoft Entra accounts.
* Manage your accounts in one central location.

## Prerequisites

To get started, you need the following items:

* A Microsoft Entra subscription. If you don't have a subscription, you can get a [free account](https://azure.microsoft.com/free/).
* E2open LSP single sign-on (SSO) enabled subscription.
* Along with Cloud Application Administrator, Application Administrator can also add or manage applications in Microsoft Entra ID.
For more information, see [Azure built-in roles](~/identity/role-based-access-control/permissions-reference.md).

## Scenario description

In this article,  you configure and test Microsoft Entra SSO in a test environment.

* E2open LSP supports **SP** initiated SSO.

## Add E2open LSP from the gallery

To configure the integration of E2open LSP into Microsoft Entra ID, you need to add E2open LSP from the gallery to your list of managed SaaS apps.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](~/identity/role-based-access-control/permissions-reference.md#cloud-application-administrator).
1. Browse to **Entra ID** > **Enterprise apps** > **New application**.
1. In the **Add from the gallery** section, type **E2open LSP** in the search box.
1. Select **E2open LSP** from results panel and then add the app. Wait a few seconds while the app is added to your tenant.

 Alternatively, you can also use the [Enterprise App Configuration Wizard](https://portal.office.com/AdminPortal/home?Q=Docs#/azureadappintegration). In this wizard, you can add an application to your tenant, add users/groups to the app, assign roles, and walk through the SSO configuration as well. [Learn more about Microsoft 365 wizards.](/microsoft-365/admin/misc/azure-ad-setup-guides)

<a name='configure-and-test-azure-ad-sso-for-e2open-lsp'></a>

## Configure and test Microsoft Entra SSO for E2open LSP

Configure and test Microsoft Entra SSO with E2open LSP using a test user called **B.Simon**. For SSO to work, you need to establish a link relationship between a Microsoft Entra user and the related user in E2open LSP.

To configure and test Microsoft Entra SSO with E2open LSP, perform the following steps:

1. **[Configure Microsoft Entra SSO](#configure-azure-ad-sso)** - to enable your users to use this feature.
    1. **Create a Microsoft Entra test user** - to test Microsoft Entra single sign-on with B.Simon.
    1. **Assign the Microsoft Entra test user** - to enable B.Simon to use Microsoft Entra single sign-on.
1. **[Configure E2open LSP SSO](#configure-e2open-lsp-sso)** - to configure the single sign-on settings on application side.
    1. **[Create E2open LSP test user](#create-e2open-lsp-test-user)** - to have a counterpart of B.Simon in E2open LSP that's linked to the Microsoft Entra representation of user.
1. **[Test SSO](#test-sso)** - to verify whether the configuration works.

<a name='configure-azure-ad-sso'></a>

## Configure Microsoft Entra SSO

Follow these steps to enable Microsoft Entra SSO.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](~/identity/role-based-access-control/permissions-reference.md#cloud-application-administrator).
1. Browse to **Entra ID** > **Enterprise apps** > **E2open LSP** > **Single sign-on**.
1. On the **Select a single sign-on method** page, select **SAML**.
1. On the **Set up single sign-on with SAML** page, select the pencil icon for **Basic SAML Configuration** to edit the settings.

   ![Screenshot shows to edit Basic S A M L Configuration.](common/edit-urls.png "Basic Configuration")

1. On the **Basic SAML Configuration** section, perform the following steps:

    a. In the **Identifier** text box, type a URL using the following pattern:
    `https://<Customer name>-<Environment>.tms-lsp.blujaysolutions.net/navi/saml/metadata`
    
    b. In the **Reply URL** text box, type a URL using the following pattern:
    `https://<Customer name>-<Environment>.tms-lsp.blujaysolutions.net/navi/sam`

    c. In the **Sign-on URL** text box, type a URL using the following pattern:
    `https://<Customer name>-<Environment>.tms-lsp.blujaysolutions.net/navi/`

    > [!NOTE]
	> These values aren't real. Update these values with the actual Identifier, Reply URL and Sign-on URL. Contact [E2open LSP Client support team](mailto:customersupport@e2open.com) to get these values. You can also refer to the patterns shown in the **Basic SAML Configuration** section.

1. On the **Set up single sign-on with SAML** page, In the **SAML Signing Certificate** section, select copy button to copy **App Federation Metadata Url** and save it on your computer.

	![Screenshot shows the Certificate download link.](common/copy-metadataurl.png "Certificate")

<a name='create-an-azure-ad-test-user'></a>

[!INCLUDE [create-assign-users-sso.md](~/identity/saas-apps/includes/create-assign-users-sso.md)]

## Configure E2open LSP SSO

To configure single sign-on on **E2open LSP** side, you need to send the **App Federation Metadata Url** to [E2open LSP support team](mailto:customersupport@e2open.com). They set this setting to have the SAML SSO connection set properly on both sides.

### Create E2open LSP test user

In this section, you create a user called Britta Simon in E2open LSP. Work with [E2open LSP support team](mailto:customersupport@e2open.com) to add the users in the E2open LSP platform. Users must be created and activated before you use single sign-on.

## Test SSO 

In this section, you test your Microsoft Entra single sign-on configuration with following options. 

* Select **Test this application**, this option redirects to E2open LSP Sign-on URL where you can initiate the login flow. 

* Go to E2open LSP Sign-on URL directly and initiate the login flow from there.

* You can use Microsoft My Apps. When you select the E2open LSP tile in the My Apps, this option redirects to E2open LSP Sign-on URL. For more information about the My Apps, see [Introduction to the My Apps](https://support.microsoft.com/account-billing/sign-in-and-start-apps-from-the-my-apps-portal-2f3b1bae-0e5a-4a86-a33e-876fbd2a4510).

## Related content

Once you configure E2open LSP you can enforce session control, which protects exfiltration and infiltration of your organization’s sensitive data in real time. Session control extends from Conditional Access. [Learn how to enforce session control with Microsoft Defender for Cloud Apps](/cloud-app-security/proxy-deployment-any-app).
