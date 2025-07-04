---
title: Configure 360 Online for Single sign-on with Microsoft Entra ID
description: Learn how to configure single sign-on between Microsoft Entra ID and 360 Online.

author: nguhiu
manager: mwongerapk
ms.reviewer: celested
ms.service: entra-id
ms.subservice: saas-apps

ms.topic: how-to
ms.date: 03/25/2025
ms.author: gideonkiratu

# Customer intent: As an IT administrator, I want to learn how to configure single sign-on between Microsoft Entra ID and 360 Online so that I can control who has access to 360 Online, enable automatic sign-in with Microsoft Entra accounts, and manage my accounts in one central location.
---
# Configure 360 Online for Single sign-on with Microsoft Entra ID

In this article,  you learn how to integrate 360 Online with Microsoft Entra ID. When you integrate 360 Online with Microsoft Entra ID, you can:

* Control in Microsoft Entra ID who has access to 360 Online.
* Enable your users to be automatically signed-in to 360 Online with their Microsoft Entra accounts.
* Manage your accounts in one central location.

## Prerequisites

The scenario outlined in this article assumes that you already have the following prerequisites:

[!INCLUDE [common-prerequisites.md](~/identity/saas-apps/includes/common-prerequisites.md)]
* 360 Online single sign-on (SSO) enabled subscription.

## Scenario description

In this article,  you configure and test Microsoft Entra single sign-on in a test environment.

* 360 Online supports **SP** initiated SSO.

> [!NOTE]
> Identifier of this application is a fixed string value so only one instance can be configured in one tenant.

## Add 360 Online from the gallery

To configure the integration of 360 Online into Microsoft Entra ID, you need to add 360 Online from the gallery to your list of managed SaaS apps.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](~/identity/role-based-access-control/permissions-reference.md#cloud-application-administrator).
1. Browse to **Entra ID** > **Enterprise apps** > **New application**.
1. In the **Add from the gallery** section, type **360 Online** in the search box.
1. Select **360 Online** from results panel and then add the app. Wait a few seconds while the app is added to your tenant.

 [!INCLUDE [sso-wizard.md](~/identity/saas-apps/includes/sso-wizard.md)]

<a name='configure-and-test-azure-ad-sso-for-360-online'></a>

## Configure and test Microsoft Entra SSO for 360 Online

Configure and test Microsoft Entra SSO with 360 Online using a test user called **B.Simon**. For SSO to work, you need to establish a link relationship between a Microsoft Entra user and the related user in 360 Online.

To configure and test Microsoft Entra SSO with 360 Online, perform the following steps:

1. **[Configure Microsoft Entra SSO](#configure-azure-ad-sso)** - to enable your users to use this feature.
    1. **Create a Microsoft Entra test user** - to test Microsoft Entra single sign-on with B.Simon.
    1. **Assign the Microsoft Entra test user** - to enable B.Simon to use Microsoft Entra single sign-on.
1. **[Configure 360 Online SSO](#configure-360-online-sso)** - to configure the single sign-on settings on application side.
    1. **[Create 360 Online test user](#create-360-online-test-user)** - to have a counterpart of B.Simon in 360 Online that's linked to the Microsoft Entra representation of user.
1. **[Test SSO](#test-sso)** - to verify whether the configuration works.

<a name='configure-azure-ad-sso'></a>

## Configure Microsoft Entra SSO

Follow these steps to enable Microsoft Entra SSO.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](~/identity/role-based-access-control/permissions-reference.md#cloud-application-administrator).
1. Browse to **Entra ID** > **Enterprise apps** > **360 Online** > **Single sign-on**.
1. On the **Select a single sign-on method** page, select **SAML**.
1. On the **Set up single sign-on with SAML** page, select the pencil icon for **Basic SAML Configuration** to edit the settings.

   ![Edit Basic SAML Configuration](common/edit-urls.png)

1. On the **Basic SAML Configuration** section, perform the following step:

    In the **Sign-on URL** text box, type a URL using the following pattern:
    `https://<company name>.public360online.com`

    > [!NOTE]
    > The value isn't  real. Update the value with the actual Sign-On URL. Contact [360 Online Client support team](mailto:360online@software-innovation.com) to get the value. You can also refer to the patterns shown in the **Basic SAML Configuration** section.

1. On the **Set up Single Sign-On with SAML** page, in the **SAML Signing Certificate** section, select **Download** to download the **Federation Metadata XML** from the given options as per your requirement and save it on your computer.

    ![The Certificate download link](common/metadataxml.png)

1. On the **Set up 360 Online** section, copy the appropriate URL(s) as per your requirement.

    ![Copy configuration URLs](common/copy-configuration-urls.png)

<a name='create-an-azure-ad-test-user'></a>

[!INCLUDE [create-assign-users-sso.md](~/identity/saas-apps/includes/create-assign-users-sso.md)]

## Configure 360 Online SSO

To configure single sign-on on **360 Online** side, you need to send the downloaded **Metadata XML** and appropriate copied URLs from the application configuration to [360 Online support team](mailto:360online@software-innovation.com). They set this setting to have the SAML SSO connection set properly on both sides.

### Create 360 Online test user

In this section, you create a user called Britta Simon in 360 Online. Work with [360 Online support team](mailto:360online@software-innovation.com) to add the users in the 360 Online platform. Users must be created and activated before you use single sign-on.

## Test SSO

In this section, you test your Microsoft Entra single sign-on configuration with following options. 

* Select **Test this application**, this option redirects to 360 Online Sign-on URL where you can initiate the login flow. 

* Go to 360 Online Sign-on URL directly and initiate the login flow from there.

* You can use Microsoft My Apps. When you select the 360 Online tile in the My Apps, this option redirects to 360 Online Sign-on URL. For more information about the My Apps, see [Introduction to the My Apps](https://support.microsoft.com/account-billing/sign-in-and-start-apps-from-the-my-apps-portal-2f3b1bae-0e5a-4a86-a33e-876fbd2a4510).

## Related content

Once you configure 360 Online you can enforce session control, which protects exfiltration and infiltration of your organization’s sensitive data in real time. Session control extends from Conditional Access. [Learn how to enforce session control with Microsoft Defender for Cloud Apps](/cloud-app-security/proxy-deployment-aad).
