---
title: Configure FortiSASE for Single sign-on with Microsoft Entra ID
description: Learn how to configure single sign-on between Microsoft Entra ID and FortiSASE.
author: nguhiu
manager: mwongerapk
ms.reviewer: CelesteDG
ms.service: entra-id
ms.subservice: saas-apps
ms.topic: how-to
ms.date: 03/25/2025
ms.author: gideonkiratu
ms.custom: sfi-image-nochange
# Customer intent: As an IT administrator, I want to learn how to configure single sign-on between Microsoft Entra ID and FortiSASE so that I can control who has access to FortiSASE, enable automatic sign-in with Microsoft Entra accounts, and manage my accounts in one central location.
---

# Configure FortiSASE for Single sign-on with Microsoft Entra ID

In this article,  you learn how to integrate FortiSASE with Microsoft Entra ID. When you integrate FortiSASE with Microsoft Entra ID, you can:

* Control in Microsoft Entra ID who has access to FortiSASE.
* Enable your users to be automatically signed-in to FortiSASE with their Microsoft Entra accounts.
* Manage your accounts in one central location.

## Prerequisites

To get started, you need the following items:

* A Microsoft Entra subscription. If you don't have a subscription, you can get a [free account](https://azure.microsoft.com/free/).
* FortiSASE single sign-on (SSO) enabled subscription.
* Along with Cloud Application Administrator, Application Administrator can also add or manage applications in Microsoft Entra ID.
For more information, see [Azure built-in roles](~/identity/role-based-access-control/permissions-reference.md).

## Scenario description

In this article,  you configure and test Microsoft Entra SSO in a test environment.

* FortiSASE supports **SP** initiated SSO.

* FortiSASE supports **Just In Time** user provisioning.

## Add FortiSASE from the gallery

To configure the integration of FortiSASE into Microsoft Entra ID, you need to add FortiSASE from the gallery to your list of managed SaaS apps.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](~/identity/role-based-access-control/permissions-reference.md#cloud-application-administrator).
1. Browse to **Entra ID** > **Enterprise apps** > **New application**.
1. In the **Add from the gallery** section, type **FortiSASE** in the search box.
1. Select **FortiSASE** from results panel and then add the app. Wait a few seconds while the app is added to your tenant.

 [!INCLUDE [sso-wizard.md](~/identity/saas-apps/includes/sso-wizard.md)]

<a name='configure-and-test-azure-ad-sso-for-fortisase'></a>

## Configure and test Microsoft Entra SSO for FortiSASE

Configure and test Microsoft Entra SSO with FortiSASE using a test user called **B.Simon**. For SSO to work, you need to establish a link relationship between a Microsoft Entra user and the related user in FortiSASE.

To configure and test Microsoft Entra SSO with FortiSASE, perform the following steps:

1. **[Configure Microsoft Entra SSO](#configure-azure-ad-sso)** - to enable your users to use this feature.
    1. **Create a Microsoft Entra test user** - to test Microsoft Entra single sign-on with B.Simon.
    1. **Assign the Microsoft Entra test user** - to enable B.Simon to use Microsoft Entra single sign-on.
1. **[Configure FortiSASE SSO](#configure-fortisase-sso)** - to configure the single sign-on settings on application side.
    1. **[Create FortiSASE test user](#create-fortisase-test-user)** - to have a counterpart of B.Simon in FortiSASE that's linked to the Microsoft Entra representation of user.
1. **[Test SSO](#test-sso)** - to verify whether the configuration works.

<a name='configure-azure-ad-sso'></a>

## Configure Microsoft Entra SSO

Follow these steps to enable Microsoft Entra SSO.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](~/identity/role-based-access-control/permissions-reference.md#cloud-application-administrator).
1. Browse to **Entra ID** > **Enterprise apps** > **FortiSASE** > **Single sign-on**.
1. On the **Select a single sign-on method** page, select **SAML**.
1. On the **Set up single sign-on with SAML** page, select the pencil icon for **Basic SAML Configuration** to edit the settings.

   ![Edit Basic SAML Configuration](common/edit-urls.png)

1. On the **Basic SAML Configuration** section, perform the following steps:

	a. In the **Identifier (Entity ID)** text box, type a URL using one of the following patterns:

	| User | URL |
	|------|-----|
	| For FortiSASE VPN User SSO | `https://<TENANTHOSTNAME>.edge.prod.fortisase.com/remote/saml/metadata` |
	| For FortiSASE SWG User SSO | `https://<TENANTHOSTNAME>.edge.prod.fortisase.com:7831/XX/YY/ZZ/saml/metadata` |

	b. In the **Reply URL** text box, type a URL using one of the following patterns:

	| User | URL |
	|------|-----|
	| For FortiSASE VPN User SSO | `https://<TENANTHOSTNAME>.edge.prod.fortisase.com/remote/saml/login` |
	| For FortiSASE SWG User SSO | `https://<TENANTHOSTNAME>.edge.prod.fortisase.com:7831/XX/YY/ZZ/saml/login` |
	
	c. In the **Sign on URL** text box, type a URL using one of the following patterns:

    | User | URL |
	|------|-----|
	| For FortiSASE VPN User SSO | `https://<TENANTHOSTNAME>.edge.prod.fortisase.com/remote/login` |
	| For FortiSASE SWG User SSO | `https://<TENANTHOSTNAME>.edge.prod.fortisase.com:7831/XX/YY/ZZ/login` |

	> [!NOTE]
	> These values aren't real. Update these values with the actual Identifier, Reply URL and Sign on URL. On the FortiSASE portal, go to **Configuration > VPN User SSO** or **Configuration > SWG User SSO** to find the service provider URLs. You can also refer to the patterns shown in the **Basic SAML Configuration** section.

1. FortiSASE application expects the SAML assertions in a specific format, which requires you to add custom attribute mappings to your SAML token attributes configuration. The following screenshot shows the list of default attributes.

	![image](common/default-attributes.png)

1. In addition to above, FortiSASE application expects few more attributes to be passed back in SAML response, which are shown below. These attributes are also pre populated but you can review them as per your requirements.
	
	| Name |  Source Attribute|
	| --------------- | --------- |
	| group | user.groups |
	| username | user.userprincipalname |

1. On the **Set up single sign-on with SAML** page, in the **SAML Signing Certificate** section,  find **Certificate (Base64)** and select **Download** to download the certificate and save it on your computer.

	![The Certificate download link](common/certificatebase64.png)

1. On the **Set up FortiSASE** section, copy the appropriate URL(s) based on your requirement.

	![Copy configuration URLs](common/copy-configuration-urls.png)

<a name='create-an-azure-ad-test-user'></a>

[!INCLUDE [create-assign-users-sso.md](~/identity/saas-apps/includes/create-assign-users-sso.md)]

## Configure FortiSASE SSO

1. Log in to your FortiSASE company site as an administrator.

1. Go to **Configuration > VPN User SSO** or **Configuration > SWG User SSO** depending on the FortiSASE mode used.

1. In the **Configure Identity Provider** section, copy the following URLs and paste in the **Basic SAML Configuration** section.

	![Screenshot that shows the Configuration](./media/fortisase-tutorial/general.png "Configuration")

1. In the **Configure Service Provider** section, perform the following steps:

	![Screenshot that shows Service Provider configuration](./media/fortisase-tutorial/certificate.png "Service Provider")

	a. In the **IdP Entity ID** textbox, paste the **Microsoft Entra Identifier** value which you copied previously.

	b. In the **IdP Single Sign-On URL** textbox, paste the **Login URL** value which you copied previously.

	c. In the **IdP Single Log-Out URL** textbox, paste the **Logout URL** value which you copied previously.

	d. Open the downloaded **Certificate (Base64)** into Notepad and upload the content into the  **IdP Certificate** textbox.

1. Review and submit the configuration.

### Create FortiSASE test user

FortiSASE supports just-in-time user provisioning, which is enabled by default. There's no action item for you in this section.

## Test SSO 

In this section, you test your Microsoft Entra single sign-on configuration with following options. 

* Select **Test this application**, this option redirects to FortiSASE Sign-on URL where you can initiate the login flow. 

* Go to FortiSASE Sign-on URL directly and initiate the login flow from there.

* You can use Microsoft My Apps. When you select the FortiSASE tile in the My Apps, this option redirects to FortiSASE Sign-on URL. For more information about the My Apps, see [Introduction to the My Apps](https://support.microsoft.com/account-billing/sign-in-and-start-apps-from-the-my-apps-portal-2f3b1bae-0e5a-4a86-a33e-876fbd2a4510).

## Related content

Once you configure FortiSASE you can enforce session control, which protects exfiltration and infiltration of your organization’s sensitive data in real time. Session control extends from Conditional Access. [Learn how to enforce session control with Microsoft Defender for Cloud Apps](/cloud-app-security/proxy-deployment-any-app).
