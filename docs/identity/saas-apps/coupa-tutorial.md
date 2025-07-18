---
title: Configure Coupa for Single sign-on with Microsoft Entra ID
description: Learn how to configure single sign-on between Microsoft Entra ID and Coupa.
author: nguhiu
manager: mwongerapk
ms.reviewer: celested
ms.service: entra-id
ms.subservice: saas-apps
ms.topic: how-to
ms.date: 03/25/2025
ms.author: gideonkiratu
ms.custom: sfi-image-nochange
# Customer intent: As an IT administrator, I want to learn how to configure single sign-on between Microsoft Entra ID and Coupa so that I can control who has access to Coupa, enable automatic sign-in with Microsoft Entra accounts, and manage my accounts in one central location.
---
# Configure Coupa for Single sign-on with Microsoft Entra ID

In this article,  you learn how to integrate Coupa with Microsoft Entra ID. When you integrate Coupa with Microsoft Entra ID, you can:

* Control in Microsoft Entra ID who has access to Coupa.
* Enable your users to be automatically signed-in to Coupa with their Microsoft Entra accounts.
* Manage your accounts in one central location.

## Prerequisites

The scenario outlined in this article assumes that you already have the following prerequisites:

[!INCLUDE [common-prerequisites.md](~/identity/saas-apps/includes/common-prerequisites.md)]
* Coupa single sign-on (SSO) enabled subscription.

## Scenario description

In this article,  you configure and test Microsoft Entra single sign-on in a test environment.

* Coupa supports **SP** initiated SSO

## Add Coupa from the gallery

To configure the integration of Coupa into Microsoft Entra ID, you need to add Coupa from the gallery to your list of managed SaaS apps.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](~/identity/role-based-access-control/permissions-reference.md#cloud-application-administrator).
1. Browse to **Entra ID** > **Enterprise apps** > **New application**.
1. In the **Add from the gallery** section, type **Coupa** in the search box.
1. Select **Coupa** from results panel and then add the app. Wait a few seconds while the app is added to your tenant.

 [!INCLUDE [sso-wizard.md](~/identity/saas-apps/includes/sso-wizard.md)]

<a name='configure-and-test-azure-ad-sso-for-coupa'></a>

## Configure and test Microsoft Entra SSO for Coupa

Configure and test Microsoft Entra SSO with Coupa using a test user called **B.Simon**. For SSO to work, you need to establish a link relationship between a Microsoft Entra user and the related user in Coupa.

To configure and test Microsoft Entra SSO with Coupa, perform the following steps:

1. **[Configure Microsoft Entra SSO](#configure-azure-ad-sso)** - to enable your users to use this feature.
    1. **Create a Microsoft Entra test user** - to test Microsoft Entra single sign-on with B.Simon.
    1. **Assign the Microsoft Entra test user** - to enable B.Simon to use Microsoft Entra single sign-on.
1. **[Configure Coupa SSO](#configure-coupa-sso)** - to configure the single sign-on settings on application side.
    1. **[Create Coupa test user](#create-coupa-test-user)** - to have a counterpart of B.Simon inCoupa that's linked to the Microsoft Entra representation of user.
1. **[Test SSO](#test-sso)** - to verify whether the configuration works.

<a name='configure-azure-ad-sso'></a>

## Configure Microsoft Entra SSO

Follow these steps to enable Microsoft Entra SSO.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](~/identity/role-based-access-control/permissions-reference.md#cloud-application-administrator).
1. Browse to **Entra ID** > **Enterprise apps** > **Coupa** > **Single sign-on**.
1. On the **Select a single sign-on method** page, select **SAML**.
1. On the **Set up single sign-on with SAML** page, select the pencil icon for **Basic SAML Configuration** to edit the settings.

   ![Edit Basic SAML Configuration](common/edit-urls.png)

1. On the **Basic SAML Configuration** section, perform the following steps:

    a. In the **Sign-on URL** text box, type a URL using the following pattern:
    `https://<companyname>.coupahost.com`

    > [!NOTE]
    > The Sign-on URL value isn't real. Update this value with the actual Sign-On URL. Contact [Coupa Client support team](https://success.coupa.com/Support/Contact_Us?) to get this value.

    b. In the **Identifier** box, type the URL:

    | Environment  | URL |
    |:-------------|----|
    | Sandbox | `sso-stg1.coupahost.com`|
    | Production | `sso-prd1.coupahost.com`|
    | | |

    c. In the **Reply URL** text box, type the URL:

    | Environment | URL |
    |------------- |----|
    | Sandbox | `https://sso-stg1.coupahost.com/sp/ACS.saml2`|
    | Production | `https://sso-prd1.coupahost.com/sp/ACS.saml2`|
    | | |

4. On the **Set up Single Sign-On with SAML** page, in the **SAML Signing Certificate** section, select **Download** to download the **Federation Metadata XML** from the given options as per your requirement and save it on your computer.

    ![The Certificate download link](common/metadataxml.png)

6. On the **Set up Coupa** section, copy the appropriate URL(s) as per your requirement.

    ![Copy configuration URLs](common/copy-configuration-urls.png)

<a name='create-an-azure-ad-test-user'></a>

[!INCLUDE [create-assign-users-sso.md](~/identity/saas-apps/includes/create-assign-users-sso.md)]

## Configure Coupa SSO

1. Sign on to your Coupa company site as an administrator.

2. Go to **Setup** > **Security Control**.

    ![Security Controls](./media/coupa-tutorial/setup.png "Security Controls")

3. In the **Log in using Coupa credentials** section, perform the following steps:

    ![Coupa SP metadata](./media/coupa-tutorial/login.png "Coupa SP metadata")

    a. Select **Log in using SAML**.

    b. Select **Browse** to upload the metadata downloaded.

    c. Select **Save**.

### Create Coupa test user

In order to enable Microsoft Entra users to log into Coupa, they must be provisioned into Coupa.  

* In the case of Coupa, provisioning is a manual task.

**To configure user provisioning, perform the following steps:**

1. Log in to your **Coupa** company site as administrator.

2. In the menu on the top, select **Setup**, and then select **Users**.

    ![Users](./media/coupa-tutorial/user.png "Users")

3. Select **Create**.

    ![Create Users](./media/coupa-tutorial/create.png "Create Users")

4. In the **User Create** section, perform the following steps:

    ![User Details](./media/coupa-tutorial/details.png "User Details")

    a. Type the **Login**, **First name**, **Last Name**, **Single Sign-On ID**, **Email** attributes of a valid Microsoft Entra account you want to provision into the related textboxes.

    b. Select **Create**.

    >[!NOTE]
    >The Microsoft Entra account holder gets an email with a link to confirm the account before it becomes active.
    >

>[!NOTE]
>You can use any other Coupa user account creation tools or APIs provided by Coupa to provision Microsoft Entra user accounts.

## Test SSO

In this section, you test your Microsoft Entra single sign-on configuration with following options. 

* Select **Test this application**, this option redirects to Coupa Sign-on URL where you can initiate the login flow. 

* Go to Coupa Sign-on URL directly and initiate the login flow from there.

* You can use Microsoft My Apps. When you select the Coupa tile in the My Apps, you should be automatically signed in to the Coupa for which you set up the SSO. For more information about the My Apps, see [Introduction to the My Apps](https://support.microsoft.com/account-billing/sign-in-and-start-apps-from-the-my-apps-portal-2f3b1bae-0e5a-4a86-a33e-876fbd2a4510).

## Related content

Once you configure  Coupa you can enforce session control, which protects exfiltration and infiltration of your organization’s sensitive data in real time. Session control extends from Conditional Access. [Learn how to enforce session control with Microsoft Defender for Cloud Apps](/cloud-app-security/proxy-deployment-any-app).
