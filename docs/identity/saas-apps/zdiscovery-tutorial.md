---
title: Configure ZDiscovery for Single sign-on with Microsoft Entra ID
description: Learn how to configure single sign-on between Microsoft Entra ID and ZDiscovery.

author: nguhiu
manager: mwongerapk
ms.reviewer: CelesteDG
ms.service: entra-id
ms.subservice: saas-apps

ms.topic: how-to
ms.date: 05/20/2025
ms.author: gideonkiratu


# Customer intent: As an IT administrator, I want to learn how to configure single sign-on between Microsoft Entra ID and ZDiscovery so that I can control who has access to ZDiscovery, enable automatic sign-in with Microsoft Entra accounts, and manage my accounts in one central location.
---

# Configure ZDiscovery for Single sign-on with Microsoft Entra ID

In this article,  you learn how to integrate ZDiscovery with Microsoft Entra ID. When you integrate ZDiscovery with Microsoft Entra ID, you can:

* Control in Microsoft Entra ID who has access to ZDiscovery.
* Enable your users to be automatically signed-in to ZDiscovery with their Microsoft Entra accounts.
* Manage your accounts in one central location.

## Prerequisites

To get started, you need the following items:

* A Microsoft Entra subscription. If you don't have a subscription, you can get a [free account](https://azure.microsoft.com/free/).
* ZDiscovery single sign-on (SSO) enabled subscription.
* Along with Cloud Application Administrator, Application Administrator can also add or manage applications in Microsoft Entra ID.
For more information, see [Azure built-in roles](~/identity/role-based-access-control/permissions-reference.md).

## Scenario description

In this article,  you configure and test Microsoft Entra SSO in a test environment.

* ZDiscovery supports **SP** and **IDP** initiated SSO.

## Add ZDiscovery from the gallery

To configure the integration of ZDiscovery into Microsoft Entra ID, you need to add ZDiscovery from the gallery to your list of managed SaaS apps.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](~/identity/role-based-access-control/permissions-reference.md#cloud-application-administrator).
1. Browse to **Entra ID** > **Enterprise apps** > **New application**.
1. In the **Add from the gallery** section, type **ZDiscovery** in the search box.
1. Select **ZDiscovery** from results panel and then add the app. Wait a few seconds while the app is added to your tenant.

 Alternatively, you can also use the [Enterprise App Configuration Wizard](https://portal.office.com/AdminPortal/home?Q=Docs#/azureadappintegration). In this wizard, you can add an application to your tenant, add users/groups to the app, assign roles, and walk through the SSO configuration as well. [Learn more about Microsoft 365 wizards.](/microsoft-365/admin/misc/azure-ad-setup-guides)

<a name='configure-and-test-azure-ad-sso-for-zdiscovery'></a>

## Configure and test Microsoft Entra SSO for ZDiscovery

Configure and test Microsoft Entra SSO with ZDiscovery using a test user called **B.Simon**. For SSO to work, you need to establish a link relationship between a Microsoft Entra user and the related user in ZDiscovery.

To configure and test Microsoft Entra SSO with ZDiscovery, perform the following steps:

1. **[Configure Microsoft Entra SSO](#configure-azure-ad-sso)** - to enable your users to use this feature.
    1. **Create a Microsoft Entra test user** - to test Microsoft Entra single sign-on with B.Simon.
    1. **Assign the Microsoft Entra test user** - to enable B.Simon to use Microsoft Entra single sign-on.
1. **[Configure ZDiscovery SSO](#configure-zdiscovery-sso)** - to configure the single sign-on settings on application side.
    1. **[Create ZDiscovery test user](#create-zdiscovery-test-user)** - to have a counterpart of B.Simon in ZDiscovery that's linked to the Microsoft Entra representation of user.
1. **[Test SSO](#test-sso)** - to verify whether the configuration works.

<a name='configure-azure-ad-sso'></a>

## Configure Microsoft Entra SSO

Follow these steps to enable Microsoft Entra SSO.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](~/identity/role-based-access-control/permissions-reference.md#cloud-application-administrator).
1. Browse to **Entra ID** > **Enterprise apps** > **ZDiscovery** > **Single sign-on**.
1. On the **Select a single sign-on method** page, select **SAML**.
1. On the **Set up single sign-on with SAML** page, select the pencil icon for **Basic SAML Configuration** to edit the settings.

    ![Screenshot shows to edit Basic S A M L Configuration.](common/edit-urls.png "Basic Configuration")

1. On the **Basic SAML Configuration** section, perform the following steps:

    a. In the **Identifier** textbox, type a value using the following pattern:
    `urn:auth0:<AUTH0_TENANT>:<CONNECTION_NAME>`

    b. In the **Reply URL** textbox, type a URL using one of the following patterns:

    | **Reply URL** |
    |-----------|
    | `https://zapproved.auth0.com/login/callback?connection=<YOUR_AUTH0_CONNECTION_NAME>` |
    | `https://zapproved-sandbox.auth0.com/login/callback?connection=<YOUR_AUTH0_CONNECTION_NAME>` |
    | `https://zapproved-preview.us.auth0.com/login/callback?connection=<YOUR_AUTH0_CONNECTION_NAME>` |

1. Select **Set additional URLs** and perform the following step if you wish to configure the application in **SP** initiated mode:    

    In the **Sign-on URL** text box, type a URL using one of the following patterns:

    | **Sign-on URL** |
    |------------|
    | `https://zdiscovery.io/<CustomerName>/` |
    | `https://zdiscovery-sandbox.io/<CustomerName>` |
    | `https://zdiscovery-preview.io/<CustomerName>` |

    > [!Note]
    > These values aren't real. Update these values with the actual Identifier, Reply URL and Sign on URL. Contact [Rise.com support team](mailto:support@zapproved.com) to get these values. You can also refer to the patterns shown in the **Basic SAML Configuration** section.

1. On the **Set up single sign-on with SAML** page, in the **SAML Signing Certificate** section,  find **Certificate (PEM)** and select **Download** to download the certificate and save it on your computer.

	![Screenshot shows the Certificate download link.](common/certificate-base64-download.png "Certificate")

1. On the **Set up ZDiscovery** section, copy the appropriate URL(s) based on your requirement.

	![Screenshot shows to copy configuration appropriate U R L.](common/copy-configuration-urls.png "Metadata")    

<a name='create-an-azure-ad-test-user'></a>

[!INCLUDE [create-assign-users-sso.md](~/identity/saas-apps/includes/create-assign-users-sso.md)]

## Configure ZDiscovery SSO

To configure single sign-on on **ZDiscovery** side, you need to send the downloaded **Certificate (PEM)** and appropriate copied URLs from the application configuration to [ZDiscovery support team](mailto:support@zapproved.com). They set this setting to have the SAML SSO connection set properly on both sides.

### Create ZDiscovery test user

In this section, you create a user called Britta Simon at ZDiscovery. Work with [ZDiscovery support team](mailto:support@zapproved.com) to add the users in the ZDiscovery platform. Users must be created and activated before you use single sign-on.

## Test SSO 

In this section, you test your Microsoft Entra single sign-on configuration with following options. 

#### SP initiated:

* Select **Test this application**, this option redirects to ZDiscovery Sign-On URL where you can initiate the login flow.  

* Go to ZDiscovery Sign-On URL directly and initiate the login flow from there.

#### IDP initiated:

* Select **Test this application**, and you should be automatically signed in to the ZDiscovery for which you set up the SSO. 

You can also use Microsoft My Apps to test the application in any mode. When you select the ZDiscovery tile in the My Apps, if configured in SP mode you would be redirected to the application Sign-On page for initiating the login flow and if configured in IDP mode, you should be automatically signed in to the ZDiscovery for which you set up the SSO. For more information, see [Microsoft Entra My Apps](/azure/active-directory/manage-apps/end-user-experiences#azure-ad-my-apps).

## Related content

Once you configure ZDiscovery you can enforce session control, which protects exfiltration and infiltration of your organization’s sensitive data in real time. Session control extends from Conditional Access. [Learn how to enforce session control with Microsoft Cloud App Security](/cloud-app-security/proxy-deployment-aad).
