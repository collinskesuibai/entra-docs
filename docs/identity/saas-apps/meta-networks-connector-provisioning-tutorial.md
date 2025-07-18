---
title: Configure Meta Networks Connector for automatic user provisioning with Microsoft Entra ID
description: Learn how to configure Microsoft Entra ID to automatically provision and de-provision user accounts to Meta Networks Connector.
author: thomasakelo
manager: mwongerapk
ms.service: entra-id
ms.subservice: saas-apps
ms.topic: how-to
ms.date: 03/25/2025
ms.author: thomasakelo
ms.custom: sfi-image-nochange
# Customer intent: As an IT administrator, I want to learn how to automatically provision and deprovision user accounts from Microsoft Entra ID to Meta Networks Connector so that I can streamline the user management process and ensure that users have the appropriate access to Meta Networks Connector.
---

# Configure Meta Networks Connector for automatic user provisioning with Microsoft Entra ID

The objective of this article is to demonstrate the steps to be performed in Meta Networks Connector and Microsoft Entra ID to configure Microsoft Entra ID to automatically provision and de-provision users and/or groups to Meta Networks Connector.

> [!NOTE]
> This article describes a connector built on top of the Microsoft Entra user Provisioning Service. For important details on what this service does, how it works, and frequently asked questions, see [Automate user provisioning and deprovisioning to SaaS applications with Microsoft Entra ID](~/identity/app-provisioning/user-provisioning.md).
>

## Prerequisites

The scenario outlined in this article assumes that you already have the following prerequisites:

[!INCLUDE [common-prerequisites.md](~/identity/saas-apps/includes/common-prerequisites.md)]
* [A Meta Networks Connector tenant](https://www.metanetworks.com/)
* A user account in Meta Networks Connector with Admin permissions.

## Step 1: Plan your provisioning deployment
1. Learn about [how the provisioning service works](~/identity/app-provisioning/user-provisioning.md).
1. Determine who's in [scope for provisioning](~/identity/app-provisioning/define-conditional-rules-for-provisioning-user-accounts.md).
1. Determine what data to [map between Microsoft Entra ID and Meta Networks Connector](~/identity/app-provisioning/customize-application-attributes.md). 


## Assigning users to Meta Networks Connector

Microsoft Entra ID uses a concept called *assignments* to determine which users should receive access to selected apps. In the context of automatic user provisioning, only the users and/or groups that have been assigned to an application in Microsoft Entra ID are synchronized.

Before configuring and enabling automatic user provisioning, you should decide which users and/or groups in Microsoft Entra ID need access to Meta Networks Connector. Once decided, you can assign these users and/or groups to Meta Networks Connector by following the instructions here:
* [Assign a user or group to an enterprise app](~/identity/enterprise-apps/assign-user-or-group-access-portal.md)

## Important tips for assigning users to Meta Networks Connector

* It's recommended that a single Microsoft Entra user is assigned to Meta Networks Connector to test the automatic user provisioning configuration. Additional users and/or groups may be assigned later.

* When assigning a user to Meta Networks Connector, you must select any valid application-specific role (if available) in the assignment dialog. Users with the **Default Access** role are excluded from provisioning.

## Step 2: Configure Meta Networks Connector for provisioning

1. Sign in to your [Meta Networks Connector Admin Console](https://login.metanetworks.com/login/) using your organization name. Navigate to **Administration > API Keys**.

	![Meta Networks Connector Admin Console](media/meta-networks-connector-provisioning-tutorial/apikey.png)

1. Select the plus sign on the upper right side of the screen to create a new **API Key**.
1. Set the **API Key Name** and **API Key Description**.

	:::image type="content" source="media/meta-networks-connector-provisioning-tutorial/keyname.png" alt-text="Screenshot of the Meta Networks Connector Admin Console with highlighted A P I key name and A P I key description values of Microsoft Entra ID and A P I key." border="false":::

1. Turn on **Write** privileges for **Groups** and **Users**.

	![Meta Networks Connector privileges](media/meta-networks-connector-provisioning-tutorial/privileges.png)

1. Select **Add**. Copy the **SECRET** and save it as it's the only time you can view it. This value is entered in the Secret Token field in the Provisioning tab of your Meta Networks Connector application.

	:::image type="content" source="media/meta-networks-connector-provisioning-tutorial/token.png" alt-text="Screenshot of a window telling users that the A P I key was added. The Secret box contains an indecipherable value and is highlighted." border="false":::

1. Add an IdP by navigating to **Administration > Settings > IdP > Create New**.

	![Meta Networks Connector Add IdP](media/meta-networks-connector-provisioning-tutorial/newidp.png)

1. In the **IdP Configuration** page you can **Name** your IdP configuration and choose an **Icon**.

	![Meta Networks Connector IdP Name](media/meta-networks-connector-provisioning-tutorial/idpname.png)

	![Meta Networks Connector IdP Icon](media/meta-networks-connector-provisioning-tutorial/icon.png)

1. Under **Configure SCIM** select the API key name created in the previous steps. Select **Save**.

	![Meta Networks Connector configure SCIM](media/meta-networks-connector-provisioning-tutorial/configure.png)

1. Navigate to **Administration > Settings > IdP tab**. Select the name of the IdP configuration created in the previous steps to view the **IdP ID**. This **ID** is added to the end of **Tenant URL** while entering the value in **Tenant URL** field in the Provisioning tab of your Meta Networks Connector application.

<a name='step-3-add-meta-networks-connector-from-the-azure-ad-application-gallery'></a>

## Step 3: Add Meta Networks Connector from the Microsoft Entra application gallery

Add Meta Networks Connector from the Microsoft Entra application gallery to start managing provisioning to Meta Networks Connector. If you have previously setup Meta Networks Connector for SSO you can use the same application. However, we recommend that you create a separate app when testing out the integration initially. Learn more about adding an application from the gallery [here](~/identity/enterprise-apps/add-application-portal.md). 


	
## Step 4: Define who is in scope for provisioning 

[!INCLUDE [create-assign-users-provisioning.md](~/identity/saas-apps/includes/create-assign-users-provisioning.md)]

## Step 5: Configuring automatic user provisioning to Meta Networks Connector 

This section guides you through the steps to configure the Microsoft Entra provisioning service to create, update, and disable users and/or groups in Meta Networks Connector based on user and/or group assignments in Microsoft Entra ID.

> [!TIP]
> You may also choose to enable SAML-based single sign-on for Meta Networks Connector, following the instructions provided in the [Meta Networks Connector Single sign-on  article](./metanetworksconnector-tutorial.md). Single sign-on can be configured independently of automatic user provisioning, though these two features complement each other

<a name='to-configure-automatic-user-provisioning-for-meta-networks-connector-in-azure-ad'></a>

### To configure automatic user provisioning for Meta Networks Connector in Microsoft Entra ID:

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) as at least a [Cloud Application Administrator](~/identity/role-based-access-control/permissions-reference.md#cloud-application-administrator).
1. Browse to **Entra ID** > **Enterprise apps**

	![Enterprise applications blade](common/enterprise-applications.png)

1. In the applications list, select **Meta Networks Connector**.

	![The Meta Networks Connector link in the Applications list](common/all-applications.png)

1. Select the **Provisioning** tab.

	![Screenshot of the Manage options with the Provisioning option called out.](common/provisioning.png)

1. Set the **Provisioning Mode** to **Automatic**.

	![Screenshot of the Provisioning Mode dropdown list with the Automatic option called out.](common/provisioning-automatic.png)

1. Under the **Admin Credentials** section, input `https://api.metanetworks.com/v1/scim/<IdP ID>` in **Tenant URL**. Input the **SCIM Authentication Token** value retrieved earlier in **Secret Token**. Select **Test Connection** to ensure Microsoft Entra ID can connect to Meta Networks Connector. If the connection fails, ensure your Meta Networks Connector account has Admin permissions and try again.

	![Tenant URL + Token](common/provisioning-testconnection-tenanturltoken.png)

1. In the **Notification Email** field, enter the email address of a person or group who should receive the provisioning error notifications and check the checkbox - **Send an email notification when a failure occurs**.

	![Notification Email](common/provisioning-notification-email.png)

1. Select **Save**.

1. Under the **Mappings** section, select **Synchronize Microsoft Entra users to Meta Networks Connector**.

1. Review the user attributes that are synchronized from Microsoft Entra ID to Meta Networks Connector in the **Attribute-Mapping** section. The attributes selected as **Matching** properties are used to match the user accounts in Meta Networks Connector for update operations. If you choose to change the [matching target attribute](~/identity/app-provisioning/customize-application-attributes.md), you need to ensure that the Meta Networks Connector API supports filtering users based on that attribute. Select the **Save** button to commit any changes.

    |Attribute|Type|Supported for filtering|Required by Meta Networks Connector|
    |---|---|---|---|
    |userName|String|&check;|&check;
	|active|Boolean||
	|phonenumbers[type eq "work"].value|String||
    |name.givenName|String||&check;
    |name.familyName|String||&check;

	> [!NOTE]
	> phonenumbers value should be in E164 format. For example +16175551212

1. Under the **Mappings** section, select **Synchronize Microsoft Entra groups to Meta Networks Connector**.

1. Review the group attributes that are synchronized from Microsoft Entra ID to Meta Networks Connector in the **Attribute-Mapping** section. The attributes selected as **Matching** properties are used to match the user accounts in Meta Networks Connector for update operations. If you choose to change the [matching target attribute](~/identity/app-provisioning/customize-application-attributes.md), you need to ensure that the Meta Networks Connector API supports filtering users based on that attribute. Select the **Save** button to commit any changes.

    |Attribute|Type|Supported for filtering|Required by Meta Networks Connector|
    |---|---|---|---|
    |displayName|String|&check;|&check;
    |members|Reference||

1. To configure scoping filters, refer to the following instructions provided in the [Scoping filter  article](~/identity/app-provisioning/define-conditional-rules-for-provisioning-user-accounts.md).

1. To enable the Microsoft Entra provisioning service for Meta Networks Connector, change the **Provisioning Status** to **On** in the **Settings** section.

	![Provisioning Status Toggled On](common/provisioning-toggle-on.png)

1. Define the users and/or groups that you would like to provision to Meta Networks Connector by choosing the desired values in **Scope** in the **Settings** section.

	![Provisioning Scope](common/provisioning-scope.png)

1. When you're ready to provision, select **Save**.

	![Saving Provisioning Configuration](common/provisioning-configuration-save.png)

This operation starts the initial synchronization of all users and/or groups defined in **Scope** in the **Settings** section. The initial sync takes longer to perform than subsequent syncs, which occur approximately every 40 minutes as long as the Microsoft Entra provisioning service is running. You can use the **Synchronization Details** section to monitor progress and follow links to provisioning activity report, which describes all actions performed by the Microsoft Entra provisioning service on Meta Networks Connector.

## Step 6: Monitor your deployment

[!INCLUDE [monitor-deployment.md](~/identity/saas-apps/includes/monitor-deployment.md)]

## Change Log
04/06/2022 - Added support for **phoneNumbers[type eq "work"].value**. Removed support for **emails[type eq "work"].value** and **manager** . **name.givenName** and **name.familyName** made required attributes.

## More resources

* [Managing user account provisioning for Enterprise Apps](~/identity/app-provisioning/configure-automatic-user-provisioning-portal.md)
* [What is application access and single sign-on with Microsoft Entra ID?](~/identity/enterprise-apps/what-is-single-sign-on.md)

## Related content

* [Learn how to review logs and get reports on provisioning activity](~/identity/app-provisioning/check-status-user-account-provisioning.md)
