---
title: Configure Standard for Success Accreditation for Single sign-on with Microsoft Entra ID
description: Learn how to configure single sign-on between Microsoft Entra ID and Standard for Success Accreditation.
author: nguhiu
manager: mwongerapk
ms.reviewer: CelesteDG
ms.service: entra-id
ms.subservice: saas-apps
ms.topic: how-to
ms.date: 05/20/2025
ms.author: gideonkiratu
ms.custom: sfi-image-nochange
# Customer intent: As an IT administrator, I want to learn how to configure single sign-on between Microsoft Entra ID and Standard for Success Accreditation so that I can control who has access to Standard for Success Accreditation, enable automatic sign-in with Microsoft Entra accounts, and manage my accounts in one central location.
---

# Configure Standard for Success Accreditation for Single sign-on with Microsoft Entra ID

In this article,  you learn how to integrate Standard for Success Accreditation with Microsoft Entra ID. When you integrate Standard for Success Accreditation with Microsoft Entra ID, you can:

* Control in Microsoft Entra ID who has access to Standard for Success Accreditation.
* Enable your users to be automatically signed-in to Standard for Success Accreditation with their Microsoft Entra accounts.

## Prerequisites
The scenario outlined in this article assumes that you already have the following prerequisites:

[!INCLUDE [common-prerequisites.md](~/identity/saas-apps/includes/common-prerequisites.md)]
* Standard for Success Accreditation single sign-on (SSO) enabled subscription.

## Scenario description

In this article,  you configure and test Microsoft Entra SSO in a test environment.

* Standard for Success Accreditation supports **SP and IDP** initiated SSO.

## Add Standard for Success Accreditation from the gallery

To configure the integration of Standard for Success Accreditation into Microsoft Entra ID, you need to add Standard for Success Accreditation from the gallery to your list of managed SaaS apps.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](~/identity/role-based-access-control/permissions-reference.md#cloud-application-administrator).
1. Browse to **Entra ID** > **Enterprise apps** > **New application**.
1. In the **Add from the gallery** section, type **Standard for Success Accreditation** in the search box.
1. Select **Standard for Success Accreditation** from the results panel and then add the app. Wait a few seconds while the app is added to your tenant.

 Alternatively, you can also use the [Enterprise App Configuration Wizard](https://portal.office.com/AdminPortal/home?Q=Docs#/azureadappintegration). In this wizard, you can add an application to your tenant, add users/groups to the app, assign roles, and walk through the SSO configuration as well. [Learn more about Microsoft 365 wizards.](/microsoft-365/admin/misc/azure-ad-setup-guides)

<a name='configure-and-test-azure-ad-sso-for-standard-for-success-accreditation'></a>

## Configure and test Microsoft Entra SSO for Standard for Success Accreditation

Configure and test Microsoft Entra SSO with Standard for Success Accreditation using a test user called **B.Simon**. For SSO to work, you need to establish a link relationship between a Microsoft Entra user and the related user in Standard for Success Accreditation.

To configure and test Microsoft Entra SSO with Standard for Success Accreditation, perform the following steps:

1. **[Configure Microsoft Entra SSO](#configure-azure-ad-sso)** - to enable your users to use this feature.
    1. **Create a Microsoft Entra test user** - to test Microsoft Entra single sign-on with B.Simon.
    1. **Assign the Microsoft Entra test user** - to enable B.Simon to use Microsoft Entra single sign-on.
1. **[Configure Standard for Success Accreditation SSO](#configure-standard-for-success-accreditation-sso)** - to configure the single sign-on settings on application side.
    1. **[Create Standard for Success Accreditation test user](#create-standard-for-success-accreditation-test-user)** - to have a counterpart of B.Simon in Standard for Success Accreditation that's linked to the Microsoft Entra representation of user.
1. **[Test SSO](#test-sso)** - to verify whether the configuration works.

<a name='configure-azure-ad-sso'></a>

## Configure Microsoft Entra SSO

Follow these steps to enable Microsoft Entra SSO.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](~/identity/role-based-access-control/permissions-reference.md#cloud-application-administrator).
1. Browse to **Entra ID** > **Enterprise apps** > **Standard for Success Accreditation** > **Single sign-on**.
1. On the **Select a single sign-on method** page, select **SAML**.
1. On the **Set up single sign-on with SAML** page, select the pencil icon for **Basic SAML Configuration** to edit the settings.

   ![Edit Basic SAML Configuration](common/edit-urls.png)

1. On the **Basic SAML Configuration** section, if you wish to configure the application in **IDP** initiated mode, perform the following steps:

    a. In the **Identifier** text box, type a value using the following pattern: 
    `api://<ApplicationId>`

    b. In the **Reply URL** text box, type a URL using the following pattern:
    `https://edu.sfsed.com/access/saml_consume?did=<INSTITUTION-ID>`

1. Select **Set additional URLs** and perform the following steps if you wish to configure the application in **SP** initiated mode:

    a. In the **Sign-on URL** text box, type a URL using the following pattern:
    `https://edu.sfsed.com/access/saml_int?did=<INSTITUTION-ID>`

    b. In the **Relay State** text box, type a URL using the following pattern:
    `https://edu.sfsed.com/access/saml_consume?did=<INSTITUTION-ID>`

    > [!NOTE]
    > These values aren't real. Update these values with the actual Identifier, Reply URL, Sign-on URL and Relay State. Contact [Standard for Success Accreditation Client support team](mailto:help_he@standardforsuccess.com) to get these values. You can also refer to the patterns shown in the **Basic SAML Configuration** section.

1. In the **SAML Signing Certificate** section, select **Edit** button to open **SAML Signing Certificate** dialog.

	![Edit SAML Signing Certificate](common/edit-certificate.png)

1. In the **SAML Signing Certificate** section, copy the **Thumbprint Value** and save it on your computer.

    ![Copy Thumbprint value](common/copy-thumbprint.png)

1. On the **Set up Standard for Success Accreditation** section, copy the appropriate URL(s) based on your requirement.

	![Copy configuration URLs](common/copy-configuration-urls.png)

<a name='create-an-azure-ad-test-user'></a>

[!INCLUDE [create-assign-users-sso.md](~/identity/saas-apps/includes/create-assign-users-sso.md)]

## Configure Standard for Success Accreditation SSO

1. Open a new web browser window and sign into the Standard for Success Accreditation site as an administrator with superuser access.

1. From the menu, select **Admin Portal**.

1. Scroll down to **Single Sign On Settings** and select the **Microsoft Azure Single Sign On** link and perform the following steps.

    :::image type="content" source="./media/standard-for-success-accreditation-tutorial/configuration.png" alt-text="Screenshot that shows how to enable Azure single sign-on in Standard for Success Accreditation.":::

    a. Select the **Enable Azure Single Sign On** checkbox.

    b. Fill the URL and Identifier fields with the appropriate URLs copied SAML setup.

    c. Fill the Application ID in the **Application ID** text box.

    d. In the **Certificate Thumbprint** text box, paste the **Thumbprint Value** that you copied.

    e. Select **Save**. 

### Create Standard for Success Accreditation test user

1.	Sign in to Standard for Success Accreditation as an Administrator with superuser privileges.

1. From the menu, select **Admin Portal** > **Create New Evaluatee** and perform the following steps.

    ![creating test user.](./media/standard-for-success-accreditation-tutorial/new-user.png)

    a. In **First Name** text box, enter B.

    b. In **Last Name** text box, enter Simon.

    c. In **University Email** text box, enter the email address you added for B.Simon within Azure.

    d. Scroll to the bottom and Select **Create User**.

## Test SSO 

In this section, you test your Microsoft Entra single sign-on configuration with following options. 

#### SP initiated:

* Select **Test this application**, this option redirects to Standard for Success Accreditation Sign on URL where you can initiate the login flow.  

* Go to Standard for Success Accreditation Sign-on URL directly and initiate the login flow from there.

#### IDP initiated:

* Select **Test this application**, and you should be automatically signed in to the Standard for Success Accreditation for which you set up the SSO 

You can also use Microsoft My Apps to test the application in any mode. When you select the Standard for Success Accreditation tile in the My Apps, if configured in SP mode you would be redirected to the application sign on page for initiating the login flow and if configured in IDP mode, you should be automatically signed in to the Standard for Success Accreditation for which you set up the SSO. For more information about the My Apps, see [Introduction to the My Apps](https://support.microsoft.com/account-billing/sign-in-and-start-apps-from-the-my-apps-portal-2f3b1bae-0e5a-4a86-a33e-876fbd2a4510).

## Related content

Once you configure Standard for Success Accreditation you can enforce session control, which protects exfiltration and infiltration of your organization’s sensitive data in real time. Session control extends from Conditional Access. [Learn how to enforce session control with Microsoft Defender for Cloud Apps](/cloud-app-security/proxy-deployment-any-app).
