---
title: Configure MVISION Cloud Microsoft Entra SSO Configuration for Single sign-on with Microsoft Entra ID
description: Learn how to configure single sign-on between Microsoft Entra ID and MVISION Cloud Microsoft Entra SSO Configuration.

author: nguhiu
manager: mwongerapk
ms.reviewer: celested
ms.service: entra-id
ms.subservice: saas-apps

ms.topic: how-to
ms.date: 05/20/2025
ms.author: gideonkiratu

# Customer intent: As an IT administrator, I want to learn how to configure single sign-on between Microsoft Entra ID and MVISION Cloud Microsoft Entra SSO Configuration so that I can control who has access to MVISION Cloud Microsoft Entra SSO Configuration, enable automatic sign-in with Microsoft Entra accounts, and manage my accounts in one central location.
---
# Configure MVISION Cloud Microsoft Entra SSO Configuration for Single sign-on with Microsoft Entra ID

In this article,  you learn how to integrate MVISION Cloud Microsoft Entra SSO Configuration with Microsoft Entra ID. When you integrate MVISION Cloud Microsoft Entra SSO Configuration with Microsoft Entra ID, you can:

* Control in Microsoft Entra ID who has access to MVISION Cloud Microsoft Entra SSO Configuration.
* Enable your users to be automatically signed-in to MVISION Cloud Microsoft Entra SSO Configuration with their Microsoft Entra accounts.
* Manage your accounts in one central location.

## Prerequisites
The scenario outlined in this article assumes that you already have the following prerequisites:

[!INCLUDE [common-prerequisites.md](~/identity/saas-apps/includes/common-prerequisites.md)]
* MVISION Cloud Microsoft Entra SSO Configuration single sign-on (SSO) enabled subscription.

## Scenario description

In this article,  you configure and test Microsoft Entra single sign-on in a test environment.

* MVISION Cloud Microsoft Entra SSO Configuration supports **SP and IDP** initiated SSO.

<a name='add-mvision-cloud-azure-ad-sso-configuration-from-the-gallery'></a>

## Add MVISION Cloud Microsoft Entra SSO Configuration from the gallery

To configure the integration of MVISION Cloud Microsoft Entra SSO Configuration into Microsoft Entra ID, you need to add MVISION Cloud Microsoft Entra SSO Configuration from the gallery to your list of managed SaaS apps.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](~/identity/role-based-access-control/permissions-reference.md#cloud-application-administrator).
1. Browse to **Entra ID** > **Enterprise apps** > **New application**.
1. In the **Add from the gallery** section, type **MVISION Cloud Microsoft Entra SSO Configuration** in the search box.
1. Select **MVISION Cloud Microsoft Entra SSO Configuration** from results panel and then add the app. Wait a few seconds while the app is added to your tenant.

 Alternatively, you can also use the [Enterprise App Configuration Wizard](https://portal.office.com/AdminPortal/home?Q=Docs#/azureadappintegration). In this wizard, you can add an application to your tenant, add users/groups to the app, assign roles, and walk through the SSO configuration as well. [Learn more about Microsoft 365 wizards.](/microsoft-365/admin/misc/azure-ad-setup-guides)

<a name='configure-and-test-azure-ad-sso-for-mvision-cloud-azure-ad-sso-configuration'></a>

## Configure and test Microsoft Entra SSO for MVISION Cloud Microsoft Entra SSO Configuration

Configure and test Microsoft Entra SSO with MVISION Cloud Microsoft Entra SSO Configuration using a test user called **Britta Simon**. For SSO to work, you need to establish a link relationship between a Microsoft Entra user and the related user in MVISION Cloud Microsoft Entra SSO Configuration.

To configure and test Microsoft Entra SSO with MVISION Cloud Microsoft Entra SSO Configuration, perform the following steps:

1. **[Configure Microsoft Entra SSO](#configure-azure-ad-sso)** - to enable your users to use this feature.
    1. **Create a Microsoft Entra test user** - to test Microsoft Entra single sign-on with Britta Simon.
    4. **Assign the Microsoft Entra test user** - to enable Britta Simon to use Microsoft Entra single sign-on.
1. **[Configure MVISION Cloud Microsoft Entra SSO Configuration SSO](#configure-mvision-cloud-azure-ad-sso-configuration-sso)** - to configure the Single Sign-On settings on application side.
    1. **[Create MVISION Cloud Microsoft Entra SSO Configuration test user](#create-mvision-cloud-azure-ad-sso-configuration-test-user)** - to have a counterpart of Britta Simon in MVISION Cloud Microsoft Entra SSO Configuration that's linked to the Microsoft Entra representation of user.
1. **[Test SSO](#test-sso)** - to verify whether the configuration works.

<a name='configure-azure-ad-sso'></a>

### Configure Microsoft Entra SSO

Follow these steps to enable Microsoft Entra SSO.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](~/identity/role-based-access-control/permissions-reference.md#cloud-application-administrator).
1. Browse to **Entra ID** > **Enterprise apps** > **Datadog** > **Single sign-on**.
1. On the **Select a single sign-on method** page, select **SAML**.
1. On the **Set up single sign-on with SAML** page, select the pencil icon for **Basic SAML Configuration** to edit the settings.

   ![Edit Basic SAML Configuration](common/edit-urls.png)

1. On the **Basic SAML Configuration** section, If you wish to configure the application in **IDP** initiated mode, perform the following steps:

    a. In the **Identifier** text box, type a URL using the following pattern:
    `https://<ENV>.myshn.net/shndash/saml/Azure_SSO`

    b. In the **Reply URL** text box, type a URL using the following pattern:
    `https://<ENV>.myshn.net/shndash/response/saml-postlogin`

5. Select **Set additional URLs** and perform the following step if you wish to configure the application in **SP** initiated mode:

    In the **Sign-on URL** text box, type a URL using the following pattern:
    `https://<ENV>.myshn.net/shndash/saml/Azure_SSO`

	> [!NOTE]
	> These values aren't real. Update these values with the actual Identifier, Reply URL and Sign-on URL. Contact [MVISION Cloud Microsoft Entra SSO Configuration Client support team](mailto:support@skyhighnetworks.com) to get these values. You can also refer to the patterns shown in the **Basic SAML Configuration** section.

6. On the **Set up Single Sign-On with SAML** page, in the **SAML Signing Certificate** section, select **Download** to download the **Certificate (Base64)** from the given options as per your requirement and save it on your computer.

	![The Certificate download link](common/certificatebase64.png)

7. On the **Set up MVISION Cloud Microsoft Entra SSO Configuration** section, copy the appropriate URL(s) as per your requirement.

	![Copy configuration URLs](common/copy-configuration-urls.png)

<a name='create-an-azure-ad-test-user'></a>

[!INCLUDE [create-assign-users-sso.md](~/identity/saas-apps/includes/create-assign-users-sso.md)]

<a name='configure-mvision-cloud-azure-ad-sso-configuration-sso'></a>

## Configure MVISION Cloud Microsoft Entra SSO Configuration SSO

To configure single sign-on on **MVISION Cloud Microsoft Entra SSO Configuration** side, you need to send the downloaded **Certificate (Base64)** and appropriate copied URLs from the application configuration to [MVISION Cloud Microsoft Entra SSO Configuration support team](mailto:support@skyhighnetworks.com). They set this setting to have the SAML SSO connection set properly on both sides.

<a name='create-mvision-cloud-azure-ad-sso-configuration-test-user'></a>

### Create MVISION Cloud Microsoft Entra SSO Configuration test user

In this section, you create a user called B.Simon in MVISION Cloud Microsoft Entra SSO Configuration. Work with [MVISION Cloud Microsoft Entra SSO Configuration support team](mailto:support@skyhighnetworks.com) to add the users in the MVISION Cloud Microsoft Entra SSO Configuration platform. Users must be created and activated before you use single sign-on.

## Test SSO 

In this section, you test your Microsoft Entra single sign-on configuration with following options. 

#### SP initiated:

* Select **Test this application**, this option redirects to MVISION Cloud Microsoft Entra SSO Configuration Sign on URL where you can initiate the login flow.  

* Go to MVISION Cloud Microsoft Entra SSO Configuration Sign-on URL directly and initiate the login flow from there.

#### IDP initiated:

* Select **Test this application**, and you should be automatically signed in to the MVISION Cloud Microsoft Entra SSO Configuration for which you set up the SSO. 

You can also use Microsoft My Apps to test the application in any mode. When you select the MVISION Cloud Microsoft Entra SSO Configuration tile in the My Apps, if configured in SP mode you would be redirected to the application sign on page for initiating the login flow and if configured in IDP mode, you should be automatically signed in to the MVISION Cloud Microsoft Entra SSO Configuration for which you set up the SSO. For more information about the My Apps, see [Introduction to the My Apps](https://support.microsoft.com/account-billing/sign-in-and-start-apps-from-the-my-apps-portal-2f3b1bae-0e5a-4a86-a33e-876fbd2a4510).

## Related content

Once you configure MVISION Cloud Microsoft Entra SSO Configuration you can enforce session control, which protects exfiltration and infiltration of your organization’s sensitive data in real time. Session control extends from Conditional Access. [Learn how to enforce session control with Microsoft Defender for Cloud Apps](/cloud-app-security/proxy-deployment-any-app).
