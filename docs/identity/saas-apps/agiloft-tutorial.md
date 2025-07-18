---
title: Configure Agiloft Contract Management Suite for Single sign-on with Microsoft Entra ID
description: Learn how to configure single sign-on between Microsoft Entra ID and Agiloft Contract Management Suite.
author: nguhiu
manager: mwongerapk
ms.reviewer: celested
ms.service: entra-id
ms.subservice: saas-apps
ms.topic: how-to
ms.date: 03/25/2025
ms.author: gideonkiratu
ms.custom: sfi-image-nochange
# Customer intent: As an IT administrator, I want to learn how to configure single sign-on between Microsoft Entra ID and Agiloft Contract Management Suite so that I can control who has access to Agiloft Contract Management Suite, enable automatic sign-in with Microsoft Entra accounts, and manage my accounts in one central location.
---
# Configure Agiloft Contract Management Suite for Single sign-on with Microsoft Entra ID

In this article,  you learn how to integrate Agiloft Contract Management Suite with Microsoft Entra ID. When you integrate Agiloft Contract Management Suite with Microsoft Entra ID, you can:

* Control in Microsoft Entra ID who has access to Agiloft Contract Management Suite.
* Enable your users to be automatically signed-in to Agiloft Contract Management Suite with their Microsoft Entra accounts.
* Manage your accounts in one central location.

## Prerequisites

The scenario outlined in this article assumes that you already have the following prerequisites:

[!INCLUDE [common-prerequisites.md](~/identity/saas-apps/includes/common-prerequisites.md)]
* Agiloft Contract Management Suite single sign-on (SSO) enabled subscription.

## Scenario description

In this article,  you configure and test Microsoft Entra single sign-on in a test environment.

* Agiloft Contract Management Suite supports **SP and IDP** initiated SSO.
* Agiloft Contract Management Suite supports **Just In Time** user provisioning.

## Add Agiloft Contract Management Suite from the gallery

To configure the integration of Agiloft Contract Management Suite into Microsoft Entra ID, you need to add Agiloft Contract Management Suite from the gallery to your list of managed SaaS apps.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](~/identity/role-based-access-control/permissions-reference.md#cloud-application-administrator).
1. Browse to **Entra ID** > **Enterprise apps** > **New application**.
1. In the **Add from the gallery** section, type **Agiloft Contract Management Suite** in the search box.
1. Select **Agiloft Contract Management Suite** from results panel and then add the app. Wait a few seconds while the app is added to your tenant.

 [!INCLUDE [sso-wizard.md](~/identity/saas-apps/includes/sso-wizard.md)]

<a name='configure-and-test-azure-ad-sso-for-agiloft-contract-management-suite'></a>

## Configure and test Microsoft Entra SSO for Agiloft Contract Management Suite

Configure and test Microsoft Entra SSO with Agiloft Contract Management Suite using a test user called **B.Simon**. For SSO to work, you need to establish a link relationship between a Microsoft Entra user and the related user in Agiloft Contract Management Suite.

To configure and test Microsoft Entra SSO with Agiloft Contract Management Suite, perform the following steps:

1. **[Configure Microsoft Entra SSO](#configure-azure-ad-sso)** - to enable your users to use this feature.
    1. **Create a Microsoft Entra test user** - to test Microsoft Entra single sign-on with B.Simon.
    1. **Assign the Microsoft Entra test user** - to enable B.Simon to use Microsoft Entra single sign-on.
1. **[Configure Agiloft Contract Management Suite SSO](#configure-agiloft-contract-management-suite-sso)** - to configure the single sign-on settings on application side.
    1. **[Create Agiloft Contract Management Suite test user](#create-agiloft-contract-management-suite-test-user)** - to have a counterpart of B.Simon in Agiloft Contract Management Suite that's linked to the Microsoft Entra representation of user.
1. **[Test SSO](#test-sso)** - to verify whether the configuration works.

<a name='configure-azure-ad-sso'></a>

## Configure Microsoft Entra SSO

Follow these steps to enable Microsoft Entra SSO.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](~/identity/role-based-access-control/permissions-reference.md#cloud-application-administrator).
1. Browse to **Entra ID** > **Enterprise apps** > **Agiloft Contract Management Suite** > **Single sign-on**.
1. On the **Select a single sign-on method** page, select **SAML**.
1. On the **Set up single sign-on with SAML** page, select the pencil icon for **Basic SAML Configuration** to edit the settings.

   ![Edit Basic SAML Configuration](common/edit-urls.png)

1. On the **Basic SAML Configuration** section, If you wish to configure the application in **IDP** initiated mode, perform the following steps:

    a. In the **Identifier** text box, type a URL using the following pattern:
    `https://<SUBDOMAIN>.agiloft.com/<KB_NAME>`

    b. In the **Reply URL** text box, type a URL using the following pattern:
    `https://<SUBDOMAIN>.agiloft.com:443/gui2/spsamlsso?project=<KB_NAME>`

    > [!NOTE]
    > The Identifier value should match the entry in the Agiloft SAML Configuration Entity ID field. That field in Agiloft might need to be updated as follows:
    > 1. Add https:// to the beginning.
    > 1. If there are any spaces in the URL, replace each one with an underscore (_).

1. Select **Set additional URLs** and perform the following step if you wish to configure the application in **SP** initiated mode:

    In the **Sign-on URL** text box, type a URL using the following pattern:
    `https://<SUBDOMAIN>.agiloft.com:443/gui2/samlssologin.jsp?project=<KB_NAME>`

    > [!NOTE]
    > These values aren't real. Update these values with the actual Identifier, Reply URL and Sign on URL. Contact [Agiloft Contract Management Suite Client support team](https://www.agiloft.com/support-login.htm) to get these values. You can also refer to the patterns shown in the **Basic SAML Configuration** section.

1. On the **Set up Single Sign-On with SAML** page, in the **SAML Signing Certificate** section, select **Download** to download the **Certificate (Base64)** from the given options as per your requirement and save it on your computer.

    ![The Certificate download link](common/certificatebase64.png)

1. On the **Set up Agiloft Contract Management Suite** section, copy the appropriate URL(s) as per your requirement.

    ![Copy configuration URLs](common/copy-configuration-urls.png)

<a name='create-an-azure-ad-test-user'></a>

[!INCLUDE [create-assign-users-sso.md](~/identity/saas-apps/includes/create-assign-users-sso.md)]

## Configure Agiloft Contract Management Suite SSO

1. In a different web browser window, log in to your Agiloft Contract Management Suite company site as an administrator.

2. Select the **Settings** icon at the top right corner of the page.

    ![Screenshot highlighting the Setup icon.](./media/agiloft-tutorial/settings.png)

3. Select **Access**.

    ![Screenshot highlighting the Access area](./media/agiloft-tutorial/access.png)


4. Select the button **Configure SAML 2.0 Single Sign-On**.

5. A wizard dialog appears. On the dialog, select the **Identity Provider Details** and fill in the following fields:  

    ![Agiloft Contract Management Suite Configuration](./media/agiloft-tutorial/details.png)

    a. In **IdP Entity Id / Issuer** textbox, paste the value of **Microsoft Entra Identifier**.

    b. In **IdP Login URL** textbox, paste the value of **Login URL**.

    c. In **IdP Logout URL** textbox, paste the value of **Logout URL**.

    d. Open your **base-64 encoded certificate** in notepad, copy the content of it into your clipboard, and then paste it to the **IdP Provided X.509 certificate contents** textbox.

    e. Select **Finish**.

### Create Agiloft Contract Management Suite test user

In this section, a user called Britta Simon is created in Agiloft Contract Management Suite. Agiloft Contract Management Suite supports just-in-time user provisioning, which is enabled by default. There's no action item for you in this section. If a user doesn't already exist in Agiloft Contract Management Suite, a new one is created after authentication.

## Test SSO

In this section, you test your Microsoft Entra single sign-on configuration with following options. 

#### SP initiated:

* Select **Test this application**, this option redirects to Agiloft Contract Management Suite Sign on URL where you can initiate the login flow.  

* Go to Agiloft Contract Management Suite Sign-on URL directly and initiate the login flow from there.

#### IDP initiated:

* Select **Test this application**, and you should be automatically signed in to the Agiloft Contract Management Suite for which you set up the SSO. 

You can also use Microsoft My Apps to test the application in any mode. When you select the Agiloft Contract Management Suite tile in the My Apps, if configured in SP mode you would be redirected to the application sign-on page for initiating the login flow and if configured in IDP mode, you should be automatically signed in to the Agiloft Contract Management Suite for which you set up the SSO. For more information about the My Apps, see [Introduction to the My Apps](https://support.microsoft.com/account-billing/sign-in-and-start-apps-from-the-my-apps-portal-2f3b1bae-0e5a-4a86-a33e-876fbd2a4510).

## Related content

Once you configure Agiloft Contract Management Suite you can enforce session control, which protects exfiltration and infiltration of your organization’s sensitive data in real time. Session control extends from Conditional Access. [Learn how to enforce session control with Microsoft Defender for Cloud Apps](/cloud-app-security/proxy-deployment-aad).
