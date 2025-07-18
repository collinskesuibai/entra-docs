---
title: Configure Settling music for Single sign-on with Microsoft Entra ID
description: Learn how to configure single sign-on between Microsoft Entra ID and Settling music.

author: nguhiu
manager: mwongerapk
ms.reviewer: celested
ms.service: entra-id
ms.subservice: saas-apps

ms.topic: how-to
ms.date: 05/20/2025
ms.author: gideonkiratu

# Customer intent: As an IT administrator, I want to learn how to configure single sign-on between Microsoft Entra ID and Settling music so that I can control who has access to Settling music, enable automatic sign-in with Microsoft Entra accounts, and manage my accounts in one central location.
---
# Configure Settling music for Single sign-on with Microsoft Entra ID

In this article,  you learn how to integrate Settling music with Microsoft Entra ID. When you integrate Settling music with Microsoft Entra ID, you can:

* Control in Microsoft Entra ID who has access to Settling music.
* Enable your users to be automatically signed-in to Settling music with their Microsoft Entra accounts.
* Manage your accounts in one central location.

## Prerequisites
The scenario outlined in this article assumes that you already have the following prerequisites:

[!INCLUDE [common-prerequisites.md](~/identity/saas-apps/includes/common-prerequisites.md)]
* Settling music single sign-on enabled subscription.

## Scenario description

In this article,  you configure and test Microsoft Entra single sign-on in a test environment.

* Settling music supports **SP** initiated SSO.

## Add Settling music from the gallery

To configure the integration of Settling music into Microsoft Entra ID, you need to add Settling music from the gallery to your list of managed SaaS apps.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](~/identity/role-based-access-control/permissions-reference.md#cloud-application-administrator).
1. Browse to **Entra ID** > **Enterprise apps** > **New application**.
1. In the **Add from the gallery** section, type **Settling music** in the search box.
1. Select **Settling music** from results panel and then add the app. Wait a few seconds while the app is added to your tenant.

 Alternatively, you can also use the [Enterprise App Configuration Wizard](https://portal.office.com/AdminPortal/home?Q=Docs#/azureadappintegration). In this wizard, you can add an application to your tenant, add users/groups to the app, assign roles, and walk through the SSO configuration as well. [Learn more about Microsoft 365 wizards.](/microsoft-365/admin/misc/azure-ad-setup-guides)

<a name='configure-and-test-azure-ad-sso-for-settling-music'></a>

## Configure and test Microsoft Entra SSO for Settling music

Configure and test Microsoft Entra SSO with Settling music using a test user called **B.Simon**. For SSO to work, you need to establish a link relationship between a Microsoft Entra user and the related user in Settling music.

To configure and test Microsoft Entra SSO with Settling music, perform the following steps:

1. **[Configure Microsoft Entra SSO](#configure-azure-ad-sso)** - to enable your users to use this feature.
    1. **Create a Microsoft Entra test user** - to test Microsoft Entra single sign-on with B.Simon.
    1. **Assign the Microsoft Entra test user** - to enable B.Simon to use Microsoft Entra single sign-on.
1. **[Configure Settling music SSO](#configure-settling-music-sso)** - to configure the single sign-on settings on application side.
    1. **[Create Settling music test user](#create-settling-music-test-user)** - to have a counterpart of B.Simon in Settling music that's linked to the Microsoft Entra representation of user.
1. **[Test SSO](#test-sso)** - to verify whether the configuration works.

<a name='configure-azure-ad-sso'></a>

## Configure Microsoft Entra SSO

Follow these steps to enable Microsoft Entra SSO.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](~/identity/role-based-access-control/permissions-reference.md#cloud-application-administrator).
1. Browse to **Entra ID** > **Enterprise apps** > **Settling music** > **Single sign-on**.
1. On the **Select a single sign-on method** page, select **SAML**.
1. On the **Set up single sign-on with SAML** page, select the pencil icon for **Basic SAML Configuration** to edit the settings.

   ![Edit Basic SAML Configuration](common/edit-urls.png)

1. On the **Basic SAML Configuration** section, perform the following steps:

    a. In the **Identifier (Entity ID)** text box, type a URL using the following pattern:
    `https://<SUBDOMAIN>.rakurakuseisan.jp/<USERACCOUNT>/`

	b. In the **Sign on URL** text box, type a URL using the following pattern:
    `https://<SUBDOMAIN>.rakurakuseisan.jp/<USERACCOUNT>/`

	> [!NOTE]
	> These values aren't real. Update these values with the actual Identifier and Sign on URL. Contact [Settling music Client support team](https://rakurakuseisan.jp/) to get these values. You can also refer to the patterns shown in the **Basic SAML Configuration** section.

1. On the **Set up Single Sign-On with SAML** page, in the **SAML Signing Certificate** section, select **Download** to download the **Certificate (Base64)** from the given options as per your requirement and save it on your computer.

	![The Certificate download link](common/certificatebase64.png)

1. On the **Set up Settling music** section, copy the appropriate URL(s) as per your requirement.

	![Copy configuration URLs](./media/settlingmusic-tutorial/copy-configuration-urls.png)

	Use the below URL for the Logout URL.

	```text
    Logout URL https://login.microsoftonline.com/common/wsfederation?wa=wsignout1.0
    ```

<a name='create-an-azure-ad-test-user'></a>

[!INCLUDE [create-assign-users-sso.md](~/identity/saas-apps/includes/create-assign-users-sso.md)]

## Configure Settling music SSO

1. In a different web browser window, sign in to Settling music as a Security Administrator.

1. On top of the page, select **management** tab.

	![Settling music step1](./media/settlingmusic-tutorial/menu.png)

1. Select  **System setting** tab.

	![Settling music step2](./media/settlingmusic-tutorial/settings.png)

1. Switch to **Security** tab.

	![Settling music step3](./media/settlingmusic-tutorial/security.png)

1. On the **Single sign-on setting** section, perform the following steps:

	![Settling music step5](./media/settlingmusic-tutorial/certificate.png)

	a. Select **To enable**.

	b. In the **Login URL of the ID provider** textbox, paste the value of **Login URL**..

	c. In the **ID provider logout URL** textbox, paste the value of **Logout URL** which is explained in [Configure Microsoft Entra SSO](#configure-azure-ad-sso) section.

	d. Select **Choose File** to upload the **Certificate (Base64)** which you have downloaded form Azure portal.

	e. Select the **Save** button.

### Create Settling music test user

In this section, you create a user called Britta Simon in Settling music. Work with [Settling music Client support team](https://rakurakuseisan.jp/) to add the users in the Settling music platform. Users must be created and activated before you use single sign-on.

## Test SSO

In this section, you test your Microsoft Entra single sign-on configuration with following options. 

* Select **Test this application**, this option redirects to Settling music Sign-on URL where you can initiate the login flow. 

* Go to Settling music Sign-on URL directly and initiate the login flow from there.

* You can use Microsoft My Apps. When you select the Settling music tile in the My Apps, this option redirects to Settling music Sign-on URL. For more information, see [Microsoft Entra My Apps](/azure/active-directory/manage-apps/end-user-experiences#azure-ad-my-apps).

## Related content

Once you configure Settling music you can enforce session control, which protects exfiltration and infiltration of your organization’s sensitive data in real time. Session control extends from Conditional Access. [Learn how to enforce session control with Microsoft Cloud App Security](/cloud-app-security/proxy-deployment-aad).
