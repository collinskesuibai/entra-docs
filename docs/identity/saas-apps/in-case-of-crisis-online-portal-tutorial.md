---
title: Configure In Case of Crisis - Online Portal for Single sign-on with Microsoft Entra ID
description: Learn how to configure single sign-on between Microsoft Entra ID and In Case of Crisis - Online Portal.

author: nguhiu
manager: mwongerapk
ms.reviewer: celested
ms.service: entra-id
ms.subservice: saas-apps

ms.topic: how-to
ms.date: 03/25/2025
ms.author: gideonkiratu

# Customer intent: As an IT administrator, I want to learn how to configure single sign-on between Microsoft Entra ID and In Case of Crisis - Online Portal so that I can control who has access to In Case of Crisis - Online Portal, enable automatic sign-in with Microsoft Entra accounts, and manage my accounts in one central location.
---

# Configure In Case of Crisis - Online Portal for Single sign-on with Microsoft Entra ID

In this article,  you learn how to integrate In Case of Crisis - Online Portal with Microsoft Entra ID. When you integrate In Case of Crisis - Online Portal with Microsoft Entra ID, you can:

* Control in Microsoft Entra ID who has access to In Case of Crisis - Online Portal.
* Enable your users to be automatically signed-in to In Case of Crisis - Online Portal with their Microsoft Entra accounts.
* Manage your accounts in one central location.

To learn more about SaaS app integration with Microsoft Entra ID, see [What is application access and single sign-on with Microsoft Entra ID](~/identity/enterprise-apps/what-is-single-sign-on.md).

## Prerequisites

The scenario outlined in this article assumes that you already have the following prerequisites:

[!INCLUDE [common-prerequisites.md](~/identity/saas-apps/includes/common-prerequisites.md)]
* In Case of Crisis - Online Portal single sign-on (SSO) enabled subscription.

## Scenario description

In this article,  you configure and test Microsoft Entra SSO in a test environment.

* In Case of Crisis - Online Portal supports **IDP** initiated SSO
* Once you configure the In Case of Crisis - Online Portal you can enforce session controls, which protect exfiltration and infiltration of your organization’s sensitive data in real-time. Session controls extend from Conditional Access. [Learn how to enforce session control with Microsoft Defender for Cloud Apps](/cloud-app-security/proxy-deployment-any-app).

## Adding In Case of Crisis - Online Portal from the gallery

To configure the integration of In Case of Crisis - Online Portal into Microsoft Entra ID, you need to add In Case of Crisis - Online Portal from the gallery to your list of managed SaaS apps.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](~/identity/role-based-access-control/permissions-reference.md#cloud-application-administrator).
1. Browse to **Entra ID** > **Enterprise apps** > **New application**.
1. In the **Add from the gallery** section, type **In Case of Crisis - Online Portal** in the search box.
1. Select **In Case of Crisis - Online Portal** from results panel and then add the app. Wait a few seconds while the app is added to your tenant.

 [!INCLUDE [sso-wizard.md](~/identity/saas-apps/includes/sso-wizard.md)]

<a name='configure-and-test-azure-ad-single-sign-on-for-in-case-of-crisis---online-portal'></a>

## Configure and test Microsoft Entra single sign-on for In Case of Crisis - Online Portal

Configure and test Microsoft Entra SSO with In Case of Crisis - Online Portal using a test user called **B.Simon**. For SSO to work, you need to establish a link relationship between a Microsoft Entra user and the related user in In Case of Crisis - Online Portal.

To configure and test Microsoft Entra SSO with In Case of Crisis - Online Portal, complete the following building blocks:

1. **[Configure Microsoft Entra SSO](#configure-azure-ad-sso)** - to enable your users to use this feature.
    * **Create a Microsoft Entra test user** - to test Microsoft Entra single sign-on with B.Simon.
    * **Assign the Microsoft Entra test user** - to enable B.Simon to use Microsoft Entra single sign-on.
1. **[Configure In Case of Crisis Online Portal SSO](#configure-in-case-of-crisis-online-portal-sso)** - to configure the single sign-on settings on application side.
    * **[Create In Case of Crisis Online Portal test user](#create-in-case-of-crisis-online-portal-test-user)** - to have a counterpart of B.Simon in In Case of Crisis - Online Portal that's linked to the Microsoft Entra representation of user.
1. **[Test SSO](#test-sso)** - to verify whether the configuration works.

<a name='configure-azure-ad-sso'></a>

## Configure Microsoft Entra SSO

Follow these steps to enable Microsoft Entra SSO.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](~/identity/role-based-access-control/permissions-reference.md#cloud-application-administrator).
1. Browse to **Entra ID** > **Enterprise apps** > **In Case of Crisis - Online Portal** > **Single sign-on**.
1. On the **Select a single sign-on method** page, select **SAML**.
1. On the **Set up single sign-on with SAML** page, select the edit/pen icon for **Basic SAML Configuration** to edit the settings.

   ![Screenshot shows to edit Basic SAML Configuration.](common/edit-urls.png)

1. On the **Basic SAML Configuration** section, the application is pre-configured and the necessary URLs are already pre-populated with Azure. The user needs to save the configuration by selecting the **Save** button.


1. On the **Set up single sign-on with SAML** page, in the **SAML Signing Certificate** section,  find **Certificate (Base64)** and select **Download** to download the certificate and save it on your computer.

	![Screenshot shows the Certificate download link.](common/certificatebase64.png "Certificate")

1. On the **Set up In Case of Crisis - Online Portal** section, copy the appropriate URL(s) based on your requirement.

   > [!NOTE]
   > On the Properties page, please send us the User Access URL. This are used in the In Case of Crisis portal.
   
<a name='create-an-azure-ad-test-user'></a>

[!INCLUDE [create-assign-users-sso.md](~/identity/saas-apps/includes/create-assign-users-sso.md)]

## Configure In Case of Crisis Online Portal SSO

To configure single sign-on on **In Case of Crisis - Online Portal** side, you need to send the downloaded **Certificate (Base64)** and appropriate copied URLs from the application configuration to [In Case of Crisis - Online Portal support team](mailto:support@rockdovesolutions.com). They set this setting to have the SAML SSO connection set properly on both sides.

### Create In Case of Crisis Online Portal test user

In this section, you create a user called B.Simon in In Case of Crisis - Online Portal. Work with [In Case of Crisis - Online Portal support team](mailto:support@rockdovesolutions.com) to add the users in the In Case of Crisis - Online Portal platform. Users must be created and activated before you use single sign-on.

## Test SSO 

In this section, you test your Microsoft Entra single sign-on configuration using the Access Panel.

When you select the In Case of Crisis - Online Portal tile in the Access Panel, you should be automatically signed in to the In Case of Crisis - Online Portal for which you set up SSO. For more information about the Access Panel, see [Introduction to the Access Panel](https://support.microsoft.com/account-billing/sign-in-and-start-apps-from-the-my-apps-portal-2f3b1bae-0e5a-4a86-a33e-876fbd2a4510).

## Additional resources

- [List of articles on How to Integrate SaaS Apps with Microsoft Entra ID](./tutorial-list.md)

- [What is application access and single sign-on with Microsoft Entra ID?](~/identity/enterprise-apps/what-is-single-sign-on.md)

- [What is Conditional Access in Microsoft Entra ID?](~/identity/conditional-access/overview.md)

- [What is session control in Microsoft Defender for Cloud Apps?](/cloud-app-security/proxy-intro-aad)
