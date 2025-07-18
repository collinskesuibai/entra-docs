---
title: Configure Ariba for Single sign-on with Microsoft Entra ID
description: Learn how to configure single sign-on between Microsoft Entra ID and Ariba.
author: nguhiu
manager: mwongerapk
ms.reviewer: celested
ms.service: entra-id
ms.subservice: saas-apps
ms.topic: how-to
ms.date: 03/25/2025
ms.author: gideonkiratu
ms.custom: sfi-image-nochange
# Customer intent: As an IT administrator, I want to learn how to configure single sign-on between Microsoft Entra ID and Ariba so that I can control who has access to Ariba, enable automatic sign-in with Microsoft Entra accounts, and manage my accounts in one central location.
---
# Configure Ariba for Single sign-on with Microsoft Entra ID

In this article,  you learn how to integrate Ariba with Microsoft Entra ID. When you integrate Ariba with Microsoft Entra ID, you can:

* Control in Microsoft Entra ID who has access to Ariba.
* Enable your users to be automatically signed-in to Ariba with their Microsoft Entra accounts.
* Manage your accounts in one central location.

## Prerequisites

The scenario outlined in this article assumes that you already have the following prerequisites:

[!INCLUDE [common-prerequisites.md](~/identity/saas-apps/includes/common-prerequisites.md)]
* Ariba single sign-on (SSO) enabled subscription.

## Scenario description

In this article,  you configure and test Microsoft Entra single sign-on in a test environment.

* Ariba supports **SP** initiated SSO

## Add Ariba from the gallery

To configure the integration of Ariba into Microsoft Entra ID, you need to add Ariba from the gallery to your list of managed SaaS apps.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](~/identity/role-based-access-control/permissions-reference.md#cloud-application-administrator).
1. Browse to **Entra ID** > **Enterprise apps** > **New application**.
1. In the **Add from the gallery** section, type **Ariba** in the search box.
1. Select **Ariba** from results panel and then add the app. Wait a few seconds while the app is added to your tenant.

 [!INCLUDE [sso-wizard.md](~/identity/saas-apps/includes/sso-wizard.md)]

<a name='configure-and-test-azure-ad-sso-for-ariba'></a>

## Configure and test Microsoft Entra SSO for Ariba

Configure and test Microsoft Entra SSO with Ariba using a test user called **B.Simon**. For SSO to work, you need to establish a link relationship between a Microsoft Entra user and the related user in Ariba.

To configure and test Microsoft Entra SSO with Ariba, perform the following steps:

1. **[Configure Microsoft Entra SSO](#configure-azure-ad-sso)** - to enable your users to use this feature.
    1. **Create a Microsoft Entra test user** - to test Microsoft Entra single sign-on with B.Simon.
    1. **Assign the Microsoft Entra test user** - to enable B.Simon to use Microsoft Entra single sign-on.
1. **[Configure Ariba SSO](#configure-ariba-sso)** - to configure the single sign-on settings on application side.
    1. **[Create Ariba test user](#create-ariba-test-user)** - to have a counterpart of B.Simon in Ariba that's linked to the Microsoft Entra representation of user.
1. **[Test SSO](#test-sso)** - to verify whether the configuration works.

<a name='configure-azure-ad-sso'></a>

### Configure Microsoft Entra SSO

Follow these steps to enable Microsoft Entra SSO.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](~/identity/role-based-access-control/permissions-reference.md#cloud-application-administrator).
1. Browse to **Entra ID** > **Enterprise apps** > **Ariba** > **Single sign-on**.
1. On the **Select a single sign-on method** page, select **SAML**.
1. On the **Set up single sign-on with SAML** page, select the pencil icon for **Basic SAML Configuration** to edit the settings.

   ![Edit Basic SAML Configuration](common/edit-urls.png)

1. On the **Basic SAML Configuration** section, perform the following steps:

    ![Ariba Domain and URLs single sign-on information](common/sp-identifier.png)

	a. In the **Sign on URL** text box, type a URL using the following pattern:
    
    ```http
    https://<subdomain>.sourcing.ariba.com
    https://<subdomain>.supplier.ariba.com
    ```

    b. In the **Identifier (Entity ID)** text box, type a URL using the following pattern:
    `http://<subdomain>.procurement-2.ariba.com`

    c. For **Reply URL**, enter one of the following URL pattern:

	| Reply URL|
	|----------|
    | `https://<subdomain>.ariba.com/CUSTOM_URL` |
	| `https://<subdomain>.procurement-eu.ariba.com/CUSTOM_URL` |
	| `https://<subdomain>.procurement-eu.ariba.com` |
	| `https://<subdomain>.procurement-2.ariba.com` |
	| `https://<subdomain>.procurement-2.ariba.com/CUSTOM_URL` |

	> [!NOTE]
	> These values aren't real. Update these values with the actual Sign-on URL, Identifier and Reply URL. Here we suggest you to use the unique value of string in the Identifier. Contact Ariba Client support team at **1-866-218-2155** to get these values.. You can also refer to the patterns shown in the **Basic SAML Configuration** section.

1. On the **Set up Single Sign-On with SAML** page, in the **SAML Signing Certificate** section, select **Download** to download the **Certificate (Base64)** from the given options as per your requirement and save it on your computer.

	![The Certificate download link](common/certificatebase64.png)

<a name='create-an-azure-ad-test-user'></a>

[!INCLUDE [create-assign-users-sso.md](~/identity/saas-apps/includes/create-assign-users-sso.md)]

## Configure Ariba SSO

To get SSO configured for your application, call Ariba support team on **1-866-218-2155** and they'll assist you further on how to provide them the downloaded **Certificate (Base64**) file.

### Create Ariba test user

In this section, you create a user called Britta Simon in Ariba. Work with Ariba support team at **1-866-218-2155** to add the users in the Ariba platform. Users must be created and activated before you use single sign-on.

## Test SSO 

In this section, you test your Microsoft Entra single sign-on configuration with following options. 

* Select **Test this application**, this option redirects to Ariba Sign-on URL where you can initiate the login flow. 

* Go to Ariba Sign-on URL directly and initiate the login flow from there.

* You can use Microsoft My Apps. When you select the Ariba tile in the My Apps, this option redirects to Ariba Sign-on URL. For more information about the My Apps, see [Introduction to the My Apps](https://support.microsoft.com/account-billing/sign-in-and-start-apps-from-the-my-apps-portal-2f3b1bae-0e5a-4a86-a33e-876fbd2a4510).

## Related content

Once you configure Ariba you can enforce session control, which protects exfiltration and infiltration of your organization’s sensitive data in real time. Session control extends from Conditional Access. [Learn how to enforce session control with Microsoft Defender for Cloud Apps](/cloud-app-security/proxy-deployment-any-app).
