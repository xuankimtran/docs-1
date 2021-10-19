---
title: "Manage Katalon Licenses"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/license-management.html
redirect_from:
    - "/katalon-studio/docs/transfer-license.html"
description:
---
After purchasing Katalon Studio Enterprise and/or Katalon Runtime Engine licenses, you can attribute, transfer, and removegrant licenses from [Katalon TestOps](https://testops.katalon.io/login).

> Requirements:
>
> You must be the Owner or Admin of your Organization to access the **Licenses** page. For further details on roles and user management, see: [TestOps User Management](https://docs.katalon.com/katalon-analytics/docs/kt_invite_user_org.html).

## View the license information

You can verify the subscription information and view all license information by following these steps:

1. Sign in to [Katalon TestOps](https://testops.katalon.io/login).

2. Go to **Settings** > **License Management**.

   The **Licenses** page appears.

3. Select a Katalon product. For example, **Katalon Studio Enterprise (Node-locked)**.

   The **Licenses** page displays as below.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/license-mgt/licenses-page-blurred-not-highlighted.png" width=100% alt="licenses page">

   * In the **Subscription** section, you can see the following information:
      * **Subscribed Licenses**: the total number of licenses you have purchased, also known as your license quota.
      *  **Available Licenses**: the remaining licenses you can use.

         > Notes:
         > 
         > Licenses attributed online, as well as offline licenses you have generated, are substracted from your license quota.

      * **Machine Quota**: the maximum number of machines that can be registered with your licenses.
      
   * In the **Licensed Users** section, you can add users for license usage. You can also view a list of users you have added for license usage.

   * In the **Online Licenses** section, you can see a list of active machine IDs (users who are currently using the licenses online).

   * In the **Offline Licenses** section, you can see a list of machine IDs bound to offline licenses.

   * In the **Registered Machines** section, you can see a list of all machine IDs that are using either types of licenses.

> Notes:
>
> Contact us at license@katalon.com if you need further help with your licenses.

## Grant a license

You can assign licenses to users. See [Grant Katalon Licenses](https://docs.katalon.com/katalon-studio/docs/use-online-license.html).

Once you have assigned a license successfully, users can follow this activation guide: [Activate Katalon License](https://docs.katalon.com/katalon-studio/docs/activate-license.html).

## Remove a license

You can remove a Licensed User, a machine ID, or a license from a machine ID. See [Remove a License](https://docs.katalon.com/katalon-studio/docs/remove-license.html).

## Transfer a license

> Notes:
>
> Only **Online Licenses** are transferable among the organization's registered users as long as the active licenses do not exceed the license quota.
>
> **Offline Licenses** cannot be transferred until their expiry dates.

> Requirements:
>
> You have already verified that your machine does not have an offline license.

After activation, the KSE/KRE node-locked licenses are bound to the machine IDs until the expiry dates. You can still remove the licenses or transfer them manually.

To transfer a KSE license, you need to:

1. Remove a license. See [Remove a License](https://docs.katalon.com/katalon-studio/docs/remove-license.html).
2. Add the new user in the **Online Licenses** section. See: [Grant Katalon Licenses](https://docs.katalon.com/katalon-studio/docs/use-online-license.html).

For KRE, one session will reserve one license. You must deactivate the machine ID that reserved that license first. Another user can then use KRE and take over the license.

For example, if the KRE license is bound to your machine ID because you have run KSE using KRE. You must deactivate your machine ID so that the other member in your organization can use the KRE node-locked license.

### Transfer the KRE license to another machine

All licensed Users in an Organization can use available KRE licenses by default once the Organization has purchased the KRE licenses.

Licensed Users activate a KRE license by running KSE with KRE. After activation, their machine ID is then added to the **Online Licenses** section. This license is then reserved for their use.

Therefore, to make a KRE license available when all licenses are reserved, a machine ID has to be deactivated.

Follow the steps above to deactivate a machine ID.