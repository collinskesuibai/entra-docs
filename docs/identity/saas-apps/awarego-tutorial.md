---
title: Configure AwareGo for Single sign-on with Microsoft Entra ID
description: Learn how to configure single sign-on between Microsoft Entra ID and AwareGo.

author: nguhiu
manager: mwongerapk
ms.reviewer: CelesteDG
ms.service: entra-id
ms.subservice: saas-apps

ms.topic: how-to
ms.date: 03/25/2025
ms.author: gideonkiratu


# Customer intent: As an IT administrator, I want to learn how to configure single sign-on between Microsoft Entra ID and AwareGo so that I can control who has access to AwareGo, enable automatic sign-in with Microsoft Entra accounts, and manage my accounts in one central location.
---

# Configure AwareGo for Single sign-on with Microsoft Entra ID

In this article,  you learn how to integrate AwareGo with Microsoft Entra ID. When you integrate AwareGo with Microsoft Entra ID, you can:

* Control in Microsoft Entra ID who has access to AwareGo.
* Enable your users to be automatically signed in to AwareGo with their Microsoft Entra accounts.
* Manage your accounts in one central location, the Azure portal.

## Prerequisites

The scenario outlined in this article assumes that you already have the following prerequisites:

[!INCLUDE [common-prerequisites.md](~/identity/saas-apps/includes/common-prerequisites.md)]
* An AwareGo single sign-on (SSO)-enabled subscription.

## Scenario description

In this article,  you configure and test Microsoft Entra SSO in a test environment. AwareGo supports a service provider (SP)-initiated SSO.


## Adding AwareGo from the gallery

To configure the integration of AwareGo into Microsoft Entra ID, you need to add AwareGo from the gallery to your list of managed software as a service (SaaS) apps.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](~/identity/role-based-access-control/permissions-reference.md#cloud-application-administrator).
1. Browse to **Entra ID** > **Enterprise apps** > **New application**.
1. In the **Add from the gallery** section, type **AwareGo** in the search box.
1. In the results pane, select **AwareGo**, and then add the app. In a few seconds, the app is added to your tenant.


<a name='configure-and-test-azure-ad-sso-for-awarego'></a>

## Configure and test Microsoft Entra SSO for AwareGo

Configure and test Microsoft Entra SSO with AwareGo by using a test user called **B.Simon**. For SSO to work, you need to establish a link relationship between a Microsoft Entra user and the related user in AwareGo.

To configure and test Microsoft Entra SSO with AwareGo, do the following:

1. **[Configure Microsoft Entra SSO](#configure-azure-ad-sso)** to enable your users to use this feature.  

    a. **Create a Microsoft Entra test user** to test Microsoft Entra single sign-on with user B.Simon.  
    b. **Assign the Microsoft Entra test user** to enable user B.Simon to use Microsoft Entra single sign-on.  

1. **[Configure AwareGo SSO](#configure-awarego-sso)** to configure the single sign-on settings on the application side.

    a. **[Create an AwareGo test user](#create-an-awarego-test-user)** to have a counterpart of B.Simon in AwareGo that's linked to the Microsoft Entra representation of the user.  
    b. **[Test SSO](#test-sso)** to verify that the configuration works.

<a name='configure-azure-ad-sso'></a>

## Configure Microsoft Entra SSO

To enable Microsoft Entra SSO in the Azure portal, do the following:

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](~/identity/role-based-access-control/permissions-reference.md#cloud-application-administrator).
1. Browse to **Entra ID** > **Enterprise apps** > **AwareGo** application integration page, under **Manage**, select **single sign-on**.
1. On the **Select a single sign-on method** page, select **SAML**.
1. To edit the settings, on the **Set up Single Sign-On with SAML** pane, select the **Edit** button.

   ![Screenshot of the Edit button for Basic SAML Configuration.](common/edit-urls.png)

1. On the edit pane, under **Basic SAML Configuration**, do the following:

    a. In the **Sign on URL** box, enter either of the following URLs:

    * `https://lms.awarego.com/auth/signin/` 
    * `https://my.awarego.com/auth/signin/`

    b. In the **Identifier (Entity ID)** box, enter a URL in the following format: `https://<SUBDOMAIN>.awarego.com`

    c. In the **Reply URL** box, enter a URL in the following format: `https://<SUBDOMAIN>.awarego.com/auth/sso/callback`

	> [!NOTE]
	> The preceding values aren't real. Update them with the actual identifier and reply URLs. To obtain the values, contact the [AwareGo client support team](mailto:support@awarego.com). You can also refer to the examples in the **Basic SAML Configuration** section.

1. On the **Set up single sign-on with SAML** page, in the **SAML Signing Certificate** section, next to **Certificate (Base64)**, select **Download** to download the certificate and save it to your computer.

	![Screenshot of the certificate "Download" link on the SAML Signing Certificate pane.](common/certificatebase64.png)

1. In the **Set up AwareGo** section, copy one or more URLs, depending on your requirements.

	![Screenshot of the "Set up AwareGo" pane for copying configuration URLs.](common/copy-configuration-urls.png)

<a name='create-an-azure-ad-test-user'></a>

[!INCLUDE [create-assign-users-sso.md](~/identity/saas-apps/includes/create-assign-users-sso.md)]

## Configure AwareGo SSO

To configure single sign-on on the **AwareGo** side, send the **Certificate (Base64)** certificate you downloaded earlier and the URLs you copied earlier to the [AwareGo support team](mailto:support@awarego.com). The support team creates this setting to establish the SAML SSO connection properly on both sides.

### Create an AwareGo test user

In this section, you create a user called Britta Simon in AwareGo. Work with the [AwareGo support team](mailto:support@awarego.com) to add the users in the AwareGo platform. You must create and activate the users before you can use single sign-on.

## Test SSO 

In this section, you can test your Microsoft Entra single sign-on configuration by doing any of the following: 

* In the Azure portal, select **Test this application**. This redirects you to the AwareGo sign-in page, where you can initiate the sign-in flow. 

* Go to the AwareGo sign-in page directly, and initiate the sign-in flow from there.

* Go to Microsoft My Apps. When you select the **AwareGo** tile in My Apps, you're redirected to the AwareGo sign-in page. For more information, see [Sign in and start apps from the My Apps portal](https://support.microsoft.com/account-billing/sign-in-and-start-apps-from-the-my-apps-portal-2f3b1bae-0e5a-4a86-a33e-876fbd2a4510).


## Related content

After you've configured AwareGo, you can enforce session control, which protects exfiltration and infiltration of your organization’s sensitive data in real time. Session control extends from Conditional Access App Control. For more information, see [Learn how to enforce session control with Microsoft Defender for Cloud Apps](/cloud-app-security/proxy-deployment-any-app).
