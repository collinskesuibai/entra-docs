---
title: Configure Invicti for Single sign-on with Microsoft Entra ID
description: Learn how to configure single sign-on between Microsoft Entra ID and Invicti.
author: nguhiu
manager: mwongerapk
ms.reviewer: CelesteDG
ms.service: entra-id
ms.subservice: saas-apps
ms.topic: how-to
ms.date: 03/25/2025
ms.author: gideonkiratu
ms.custom: sfi-image-nochange
# Customer intent: As an IT administrator, I want to learn how to configure single sign-on between Microsoft Entra ID and Netsparker Enterprise so that I can control who has access to Netsparker Enterprise, enable automatic sign-in with Microsoft Entra accounts, and manage my accounts in one central location.
---

# Configure Invicti for Single sign-on with Microsoft Entra ID

In this article,  you learn how to integrate Invicti with Microsoft Entra ID. When you integrate Invicti with Microsoft Entra ID, you can:

* Control in Microsoft Entra ID who has access to Invicti.
* Enable your users to be automatically signed-in to Invicti with their Microsoft Entra accounts.
* Manage your accounts in one central location.

## Prerequisites

To get started, you need the following items:

* A Microsoft Entra subscription. If you don't have a subscription, you can get a [free account](https://azure.microsoft.com/free/).
* Invicti single sign-on (SSO) enabled subscription.
* Along with Cloud Application Administrator, Application Administrator can also add or manage applications in Microsoft Entra ID.
For more information, see [Azure built-in roles](~/identity/role-based-access-control/permissions-reference.md).

## Scenario description

In this article,  you configure and test Microsoft Entra SSO in a test environment.

* Invicti supports **SP and IDP** initiated SSO.
* Invicti supports **Just In Time** user provisioning.
* Invicti supports [Automated user provisioning](netsparker-enterprise-provisioning-tutorial.md).

> [!NOTE]
> Identifier of this application is a fixed string value so only one instance can be configured in one tenant.

## Add Invicti from the gallery

To configure the integration of Invicti into Microsoft Entra ID, you need to add Invicti from the gallery to your list of managed SaaS apps.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](~/identity/role-based-access-control/permissions-reference.md#cloud-application-administrator).
1. Browse to **Entra ID** > **Enterprise apps** > **New application**.
1. In the **Add from the gallery** section, type **Invicti** in the search box.
1. Select **Invicti** from results panel and then add the app. Wait a few seconds while the app is added to your tenant.

 Alternatively, you can also use the [Enterprise App Configuration Wizard](https://portal.office.com/AdminPortal/home?Q=Docs#/azureadappintegration). In this wizard, you can add an application to your tenant, add users/groups to the app, assign roles, and walk through the SSO configuration as well. [Learn more about Microsoft 365 wizards.](/microsoft-365/admin/misc/azure-ad-setup-guides)

<a name='configure-and-test-azure-ad-sso-for-invicti'></a>

## Configure and test Microsoft Entra SSO for Invicti

Configure and test Microsoft Entra SSO with Invicti using a test user called **B.Simon**. For SSO to work, you need to establish a link relationship between a Microsoft Entra user and the related user in Invicti.

To configure and test Microsoft Entra SSO with Invicti, perform the following steps:

1. **[Configure Microsoft Entra SSO](#configure-azure-ad-sso)** - to enable your users to use this feature.
    1. **Create a Microsoft Entra test user** - to test Microsoft Entra single sign-on with B.Simon.
    1. **Assign the Microsoft Entra test user** - to enable B.Simon to use Microsoft Entra single sign-on.
1. **[Configure Invicti SSO](#configure-invicti-sso)** - to configure the single sign-on settings on application side.
    1. **[Create Invicti test user](#create-invicti-test-user)** - to have a counterpart of B.Simon in Invicti that's linked to the Microsoft Entra representation of user.
1. **[Test SSO](#test-sso)** - to verify whether the configuration works.

<a name='configure-azure-ad-sso'></a>

## Configure Microsoft Entra SSO

Follow these steps to enable Microsoft Entra SSO.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](~/identity/role-based-access-control/permissions-reference.md#cloud-application-administrator).
1. Browse to **Entra ID** > **Enterprise apps** > **Invicti** > **Single sign-on**.
1. On the **Select a single sign-on method** page, select **SAML**.
1. On the **Set up single sign-on with SAML** page, select the edit/pen icon for **Basic SAML Configuration** to edit the settings.

   ![Edit Basic SAML Configuration](common/edit-urls.png)

1. On the **Basic SAML Configuration** section, if you wish to configure the application in **IDP** initiated mode, perform the following steps: 

    In the **Reply URL** text box, type a URL using the following pattern:
    `https://www.netsparkercloud.com/account/assertionconsumerservice/?spId=<SPID>`

1. Select **Set additional URLs** and perform the following step if you wish to configure the application in **SP** initiated mode:

    In the **Sign-on URL** text box, type the URL:
    `https://www.netsparkercloud.com/account/ssosignin/`

	> [!NOTE]
	> The Reply URL value isn't real. Update the value with the actual Reply URL. Contact [Invicti Client support team](mailto:support@netsparker.com) to get these values. You can also refer to the patterns shown in the **Basic SAML Configuration** section. 

1. On the **Set up single sign-on with SAML** page, in the **SAML Signing Certificate** section,  find **Certificate (Base64)** and select **Download** to download the certificate and save it on your computer.

	![The Certificate download link](common/certificatebase64.png)

1. On the **Set up Invicti** section, copy the appropriate URL(s) based on your requirement.

	![Copy configuration URLs](common/copy-configuration-urls.png)

<a name='create-an-azure-ad-test-user'></a>

[!INCLUDE [create-assign-users-sso.md](~/identity/saas-apps/includes/create-assign-users-sso.md)]

## Configure Invicti SSO

1.  Log in to Invicti as an Administrator.

1. Go to the **Settings > Single Sign-On**.

1. In the **Single Sign-On** window, select the **Microsoft Entra ID** tab. 

1. Perform the following steps in the following page.

    ![Microsoft Entra ID tab](./media/netsparker-enterprise-tutorial/configure-sso.png)

    a. Copy the **Identifier** value, paste this value into the **Identifier** text box in the **Basic SAML Configuration** section.

    b. Copy the **SAML 2.0 Service URL** value, paste this value into the **Reply URL** text box in the **Basic SAML Configuration** section.

    c. Paste the **Identifier** value into the **IdP Identifier** field.

    d. Paste the **Reply URL** value into the **SAML 2.0 Endpoint** field.

    e. Open the downloaded **Certificate (Base64)** into Notepad and paste the content into the **x.509 Certificate** textbox.

    f. Check **Enable Auto Provisioning** and **Require SAML assertions to be encrypted** as required.

    g. Select **Save Changes**.

### Create Invicti test user

In this section, a user called Britta Simon is created in Invicti. Invicti supports just-in-time user provisioning, which is enabled by default. There's no action item for you in this section. If a user doesn't already exist in Invicti, a new one is created after authentication.

## Test SSO 

In this section, you test your Microsoft Entra single sign-on configuration with following options. 

#### SP initiated:

* Select **Test this application**, this option redirects to Invicti Sign-on URL where you can initiate the login flow.  

* Go to Invicti Sign-on URL directly and initiate the login flow from there.

#### IDP initiated:

* Select **Test this application**, and you should be automatically signed in to the Invicti for which you set up the SSO. 

You can also use Microsoft My Apps to test the application in any mode. When you select the Invicti tile in the My Apps, if configured in SP mode you would be redirected to the application sign on page for initiating the login flow and if configured in IDP mode, you should be automatically signed in to the Invicti for which you set up the SSO. For more information, see [Microsoft Entra My Apps](/azure/active-directory/manage-apps/end-user-experiences#azure-ad-my-apps).

## Related content

Once you configure Invicti you can enforce session control, which protects exfiltration and infiltration of your organization’s sensitive data in real time. Session control extends from Conditional Access. [Learn how to enforce session control with Microsoft Cloud App Security](/cloud-app-security/proxy-deployment-aad).
