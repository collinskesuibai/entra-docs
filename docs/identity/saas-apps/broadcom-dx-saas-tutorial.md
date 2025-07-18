---
title: Configure Broadcom DX SaaS for Single sign-on with Microsoft Entra ID
description: Learn how to configure single sign-on between Microsoft Entra ID and Broadcom DX SaaS.
author: nguhiu
manager: mwongerapk
ms.reviewer: CelesteDG
ms.service: entra-id
ms.subservice: saas-apps
ms.topic: how-to
ms.date: 03/25/2025
ms.author: gideonkiratu
ms.custom: sfi-image-nochange
# Customer intent: As an IT administrator, I want to learn how to configure single sign-on between Microsoft Entra ID and Broadcom DX SaaS so that I can control who has access to Broadcom DX SaaS, enable automatic sign-in with Microsoft Entra accounts, and manage my accounts in one central location.
---

# Configure Broadcom DX SaaS for Single sign-on with Microsoft Entra ID

In this article,  you learn how to integrate Broadcom DX SaaS with Microsoft Entra ID. When you integrate Broadcom DX SaaS with Microsoft Entra ID, you can:

* Control in Microsoft Entra ID who has access to Broadcom DX SaaS.
* Enable your users to be automatically signed-in to Broadcom DX SaaS with their Microsoft Entra accounts.
* Manage your accounts in one central location.

## Prerequisites

The scenario outlined in this article assumes that you already have the following prerequisites:

[!INCLUDE [common-prerequisites.md](~/identity/saas-apps/includes/common-prerequisites.md)]
* Broadcom DX SaaS single sign-on (SSO) enabled subscription.

> [!NOTE]
> This integration is also available to use from Microsoft Entra US Government Cloud environment. You can find this application in the Microsoft Entra US Government Cloud Application Gallery and configure it in the same way as you do from public cloud.

## Scenario description

In this article,  you configure and test Microsoft Entra SSO in a test environment.

* Broadcom DX SaaS supports **IDP** initiated SSO.

* Broadcom DX SaaS supports **Just In Time** user provisioning.

> [!NOTE]
> Identifier of this application is a fixed string value so only one instance can be configured in one tenant.

## Add Broadcom DX SaaS from the gallery

To configure the integration of Broadcom DX SaaS into Microsoft Entra ID, you need to add Broadcom DX SaaS from the gallery to your list of managed SaaS apps.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](~/identity/role-based-access-control/permissions-reference.md#cloud-application-administrator).
1. Browse to **Entra ID** > **Enterprise apps** > **New application**.
1. In the **Add from the gallery** section, type **Broadcom DX SaaS** in the search box.
1. Select **Broadcom DX SaaS** from results panel and then add the app. Wait a few seconds while the app is added to your tenant.

 [!INCLUDE [sso-wizard.md](~/identity/saas-apps/includes/sso-wizard.md)]


<a name='configure-and-test-azure-ad-sso-for-broadcom-dx-saas'></a>

## Configure and test Microsoft Entra SSO for Broadcom DX SaaS

Configure and test Microsoft Entra SSO with Broadcom DX SaaS using a test user called **B.Simon**. For SSO to work, you need to establish a link relationship between a Microsoft Entra user and the related user in Broadcom DX SaaS.

To configure and test Microsoft Entra SSO with Broadcom DX SaaS, perform the following steps:

1. **[Configure Microsoft Entra SSO](#configure-azure-ad-sso)** - to enable your users to use this feature.
    1. **Create a Microsoft Entra test user** - to test Microsoft Entra single sign-on with B.Simon.
    1. **Assign the Microsoft Entra test user** - to enable B.Simon to use Microsoft Entra single sign-on.
1. **[Configure Broadcom DX SaaS SSO](#configure-broadcom-dx-saas-sso)** - to configure the single sign-on settings on application side.
    1. **[Create Broadcom DX SaaS test user](#create-broadcom-dx-saas-test-user)** - to have a counterpart of B.Simon in Broadcom DX SaaS that's linked to the Microsoft Entra representation of user.
1. **[Test SSO](#test-sso)** - to verify whether the configuration works.

<a name='configure-azure-ad-sso'></a>

## Configure Microsoft Entra SSO

Follow these steps to enable Microsoft Entra SSO.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](~/identity/role-based-access-control/permissions-reference.md#cloud-application-administrator).
1. Browse to **Entra ID** > **Enterprise apps** > **Broadcom DX SaaS** > **Single sign-on**.
1. On the **Select a single sign-on method** page, select **SAML**.
1. On the **Set up single sign-on with SAML** page, select the pencil icon for **Basic SAML Configuration** to edit the settings.

   ![Edit Basic SAML Configuration](common/edit-urls.png)

1. On the **Set up single sign-on with SAML** page, perform the following steps:

    a. In the **Identifier** text box, type a value using the following pattern:
    `DXI_<TENANT_NAME>`

    b. In the **Reply URL** text box, type a URL using the following pattern:
    `https://axa.dxi-na1.saas.broadcom.com/ess/authn/<TENANT_NAME>`

	> [!NOTE]
	> These values aren't real. Update these values with the actual Identifier and Reply URL. Contact [Broadcom DX SaaS Client support team](mailto:dxi-na1@saas.broadcom.com) to get these values. You can also refer to the patterns shown in the **Basic SAML Configuration** section.

1. Broadcom DX SaaS application expects the SAML assertions in a specific format, which requires you to add custom attribute mappings to your SAML token attributes configuration. The following screenshot shows the list of default attributes.

	![image](common/default-attributes.png)

1. In addition to above, Broadcom DX SaaS application expects few more attributes to be passed back in SAML response, which are shown below. These attributes are also pre populated but you can review them as per your requirements.
	
	| Name |  Source Attribute|
	| --------------- | --------- |
	| Group | user.groups |

1. On the **Set up single sign-on with SAML** page, in the **SAML Signing Certificate** section,  find **Certificate (Base64)** and select **Download** to download the certificate and save it on your computer.

	![The Certificate download link](common/certificatebase64.png)

1. On the **Set up Broadcom DX SaaS** section, copy the appropriate URL(s) based on your requirement.

	![Copy configuration URLs](common/copy-configuration-urls.png)

<a name='create-an-azure-ad-test-user'></a>

[!INCLUDE [create-assign-users-sso.md](~/identity/saas-apps/includes/create-assign-users-sso.md)]

## Configure Broadcom DX SaaS SSO

1. Log in to your Broadcom DX SaaS company site as an administrator.

2. Go to the **Settings** and select **Users** tab.

    ![Users](./media/broadcom-dx-saas-tutorial/settings.png "Users")

3. In the **User management** section, select ellipses and select **SAML**.

    ![User management](./media/broadcom-dx-saas-tutorial/local.png "User management")

4. In the **Identify SAML account** section, perform the  following steps.
   
    ![Account](./media/broadcom-dx-saas-tutorial/broadcom-1.png "Account") 

    a. In the **Issuer** textbox, paste the **Microsoft Entra Identifier** value which you copied previously.

    b. In the **Identity Provider (IDP) Login URL** textbox, paste the **Login URL** value which you copied previously.

    c. In the **Identity Provider (IDP) Logout URL** textbox, paste the **Logout URL** value which you copied previously.

    d. Open the downloaded **Certificate (Base64)** into Notepad and paste the content into the **Identity provider certificate** textbox.

    e. Select **NEXT**.

5. In the **Map attributes** section, fill the required SAML attributes in the following page and select **NEXT**.

    ![Attributes](./media/broadcom-dx-saas-tutorial/broadcom-2.png "Attributes") 


6. In the **Identify user group** section, enter the object ID of that group and select **NEXT**.

    ![Add group](./media/broadcom-dx-saas-tutorial/broadcom-3.png "Add group") 

7. In the **Populate SAML Account** section, verify the populated values and select **SAVE**.

    ![SAML Account](./media/broadcom-dx-saas-tutorial/broadcom-4.png "SAML Account") 

### Create Broadcom DX SaaS test user

In this section, a user called Britta Simon is created in Broadcom DX SaaS. Broadcom DX SaaS supports just-in-time user provisioning, which is enabled by default. There's no action item for you in this section. If a user doesn't already exist in Broadcom DX SaaS, a new one is created after authentication.

## Test SSO 

In this section, you test your Microsoft Entra single sign-on configuration with following options.

* Select **Test this application**, and you should be automatically signed in to the Broadcom DX SaaS for which you set up the SSO.

* You can use Microsoft My Apps. When you select the Broadcom DX SaaS tile in the My Apps, you should be automatically signed in to the Broadcom DX SaaS for which you set up the SSO. For more information about the My Apps, see [Introduction to the My Apps](https://support.microsoft.com/account-billing/sign-in-and-start-apps-from-the-my-apps-portal-2f3b1bae-0e5a-4a86-a33e-876fbd2a4510).

## Related content

Once you configure Broadcom DX SaaS you can enforce session control, which protects exfiltration and infiltration of your organization’s sensitive data in real time. Session control extends from Conditional Access. [Learn how to enforce session control with Microsoft Defender for Cloud Apps](/cloud-app-security/proxy-deployment-any-app).
