---
title: Configure Envi MMIS for Single sign-on with Microsoft Entra ID
description: Learn how to configure single sign-on between Microsoft Entra ID and Envi MMIS.
author: nguhiu
manager: mwongerapk
ms.reviewer: celested
ms.service: entra-id
ms.subservice: saas-apps
ms.topic: how-to
ms.date: 03/25/2025
ms.author: gideonkiratu
ms.custom: sfi-image-nochange
# Customer intent: As an IT administrator, I want to learn how to configure single sign-on between Microsoft Entra ID and Envi MMIS so that I can control who has access to Envi MMIS, enable automatic sign-in with Microsoft Entra accounts, and manage my accounts in one central location.
---
# Configure Envi MMIS for Single sign-on with Microsoft Entra ID

In this article,  you learn how to integrate Envi MMIS with Microsoft Entra ID. When you integrate Envi MMIS with Microsoft Entra ID, you can:

* Control in Microsoft Entra ID who has access to Envi MMIS.
* Enable your users to be automatically signed-in to Envi MMIS with their Microsoft Entra accounts.
* Manage your accounts in one central location.

## Prerequisites

The scenario outlined in this article assumes that you already have the following prerequisites:

[!INCLUDE [common-prerequisites.md](~/identity/saas-apps/includes/common-prerequisites.md)]
* Envi MMIS single sign-on (SSO) enabled subscription.

## Scenario description

In this article,  you configure and test Microsoft Entra single sign-on in a test environment.

* Envi MMIS supports **SP** and **IDP** initiated SSO.

## Add Envi MMIS from the gallery

To configure the integration of Envi MMIS into Microsoft Entra ID, you need to add Envi MMIS from the gallery to your list of managed SaaS apps.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](~/identity/role-based-access-control/permissions-reference.md#cloud-application-administrator).
1. Browse to **Entra ID** > **Enterprise apps** > **New application**.
1. In the **Add from the gallery** section, type **Envi MMIS** in the search box.
1. Select **Envi MMIS** from results panel and then add the app. Wait a few seconds while the app is added to your tenant.

 [!INCLUDE [sso-wizard.md](~/identity/saas-apps/includes/sso-wizard.md)]

<a name='configure-and-test-azure-ad-sso-for-envi-mmis'></a>

## Configure and test Microsoft Entra SSO for Envi MMIS

Configure and test Microsoft Entra SSO with Envi MMIS using a test user called **B.Simon**. For SSO to work, you need to establish a link relationship between a Microsoft Entra user and the related user in Envi MMIS.

To configure and test Microsoft Entra SSO with Envi MMIS, perform the following steps:

1. **[Configure Microsoft Entra SSO](#configure-azure-ad-sso)** - to enable your users to use this feature.
    1. **Create a Microsoft Entra test user** - to test Microsoft Entra single sign-on with B.Simon.
    1. **Assign the Microsoft Entra test user** - to enable B.Simon to use Microsoft Entra single sign-on.
1. **[Configure Envi MMIS SSO](#configure-envi-mmis-sso)** - to configure the single sign-on settings on application side.
    1. **[Create Envi MMIS test user](#create-envi-mmis-test-user)** - to have a counterpart of B.Simon in Envi MMIS that's linked to the Microsoft Entra representation of user.
1. **[Test SSO](#test-sso)** - to verify whether the configuration works.

<a name='configure-azure-ad-sso'></a>

## Configure Microsoft Entra SSO

Follow these steps to enable Microsoft Entra SSO.

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](~/identity/role-based-access-control/permissions-reference.md#cloud-application-administrator).
1. Browse to **Entra ID** > **Enterprise apps** > **Envi MMIS** > **Single sign-on**.
1. On the **Select a single sign-on method** page, select **SAML**.
1. On the **Set up single sign-on with SAML** page, select the pencil icon for **Basic SAML Configuration** to edit the settings.

   ![Edit Basic SAML Configuration](common/edit-urls.png)

1. On the **Basic SAML Configuration** section, If you wish to configure the application in **IDP** initiated mode, perform the following steps:

    1. In the **Identifier** text box, type a URL using the following pattern:
    `https://www.<CUSTOMER DOMAIN>.com/Account`

    1. In the **Reply URL** text box, type a URL using the following pattern:
    `https://www.<CUSTOMER DOMAIN>.com/Account/Acs`

1. Select **Set additional URLs** and perform the following step if you wish to configure the application in **SP** initiated mode:

    In the **Sign-on URL** text box, type a URL using the following pattern:
    `https://www.<CUSTOMER DOMAIN>.com/Account`

    > [!NOTE]
    > These values aren't real. Update these values with the actual Identifier, Reply URL and Sign-on URL. Contact [Envi MMIS Client support team](mailto:support@ioscorp.com) to get these values. You can also refer to the patterns shown in the **Basic SAML Configuration** section.

1. On the **Set-up Single Sign-On with SAML** page, in the **SAML Signing Certificate** section, select **Download** to download the **Federation Metadata XML** from the given options as per your requirement and save it on your computer.

    ![The Certificate download link](common/metadataxml.png)

1. On the **Set up Envi MMIS** section, copy the appropriate URL(s) as per your requirement.

    ![Copy configuration URLs](common/copy-configuration-urls.png)

<a name='create-an-azure-ad-test-user'></a>

[!INCLUDE [create-assign-users-sso.md](~/identity/saas-apps/includes/create-assign-users-sso.md)]

## Configure Envi MMIS SSO

1. In a different web browser window, sign into your Envi MMIS site as an administrator.

2. Select **My Domain** tab.

    ![Screenshot that shows the "User" menu with "My Domain" selected.](./media/envimmis-tutorial/domain.png)

3. Select **Edit**.

    ![Screenshot that shows the "Edit" button selected.](./media/envimmis-tutorial/edit-icon.png)

4. Select **Use remote authentication** checkbox and then select **HTTP Redirect** from the **Authentication Type** dropdown.

    ![Screenshot that shows the "Details" tab with "Use remote authentication" checked and "H T T P Redirect" selected.](./media/envimmis-tutorial/details.png)

5. Select **Resources** tab and then select **Upload Metadata**.

    ![Screenshot that shows the "Resources" tab with the "Upload Metadata" action selected.](./media/envimmis-tutorial/metadata.png)

6. In the **Upload Metadata** pop-up, perform the following steps:

    ![Screenshot that shows the "Upload Metadata" pop-up with the "File" option selected and the "choose file" icon and "OK" button highlighted.](./media/envimmis-tutorial/file.png)

    1. Select **File** option from the **Upload From** dropdown.

    1. Upload the downloaded metadata file from Azure portal by selecting the **choose file icon**.

    1. Select **Ok**.

7. After uploading the downloaded metadata file, the fields gets populated automatically. Select **Update**.

    ![Configure Single Sign-On Save button](./media/envimmis-tutorial/fields.png)

### Create Envi MMIS test user

To enable Microsoft Entra users to sign in to Envi MMIS, they must be provisioned into Envi MMIS. In the case of Envi MMIS, provisioning is a manual task.

**To provision a user account, perform the following steps:**

1. Sign in to your Envi MMIS company site as an administrator.

2. Select **User List** tab.

    ![Screenshot that shows the "User" menu with "User List" selected.](./media/envimmis-tutorial/list.png)

3. Select **Add User** button.

    ![Screenshot that shows the "Users" section with the "Add User" button selected.](./media/envimmis-tutorial/user.png)

4. In the **Add User** section, perform the following steps:

    ![Screenshot that shows to Add Employee.](./media/envimmis-tutorial/add-user.png)

    1. In the **User Name** textbox, type the username of Britta Simon account like **brittasimon\@contoso.com**.
    
    1. In the **First Name** textbox, type the first name of BrittaSimon like **Britta**.

    1. In the **Last Name** textbox, type the last name of BrittaSimon like **Simon**.

    1. Enter the Title of the user in the **Title** of the textbox.

    1. In the **Email Address** textbox, type the email address of Britta Simon account like **brittasimon\@contoso.com**.

    1. In the **SSO User Name** textbox, type the username of Britta Simon account like **brittasimon\@contoso.com**.

    1. Select **Save**.

## Test SSO

In this section, you test your Microsoft Entra single sign-on configuration with following options. 

#### SP initiated:

* Select **Test this application**, this option redirects to Envi MMIS Sign on URL where you can initiate the login flow.  

* Go to Envi MMIS Sign-on URL directly and initiate the login flow from there.

#### IDP initiated:

* Select **Test this application**, and you should be automatically signed in to the Envi MMIS for which you set up the SSO. 

You can also use Microsoft My Apps to test the application in any mode. When you select the Envi MMIS tile in the My Apps, if configured in SP mode you would be redirected to the application sign on page for initiating the login flow and if configured in IDP mode, you should be automatically signed in to the Envi MMIS for which you set up the SSO. For more information about the My Apps, see [Introduction to the My Apps](https://support.microsoft.com/account-billing/sign-in-and-start-apps-from-the-my-apps-portal-2f3b1bae-0e5a-4a86-a33e-876fbd2a4510).

## Related content

Once you configure Envi MMIS you can enforce session control, which protects exfiltration and infiltration of your organization’s sensitive data in real time. Session control extends from Conditional Access. [Learn how to enforce session control with Microsoft Defender for Cloud Apps](/cloud-app-security/proxy-deployment-aad).
