---
title: Configure EPHOTO DAM for Single sign-on with Microsoft Entra ID
description: Learn how to configure single sign-on between Microsoft Entra ID and EPHOTO DAM.

author: nguhiu
manager: mwongerapk
ms.reviewer: CelesteDG
ms.service: entra-id
ms.subservice: saas-apps

ms.topic: how-to
ms.date: 03/25/2025
ms.author: gideonkiratu


# Customer intent: As an IT administrator, I want to learn how to configure single sign-on between Microsoft Entra ID and EPHOTO DAM so that I can control who has access to EPHOTO DAM, enable automatic sign-in with Microsoft Entra accounts, and manage my accounts in one central location.
---

# Configure EPHOTO DAM for Single sign-on with Microsoft Entra ID

In this article,  you learn how to integrate EPHOTO DAM with Microsoft Entra ID. When you integrate EPHOTO DAM with Microsoft Entra ID, you can:

* Control in Microsoft Entra ID who has access to EPHOTO DAM.
* Enable your users to be automatically signed-in to EPHOTO DAM with their Microsoft Entra accounts.
* Manage your accounts in one central location.

## Prerequisites

The scenario outlined in this article assumes that you already have the following prerequisites:

[!INCLUDE [common-prerequisites.md](~/identity/saas-apps/includes/common-prerequisites.md)]
* EPHOTO DAM single sign-on (SSO) enabled subscription.

## Scenario description

In this article,  you configure and test Microsoft Entra SSO in a test environment.

* EPHOTO DAM supports **SP and IDP** initiated SSO

## Adding EPHOTO DAM from the gallery

To configure the integration of EPHOTO DAM into Microsoft Entra ID, you need to add EPHOTO DAM from the gallery to your list of managed SaaS apps.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](~/identity/role-based-access-control/permissions-reference.md#cloud-application-administrator).
1. Browse to **Entra ID** > **Enterprise apps** > **New application**.
1. In the **Add from the gallery** section, type **EPHOTO DAM** in the search box.
1. Select **EPHOTO DAM** from results panel and then add the app. Wait a few seconds while the app is added to your tenant.

 [!INCLUDE [sso-wizard.md](~/identity/saas-apps/includes/sso-wizard.md)]


<a name='configure-and-test-azure-ad-sso-for-ephoto-dam'></a>

## Configure and test Microsoft Entra SSO for EPHOTO DAM

Configure and test Microsoft Entra SSO with EPHOTO DAM using a test user called **B.Simon**. For SSO to work, you need to establish a link relationship between a Microsoft Entra user and the related user in EPHOTO DAM.

To configure and test Microsoft Entra SSO with EPHOTO DAM, perform the following steps:

1. **[Configure Microsoft Entra SSO](#configure-azure-ad-sso)** - to enable your users to use this feature.
    1. **Create a Microsoft Entra test user** - to test Microsoft Entra single sign-on with B.Simon.
    1. **Assign the Microsoft Entra test user** - to enable B.Simon to use Microsoft Entra single sign-on.
1. **[Configure EPHOTO DAM SSO](#configure-ephoto-dam-sso)** - to configure the single sign-on settings on application side.
    1. **[Create EPHOTO DAM test user](#create-ephoto-dam-test-user)** - to have a counterpart of B.Simon in EPHOTO DAM that's linked to the Microsoft Entra representation of user.
1. **[Test SSO](#test-sso)** - to verify whether the configuration works.

<a name='configure-azure-ad-sso'></a>

## Configure Microsoft Entra SSO

Follow these steps to enable Microsoft Entra SSO.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](~/identity/role-based-access-control/permissions-reference.md#cloud-application-administrator).
1. Browse to **Entra ID** > **Enterprise apps** > **EPHOTO DAM** > **Single sign-on**.
1. On the **Select a single sign-on method** page, select **SAML**.
1. On the **Set up single sign-on with SAML** page, select the pencil icon for **Basic SAML Configuration** to edit the settings.

   ![Edit Basic SAML Configuration](common/edit-urls.png)

1. On the **Basic SAML Configuration** section, if you wish to configure the application in **IDP** initiated mode, enter the values for the following fields:

    a. In the **Identifier** text box, type a URL using the following pattern:
    `https://<SUBDOMAIN>.ephoto.fr/simplesaml/module.php/saml/sp/metadata.php/<CUSTOMER_NAME>`

    b. In the **Reply URL** text box, type a URL using the following pattern:
    `https://<SUBDOMAIN>.ephoto.fr/simplesaml/module.php/saml/sp/saml2-acs.php/<CUSTOMER_NAME>`

1. Select **Set additional URLs** and perform the following step if you wish to configure the application in **SP** initiated mode:

    In the **Sign-on URL** text box, type a URL using the following pattern:
    `https://<SUBDOMAIN>.ephoto.fr`

	> [!NOTE]
	> These values aren't real. Update these values with the actual Identifier, Reply URL and Sign-on URL. Contact [EPHOTO DAM Client support team](mailto:support-systeme@einden.fr) to get these values. You can also refer to the patterns shown in the **Basic SAML Configuration** section.

1. On the **Set up single sign-on with SAML** page, in the **SAML Signing Certificate** section,  find **Federation Metadata XML** and select **Download** to download the certificate and save it on your computer.

	![The Certificate download link](common/metadataxml.png)

1. On the **Set up EPHOTO DAM** section, copy the appropriate URL(s) based on your requirement.

	![Copy configuration URLs](common/copy-configuration-urls.png)
<a name='create-an-azure-ad-test-user'></a>

[!INCLUDE [create-assign-users-sso.md](~/identity/saas-apps/includes/create-assign-users-sso.md)]

## Configure EPHOTO DAM SSO

To configure single sign-on on **EPHOTO DAM** side, you need to send the downloaded **Federation Metadata XML** and appropriate copied URLs from the application configuration to [EPHOTO DAM support team](mailto:support-systeme@einden.fr). They set this setting to have the SAML SSO connection set properly on both sides.

### Create EPHOTO DAM test user

In this section, you create a user called Britta Simon in EPHOTO DAM. Work with [EPHOTO DAM support team](mailto:support-systeme@einden.fr) to add the users in the EPHOTO DAM platform. Users must be created and activated before you use single sign-on.

## Test SSO 

In this section, you test your Microsoft Entra single sign-on configuration with following options. 

#### SP initiated:

* Select **Test this application**, this option redirects to EPHOTO DAM Sign on URL where you can initiate the login flow.  

* Go to EPHOTO DAM Sign-on URL directly and initiate the login flow from there.

#### IDP initiated:

* Select **Test this application**, and you should be automatically signed in to the EPHOTO DAM for which you set up the SSO 

You can also use Microsoft My Apps to test the application in any mode. When you select the EPHOTO DAM tile in the My Apps, if configured in SP mode you would be redirected to the application sign on page for initiating the login flow and if configured in IDP mode, you should be automatically signed in to the EPHOTO DAM for which you set up the SSO. For more information about the My Apps, see [Introduction to the My Apps](https://support.microsoft.com/account-billing/sign-in-and-start-apps-from-the-my-apps-portal-2f3b1bae-0e5a-4a86-a33e-876fbd2a4510).


## Related content

Once you configure EPHOTO DAM you can enforce session control, which protects exfiltration and infiltration of your organization’s sensitive data in real time. Session control extends from Conditional Access. [Learn how to enforce session control with Microsoft Defender for Cloud Apps](/cloud-app-security/proxy-deployment-any-app).
