---
title: Configure Zoho One for Single sign-on with Microsoft Entra ID
description: Learn how to configure single sign-on between Microsoft Entra ID and Zoho One.
author: nguhiu
manager: mwongerapk
ms.reviewer: celested
ms.service: entra-id
ms.subservice: saas-apps
ms.topic: how-to
ms.date: 05/20/2025
ms.author: gideonkiratu
ms.custom: sfi-image-nochange
# Customer intent: As an IT administrator, I want to learn how to configure single sign-on between Microsoft Entra ID and Zoho One so that I can control who has access to Zoho One, enable automatic sign-in with Microsoft Entra accounts, and manage my accounts in one central location.
---
# Configure Zoho One for Single sign-on with Microsoft Entra ID

In this article,  you learn how to integrate Zoho One with Microsoft Entra ID. When you integrate Zoho One with Microsoft Entra ID, you can:

* Control in Microsoft Entra ID who has access to Zoho One.
* Enable your users to be automatically signed-in to Zoho One with their Microsoft Entra accounts.
* Manage your accounts in one central location.

## Prerequisites
The scenario outlined in this article assumes that you already have the following prerequisites:

[!INCLUDE [common-prerequisites.md](~/identity/saas-apps/includes/common-prerequisites.md)]
* Zoho One single sign-on enabled subscription.

## Scenario description

In this article,  you configure and test Microsoft Entra single sign-on in a test environment.

* Zoho One supports **SP** and **IDP** initiated SSO.

> [!NOTE]
> Identifier of this application is a fixed string value so only one instance can be configured in one tenant.

## Add Zoho One from the gallery

To configure the integration of Zoho One into Microsoft Entra ID, you need to add Zoho One from the gallery to your list of managed SaaS apps.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](~/identity/role-based-access-control/permissions-reference.md#cloud-application-administrator).
1. Browse to **Entra ID** > **Enterprise apps** > **New application**.
1. In the **Add from the gallery** section, type **Zoho One** in the search box.
1. Select **Zoho One** from results panel and then add the app. Wait a few seconds while the app is added to your tenant.

 Alternatively, you can also use the [Enterprise App Configuration Wizard](https://portal.office.com/AdminPortal/home?Q=Docs#/azureadappintegration). In this wizard, you can add an application to your tenant, add users/groups to the app, assign roles, and walk through the SSO configuration as well. [Learn more about Microsoft 365 wizards.](/microsoft-365/admin/misc/azure-ad-setup-guides)

<a name='configure-and-test-azure-ad-sso-for-zoho-one'></a>

## Configure and test Microsoft Entra SSO for Zoho One

Configure and test Microsoft Entra SSO with Zoho One using a test user called **B.Simon**. For SSO to work, you need to establish a link relationship between a Microsoft Entra user and the related user in Zoho One.

To configure and test Microsoft Entra SSO with Zoho One, perform the following steps:

1. **[Configure Microsoft Entra SSO](#configure-azure-ad-sso)** - to enable your users to use this feature.
    1. **Create a Microsoft Entra test user** - to test Microsoft Entra single sign-on with B.Simon.
    1. **Assign the Microsoft Entra test user** - to enable B.Simon to use Microsoft Entra single sign-on.
1. **[Configure Zoho One SSO](#configure-zoho-one-sso)** - to configure the single sign-on settings on application side.
    1. **[Create Zoho One test user](#create-zoho-one-test-user)** - to have a counterpart of B.Simon in Zoho One that's linked to the Microsoft Entra representation of user.
1. **[Test SSO](#test-sso)** - to verify whether the configuration works.

<a name='configure-azure-ad-sso'></a>

## Configure Microsoft Entra SSO

Follow these steps to enable Microsoft Entra SSO.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](~/identity/role-based-access-control/permissions-reference.md#cloud-application-administrator).
1. Browse to **Entra ID** > **Enterprise apps** > **Zoho One** > **Single sign-on**.
1. On the **Select a single sign-on method** page, select **SAML**.
1. On the **Set up single sign-on with SAML** page, select the pencil icon for **Basic SAML Configuration** to edit the settings.

   ![Edit Basic SAML Configuration](common/edit-urls.png)

1. On the **Basic SAML Configuration** section, if you wish to configure the application in **IDP** initiated mode, perform the following steps:

    a. In the **Identifier** text box, type the value:
    `one.zoho.com`

    b. In the **Reply URL** text box, type a URL using the following pattern:
    `https://accounts.zoho.com/samlresponse/<saml-identifier>`

	> [!NOTE]
	> The preceding **Reply URL** value isn't real. You get the `<saml-identifier>` value from #step4 of **Configure Zoho One Single Sign-On** section, which is explained later in the article.

	c. Select **Set additional URLs**.

	d. In the **Relay State** text box, type the URL:
    `https://one.zoho.com`

1. If you wish to configure the application in **SP** initiated mode, perform the following step:

    In the **Sign-on URL** text box, type a URL using the following pattern:
    `https://accounts.zoho.com/samlauthrequest/<domain_name>?serviceurl=https://one.zoho.com` 

    > [!NOTE] 
	> The preceding **Sign-on URL** value isn't real. You update the value with the actual Sign-On URL from the **Configure Zoho One Single Sign-On** section, which is explained later in the article. 

1. On the **Set up Single Sign-On with SAML** page, in the **SAML Signing Certificate** section, select **Download** to download the **Certificate (Base64)** from the given options as per your requirement and save it on your computer.

	![The Certificate download link](common/certificatebase64.png)

1. On the **Set up Zoho One** section, copy the appropriate URL(s) as per your requirement.

	![Copy configuration URLs](common/copy-configuration-urls.png)

<a name='create-an-azure-ad-test-user'></a>

[!INCLUDE [create-assign-users-sso.md](~/identity/saas-apps/includes/create-assign-users-sso.md)]

## Configure Zoho One SSO

1. In a different web browser window, sign in to your Zoho One company site as an administrator.

2. On the **Organization** tab, Select **Setup** under **SAML Authentication**.

	![Zoho One org](./media/zoho-one-tutorial/set-up.png)

3. On the Pop-up page perform the following steps:

	![Zoho One sig](./media/zoho-one-tutorial/save.png)

	a. In the **Sign-in URL** textbox, paste the value of **Login URL**.

	b. In the **Sign-out URL** textbox, paste the value of **Logout URL**.

	c. Select **Browse** to upload the **Certificate (Base64)** which you have downloaded previously.

	d. Select **Save**.

4. After saving the SAML Authentication setup, copy the **SAML-Identifier** value and append it with the **Reply URL** in place of `<saml-identifier>`, like `https://accounts.zoho.com/samlresponse/one.zoho.com` and paste the generated value in the **Reply URL** textbox under **Basic SAML Configuration** section.

	![Zoho One saml](./media/zoho-one-tutorial/saml-identifier.png)

5. Go to the **Domains** tab and then select **Add Domain**.

	![Zoho One domain](./media/zoho-one-tutorial/add-domain.png)

6. On the **Add Domain** page, perform the following steps:

	![Zoho One add domain](./media/zoho-one-tutorial/add-domain-name.png)

	a. In the **Domain Name** textbox, type domain like contoso.com.

	b. Select **Add**.

	>[!Note]
	>After adding the domain follow [these](https://www.zoho.com/one/help/admin-guide/domain-verification.html) steps to verify your domain. Once the domain is verified, use your domain name in **Sign-on URL** in **Basic SAML Configuration** section in Azure portal.

### Create Zoho One test user

To enable Microsoft Entra users to sign in to Zoho One, they must be provisioned into Zoho One. In Zoho One, provisioning is a manual task.

**To provision a user account, perform the following steps:**

1. Sign in to Zoho One as a Security Administrator.

2. On the **Users** tab, Select **user logo**.

	![Zoho One user](./media/zoho-one-tutorial/user.png)

3. On the **Add User** page, perform the following steps:

	![Zoho One add user](./media/zoho-one-tutorial/add-user.png)
	
	a. In **Name** text box, enter the name of user like **Britta simon**.
	
	b. In **Email Address** text box, enter the email of user like brittasimon@contoso.com.

	>[!Note]
	>Select your verified domain from the domain list.

	c. Select **Add**.

## Test SSO

In this section, you test your Microsoft Entra single sign-on configuration with following options. 

#### SP initiated:

* Select **Test this application**, this option redirects to Zoho One Sign on URL where you can initiate the login flow.  

* Go to Zoho One Sign-on URL directly and initiate the login flow from there.

#### IDP initiated:

* Select **Test this application**, and you should be automatically signed in to the Zoho One for which you set up the SSO. 

You can also use Microsoft My Apps to test the application in any mode. When you select the Zoho One tile in the My Apps, if configured in SP mode you would be redirected to the application sign on page for initiating the login flow and if configured in IDP mode, you should be automatically signed in to the Zoho One for which you set up the SSO. For more information about the My Apps, see [Introduction to the My Apps](https://support.microsoft.com/account-billing/sign-in-and-start-apps-from-the-my-apps-portal-2f3b1bae-0e5a-4a86-a33e-876fbd2a4510).

## Related content

Once you configure Zoho One you can enforce session control, which protects exfiltration and infiltration of your organization’s sensitive data in real time. Session control extends from Conditional Access. [Learn how to enforce session control with Microsoft Defender for Cloud Apps](/cloud-app-security/proxy-deployment-any-app).
