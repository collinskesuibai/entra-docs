---
title: Configure Front for Single sign-on with Microsoft Entra ID
description: Learn how to configure single sign-on between Microsoft Entra ID and Front.
author: nguhiu
manager: mwongerapk
ms.reviewer: celested
ms.service: entra-id
ms.subservice: saas-apps
ms.topic: how-to
ms.date: 03/25/2025
ms.author: gideonkiratu
ms.custom: sfi-image-nochange
# Customer intent: As an IT administrator, I want to learn how to configure single sign-on between Microsoft Entra ID and Front so that I can control who has access to Front, enable automatic sign-in with Microsoft Entra accounts, and manage my accounts in one central location.
---
# Configure Front for Single sign-on with Microsoft Entra ID

In this article,  you learn how to integrate Front with Microsoft Entra ID. When you integrate Front with Microsoft Entra ID, you can:

* Control in Microsoft Entra ID who has access to Front.
* Enable your users to be automatically signed-in to Front with their Microsoft Entra accounts.
* Manage your accounts in one central location.

## Prerequisites

The scenario outlined in this article assumes that you already have the following prerequisites:

[!INCLUDE [common-prerequisites.md](~/identity/saas-apps/includes/common-prerequisites.md)]
* Front single sign-on (SSO) enabled subscription.

## Scenario description

In this article,  you configure and test Microsoft Entra single sign-on in a test environment.

* Front supports **IDP** initiated SSO.

## Adding Front from the gallery

To configure the integration of Front into Microsoft Entra ID, you need to add Front from the gallery to your list of managed SaaS apps.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](~/identity/role-based-access-control/permissions-reference.md#cloud-application-administrator).
1. Browse to **Entra ID** > **Enterprise apps** > **New application**.
1. In the **Add from the gallery** section, type **Front** in the search box.
1. Select **Front** from results panel and then add the app. Wait a few seconds while the app is added to your tenant.

 [!INCLUDE [sso-wizard.md](~/identity/saas-apps/includes/sso-wizard.md)]

<a name='configure-and-test-azure-ad-sso-for-front'></a>

## Configure and test Microsoft Entra SSO for Front

Configure and test Microsoft Entra SSO with Front using a test user called **B.Simon**. For SSO to work, you need to establish a link relationship between a Microsoft Entra user and the related user in Front.

To configure and test Microsoft Entra SSO with Front, perform the following steps:

1. **[Configure Microsoft Entra SSO](#configure-azure-ad-sso)** - to enable your users to use this feature.
    1. **Create a Microsoft Entra test user** - to test Microsoft Entra single sign-on with B.Simon.
    1. **Assign the Microsoft Entra test user** - to enable B.Simon to use Microsoft Entra single sign-on.
1. **[Configure Front SSO](#configure-front-sso)** - to configure the single sign-on settings on application side.
    1. **[Create Front test user](#create-front-test-user)** - to have a counterpart of B.Simon in Front that's linked to the Microsoft Entra representation of user.
1. **[Test SSO](#test-sso)** - to verify whether the configuration works.

<a name='configure-azure-ad-sso'></a>

## Configure Microsoft Entra SSO

Follow these steps to enable Microsoft Entra SSO.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](~/identity/role-based-access-control/permissions-reference.md#cloud-application-administrator).
1. Browse to **Entra ID** > **Enterprise apps** > **Front** > **Single sign-on**.
1. On the **Select a single sign-on method** page, select **SAML**.
1. On the **Set up single sign-on with SAML** page, select the pencil icon for **Basic SAML Configuration** to edit the settings.

   ![Edit Basic SAML Configuration](common/edit-urls.png)

1. On the **Set up Single Sign-On with SAML** page, perform the following steps:

    a. In the **Identifier** text box, type a URL using the following pattern:
    `https://<companyname>.frontapp.com`

    b. In the **Reply URL** text box, type a URL using the following pattern:
    `https://<companyname>.frontapp.com/sso/saml/callback`

	> [!NOTE]
	> These values aren't real. Update these values with the actual Identifier and Reply URL. Contact [Front Client support team](mailto:support@frontapp.com) to get these values. You can also refer to the patterns shown in the **Basic SAML Configuration** section.

1. On the **Set up Single Sign-On with SAML** page, in the **SAML Signing Certificate** section, select **Download** to download the **Certificate (Base64)** from the given options as per your requirement and save it on your computer.

	![The Certificate download link](common/certificatebase64.png)

1. On the **Set up Front** section, copy the appropriate URL(s) as per your requirement.

	![Copy configuration URLs](common/copy-configuration-urls.png)

<a name='create-an-azure-ad-test-user'></a>

[!INCLUDE [create-assign-users-sso.md](~/identity/saas-apps/includes/create-assign-users-sso.md)]

## Configure Front SSO

1. Log in to your Front website as an administrator.

2. Go to the **settings** and select the**Preferences**.

3. Perform the following steps in the **Company preferences** page.
   
    ![Screenshot that shows the "Company preferences" section with the "Single Sign On" link selected.](./media/front-tutorial/single-sign-on.png)

    a. Select **Single Sign On** on the left side navigation.

    b. Select **SAML** in the drop-down list of **Single Sign On**.

    c. In the **Entry Point** textbox enter the value of **Login URL** which you copied previously.

    d. Select the **Requested authentication context** type as **Disabled**.

    e. Open your downloaded **Certificate(Base64)** file in notepad, copy the content of it into your clipboard, and then paste it to the **Signing certificate** textbox.

7. On the **Service provider settings** section, perform the following steps:

	![Configure Single Sign-On On App side](./media/front-tutorial/service-provider.png)

	a. Copy the value of **Entity ID** and paste it into the **Identifier** textbox in **Front Domain and URLs** section in Azure portal.

	b. Copy the value of **ACS URL** and paste it into the **Reply URL** textbox in **Front Domain and URLs** section in Azure portal.
	
8. Select **Save** button.


### Create Front test user

In this section, you create a user called Britta Simon in Front. Work with [Front Client support team](mailto:support@frontapp.com) to add the users in the Front platform. Users must be created and activated before you use single sign-on.

## Test SSO 

In this section, you test your Microsoft Entra single sign-on configuration with following options.

* Select **Test this application**, and you should be automatically signed in to the Front for which you set up the SSO

* You can use Microsoft My Apps. When you select the Front tile in the My Apps, you should be automatically signed in to the Front for which you set up the SSO. For more information about the My Apps, see [Introduction to the My Apps](https://support.microsoft.com/account-billing/sign-in-and-start-apps-from-the-my-apps-portal-2f3b1bae-0e5a-4a86-a33e-876fbd2a4510).

## Related content

Once you configure Front you can enforce session control, which protects exfiltration and infiltration of your organization’s sensitive data in real time. Session control extends from Conditional Access. [Learn how to enforce session control with Microsoft Defender for Cloud Apps](/cloud-app-security/proxy-deployment-any-app).
