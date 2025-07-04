---
title: Configure Infrascale Cloud Backup for Single sign-on with Microsoft Entra ID
description: Learn how to configure single sign-on between Microsoft Entra ID and Infrascale Cloud Backup.
author: nguhiu
manager: mwongerapk
ms.reviewer: CelesteDG
ms.service: entra-id
ms.subservice: saas-apps
ms.topic: how-to
ms.date: 03/25/2025
ms.author: gideonkiratu
ms.custom: sfi-image-nochange
# Customer intent: As an IT administrator, I want to learn how to configure single sign-on between Microsoft Entra ID and Infrascale Cloud Backup so that I can control who has access to Infrascale Cloud Backup, enable automatic sign-in with Microsoft Entra accounts, and manage my accounts in one central location.
---

# Configure Infrascale Cloud Backup for Single sign-on with Microsoft Entra ID

In this article,  you learn how to integrate Infrascale Cloud Backup with Microsoft Entra ID. When you integrate Infrascale Cloud Backup with Microsoft Entra ID, you can:

* Control in Microsoft Entra ID who has access to Infrascale Cloud Backup.
* Enable your users to be automatically signed-in to Infrascale Cloud Backup with their Microsoft Entra accounts.
* Manage your accounts in one central location.

## Prerequisites

To get started, you need the following items:

* A Microsoft Entra subscription. If you don't have a subscription, you can get a [free account](https://azure.microsoft.com/free/).
* Infrascale Cloud Backup single sign-on (SSO) enabled subscription.
* Along with Cloud Application Administrator, Application Administrator can also add or manage applications in Microsoft Entra ID. For more information, see [Azure built-in roles](~/identity/role-based-access-control/permissions-reference.md).

## Scenario description

In this article,  you configure and test Microsoft Entra SSO in a test environment.

* Infrascale Cloud Backup supports **SP** initiated SSO.

## Add Infrascale Cloud Backup from the gallery

To configure the integration of Infrascale Cloud Backup into Microsoft Entra ID, you need to add Infrascale Cloud Backup from the gallery to your list of managed SaaS apps.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](~/identity/role-based-access-control/permissions-reference.md#cloud-application-administrator).
1. Browse to **Entra ID** > **Enterprise apps** > **New application**.
1. In the **Add from the gallery** section, type **Infrascale Cloud Backup** in the search box.
1. Select **Infrascale Cloud Backup** from results panel and then add the app. Wait a few seconds while the app is added to your tenant.

 [!INCLUDE [sso-wizard.md](~/identity/saas-apps/includes/sso-wizard.md)]

<a name='configure-and-test-azure-ad-sso-for-infrascale-cloud-backup'></a>

## Configure and test Microsoft Entra SSO for Infrascale Cloud Backup

Configure and test Microsoft Entra SSO with Infrascale Cloud Backup using a test user called **B.Simon**. For SSO to work, you need to establish a link relationship between a Microsoft Entra user and the related user in Infrascale Cloud Backup.

To configure and test Microsoft Entra SSO with Infrascale Cloud Backup, perform the following steps:

1. **[Configure Microsoft Entra SSO](#configure-azure-ad-sso)** - to enable your users to use this feature.
    1. **Create a Microsoft Entra test user** - to test Microsoft Entra single sign-on with B.Simon.
    1. **Assign the Microsoft Entra test user** - to enable B.Simon to use Microsoft Entra single sign-on.
1. **[Configure Infrascale Cloud Backup SSO](#configure-infrascale-cloud-backup-sso)** - to configure the single sign-on settings on application side.
    1. **[Create Infrascale Cloud Backup test user](#create-infrascale-cloud-backup-test-user)** - to have a counterpart of B.Simon in Infrascale Cloud Backup that's linked to the Microsoft Entra representation of user.
1. **[Test SSO](#test-sso)** - to verify whether the configuration works.

<a name='configure-azure-ad-sso'></a>

## Configure Microsoft Entra SSO

Follow these steps to enable Microsoft Entra SSO.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](~/identity/role-based-access-control/permissions-reference.md#cloud-application-administrator).
1. Browse to **Entra ID** > **Enterprise apps** > **Infrascale Cloud Backup** > **Single sign-on**.
1. On the **Select a single sign-on method** page, select **SAML**.
1. On the **Set up single sign-on with SAML** page, select the pencil icon for **Basic SAML Configuration** to edit the settings.

    ![Screenshot shows to edit Basic S A M L Configuration.](common/edit-urls.png "Basic Configuration")

1. On the **Basic SAML Configuration** section, perform the following steps:

    a. In the **Identifier** textbox, type a URL using the following pattern:
    `https://dashboard.sosonlinebackup.com/<ID>`

    b. In the **Reply URL** textbox, type the URL:
    `https://dashboard.managedoffsitebackup.net/Account/AssertionConsumerService`  

    c. The **Sign-on URL** text box requires a specific URL for your company. The general pattern of the URL is:
    `https://[OptionalPrefix]dashboard[OptionalSuffix].CompanySpecificString.[com/net,etc]/Account/SingleSignOn`

    > [!Note]
    > don't enter this in the Sign-on URL text box. The Identifier value isn't a real URL – just a general pattern. Update this value with the actual Identifier URL obtained from Infrascale. Contact [Infrascale Cloud Backup support team](mailto:support@infrascale.com) to get the value.

1. On the **Set up single sign-on with SAML** page, In the **SAML Signing Certificate** section, select copy button to copy **App Federation Metadata Url** and save it on your computer.

	![Screenshot shows the Certificate download link.](common/copy-metadataurl.png "Certificate")  

<a name='create-an-azure-ad-test-user'></a>

[!INCLUDE [create-assign-users-sso.md](~/identity/saas-apps/includes/create-assign-users-sso.md)]

## Configure Infrascale Cloud Backup SSO

1. Log in to your Infrascale Cloud Backup company site as an administrator.

1. Go to **Settings** > **Single Sign-On** and select **Enable Single Sign-On (SSO)**.

1. In the **Single Sign-On Settings** page, perform the following steps:
    
    ![Screenshot that shows the Configuration Settings.](./media/infrascale-cloud-backup-tutorial/settings.png "Configuration")

    a. Copy **Service Provider EntityID** value, paste this value into the **Identifier** text box in the **Basic SAML Configuration** section.

    b. Copy **Reply URL** value, paste this value into the **Reply URL** text box in the **Basic SAML Configuration** section.

    c. Select **Via metadata URL** button under Identity Provider Settings section.

    d. Copy **App Federation Metadata Url** and paste it in the **Metadata URL** textbox.

    e. Select **Save**.

### Create Infrascale Cloud Backup test user

In this section, you create a user called Britta Simon in Infrascale Cloud Backup. Work with [Infrascale Cloud Backup support team](mailto:support@infrascale.com) to add the users in the Infrascale Cloud Backup platform. Users must be created and activated before you use single sign-on.

## Test SSO 

In this section, you test your Microsoft Entra single sign-on configuration with following options. 

* Select **Test this application**, this option redirects to Infrascale Cloud Backup Sign-On URL where you can initiate the login flow. 

* Go to Infrascale Cloud Backup Sign-On URL directly and initiate the login flow from there.

* You can use Microsoft My Apps. When you select the Infrascale Cloud Backup tile in the My Apps, this option redirects to Infrascale Cloud Backup Sign-On URL. For more information, see [Microsoft Entra My Apps](/azure/active-directory/manage-apps/end-user-experiences#azure-ad-my-apps).

## Related content

Once you configure Infrascale Cloud Backup you can enforce session control, which protects exfiltration and infiltration of your organization’s sensitive data in real time. Session control extends from Conditional Access. [Learn how to enforce session control with Microsoft Cloud App Security](/cloud-app-security/proxy-deployment-aad).
