---
title: Configure Palo Alto Networks - GlobalProtect for Single sign-on with Microsoft Entra ID
description: Learn how to configure single sign-on between Microsoft Entra ID and Palo Alto Networks - GlobalProtect.

author: nguhiu
manager: mwongerapk
ms.reviewer: celested
ms.service: entra-id
ms.subservice: saas-apps
ms.workload: identity
ms.topic: how-to
ms.date: 05/20/2025
ms.author: gideonkiratu

# Customer intent: As an IT administrator, I want to learn how to configure single sign-on between Microsoft Entra ID and Palo Alto Networks - GlobalProtect so that I can control who has access to Palo Alto Networks - GlobalProtect, enable automatic sign-in with Microsoft Entra accounts, and manage my accounts in one central location.
---

# Configure Palo Alto Networks - GlobalProtect for Single sign-on with Microsoft Entra ID

In this article,  you learn how to integrate Palo Alto Networks - GlobalProtect with Microsoft Entra ID. When you integrate Palo Alto Networks - GlobalProtect with Microsoft Entra ID, you can:

* Control in Microsoft Entra ID who has access to Palo Alto Networks - GlobalProtect.
* Enable your users to be automatically signed-in to Palo Alto Networks - GlobalProtect with their Microsoft Entra accounts.
* Manage your accounts in one central location.

## Prerequisites
The scenario outlined in this article assumes that you already have the following prerequisites:

[!INCLUDE [common-prerequisites.md](~/identity/saas-apps/includes/common-prerequisites.md)]
* Palo Alto Networks - GlobalProtect single sign-on (SSO) enabled subscription.

## Scenario description

In this article,  you configure and test Microsoft Entra SSO in a test environment.

* Palo Alto Networks - GlobalProtect supports **SP** initiated SSO
* Palo Alto Networks - GlobalProtect supports **Just In Time** user provisioning

## Adding Palo Alto Networks - GlobalProtect from the gallery

To configure the integration of Palo Alto Networks - GlobalProtect into Microsoft Entra ID, you need to add Palo Alto Networks - GlobalProtect from the gallery to your list of managed SaaS apps.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](~/identity/role-based-access-control/permissions-reference.md#cloud-application-administrator).
1. Browse to **Entra ID** > **Enterprise apps** > **New application**.
1. In the **Add from the gallery** section, type **Palo Alto Networks - GlobalProtect** in the search box.
1. Select **Palo Alto Networks - GlobalProtect** from results panel and then add the app. Wait a few seconds while the app is added to your tenant.

Alternatively, you can also use the [Enterprise App Configuration Wizard](https://portal.office.com/AdminPortal/home?Q=Docs#/azureadappintegration). In this wizard, you can add an application to your tenant, add users/groups to the app, assign roles, and walk through the SSO configuration as well. [Learn more about Microsoft 365 wizards.](/microsoft-365/admin/misc/azure-ad-setup-guides)

## Configure and test Microsoft Entra SSO for Palo Alto Networks - GlobalProtect

Configure and test Microsoft Entra SSO with Palo Alto Networks - GlobalProtect using a test user called **B.Simon**. For SSO to work, you need to establish a link relationship between a Microsoft Entra user and the related user in Palo Alto Networks - GlobalProtect.

To configure and test Microsoft Entra SSO with Palo Alto Networks - GlobalProtect, perform the following steps:

1. **[Configure Microsoft Entra SSO](#configure-microsoft-entra-sso)** - to enable your users to use this feature.
    1. **Create a Microsoft Entra test user** - to test Microsoft Entra single sign-on with B.Simon.
    1. **Assign the Microsoft Entra test user** - to enable B.Simon to use Microsoft Entra single sign-on.
1. **[Configure Palo Alto Networks - GlobalProtect SSO](#configure-palo-alto-networks---globalprotect-sso)** - to configure the single sign-on settings on application side.
    1. **[Create Palo Alto Networks - GlobalProtect test user](#create-palo-alto-networks---globalprotect-test-user)** - to have a counterpart of B.Simon in Palo Alto Networks - GlobalProtect that's linked to the Microsoft Entra ID representation of user.
1. **[Test SSO](#test-sso)** - to verify whether the configuration works.

## Configure Microsoft Entra SSO

Follow these steps to enable Microsoft Entra SSO.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](~/identity/role-based-access-control/permissions-reference.md#cloud-application-administrator).
1. Browse to **Entra ID** > **Enterprise apps** > **Palo Alto Networks - GlobalProtect** > **Single sign-on**.
1. On the **Select a single sign-on method** page, select **SAML**.
1. On the **Set up single sign-on with SAML** page, select the pencil icon for **Basic SAML Configuration** to edit the settings.

   ![Screenshot shows how to edit Basic SAML Configuration.](common/edit-urls.png "Basic Configuration")

1. On the **Basic SAML Configuration** section, perform the following steps:

    a. In the **Identifier (Entity ID)** text box, type a URL using the following pattern:
    `https://<Customer Firewall URL>/SAML20/SP`

    b. In the **Reply URL (Assertion Consumer Service URL)** text box, type a URL using the following pattern:
   `https://<Customer Firewall URL>/SAML20/SP/ACS`

	c. In the **Sign on URL** text box, type a URL using the following pattern:
    `https://<Customer Firewall URL>`

	> [!NOTE]
	> These values aren't real. Update these values with the actual Identifier, Reply URL and Sign on URL. Contact [Palo Alto Networks - GlobalProtect Client support team](https://support.paloaltonetworks.com/support) to get these values. You can also refer to the patterns shown in the **Basic SAML Configuration** section in the Microsoft Entra admin center.

1. On the **Set up single sign-on with SAML** page, in the **SAML Signing Certificate** section, find **Federation Metadata XML** and select **Download** to download the XML file (which also contains the SAML certificate) and save it on your computer.

	![Screenshot shows the Certificate download link.](common/metadataxml.png "Certificate")

1. On the **Set up Palo Alto Networks - GlobalProtect** section, copy the appropriate URL(s) based on your requirement.

	![Screenshot shows to copy configuration URLs.](common/copy-configuration-urls.png "Metadata")

[!INCLUDE [create-assign-users-sso.md](~/identity/saas-apps/includes/create-assign-users-sso.md)]

## Configure Palo Alto Networks - GlobalProtect SSO

1. Open the Palo Alto Networks - GlobalProtect as an administrator in another browser window.

2. Select **Device**.

	![Configure Palo Alto Single Sign-on 1](./media/paloaltoglobalprotect-tutorial/tutorial_paloaltoadmin_admin1.png)

3. Select **SAML Identity Provider** from the left navigation bar and select "Import" to import the metadata file.

	![Configure Palo Alto Single Sign-on 2](./media/paloaltoglobalprotect-tutorial/tutorial_paloaltoadmin_admin2.png)

4. Perform following actions on the Import window

	![Configure Palo Alto Single Sign-on 3](./media/paloaltoglobalprotect-tutorial/tutorial_paloaltoadmin_admin3.png)

	a. In the **Profile Name** textbox, provide a name, such as Microsoft Entra GlobalProtect.

    b. In **Identity Provider Metadata**, select **Browse** and select the Federation Metadata XML file which you have downloaded from Microsoft Entra admin center.

	c. **Optional:** Uncheck Validate Identity Provider certificate. If checked, the Certificate from Microsoft Entra needs to be uploaded on firewall as well.

	d. Select **OK**

	> [!NOTE]
	> If the upload fails with the error message `Failed to parse IDP Metadata` check that you have the required administrator privileges on the system and that the profile name doesn't exceed 31 characters.

### Create Palo Alto Networks - GlobalProtect test user

In this section, a user called B.Simon is created in Palo Alto Networks - GlobalProtect. Palo Alto Networks - GlobalProtect supports just-in-time user provisioning, which is enabled by default. There's no action item for you in this section. If a user doesn't already exist in Palo Alto Networks - GlobalProtect, a new one is created after authentication.

## Test SSO 

In this section, you test your Microsoft Entra single sign-on configuration with following options. 

* Select **Test this application**, this option redirects to Palo Alto Networks - GlobalProtect Sign-on URL where you can initiate the login flow. 

* Go to Palo Alto Networks - GlobalProtect Sign-on URL directly and initiate the login flow from there.

* You can use Microsoft My Apps. When you select the Palo Alto Networks - GlobalProtect tile in the My Apps, you should be automatically signed in to the Palo Alto Networks - GlobalProtect for which you set up the SSO. For more information about the My Apps, see [Introduction to the My Apps](https://support.microsoft.com/account-billing/sign-in-and-start-apps-from-the-my-apps-portal-2f3b1bae-0e5a-4a86-a33e-876fbd2a4510).

## Related content

Once you configure Palo Alto Networks  - GlobalProtect you can enforce session control, which protects exfiltration and infiltration of your organization’s sensitive data in real time. Session control extends from Conditional Access. [Learn how to enforce session control with Microsoft Defender for Cloud Apps](/cloud-app-security/proxy-deployment-any-app).
