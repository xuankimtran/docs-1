---
title: "Grant and Use a Katalon Studio Enterprise Offline License"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/how-to-create-kse-offline-license.html
description: How to grant a Katalon Studio Enterprise offline license 
---

> Only **node-locked** Katalon Studio Enterprise (KSE) licenses with a **yearly** billing cycle can be converted to offline licenses.

A KSE license once converted to an offline license binds to a machine until it expires (in 60 days). It would be best if you were careful in deciding to generate an offline license since this decision is irreversible.

There are two roles in this tutorial:

* Owner/Admins of the organization that have purchased KSE licenses.
* Users need offline licenses.

   > Here we only refer to organization roles since a Katalon user may have both roles.

### Step 1: Users view and send a machine ID to Owner/Admins

To copy and send the machine ID on which Katalon Studio is executed, Users need to do the following steps:

1. Download and open **Katalon Studio**
2. In the **Katalon Studio Activation** window, click **Offline Activation** to view and copy the machine ID

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-offline-kse-licenses/view-machineid.png" width="494" height="">

3. Send the machine ID to the Organization Owner/Admins

### Step 2: Owner/Admins create and send back offline licenses

* Create an Offline license for the computer that will execute Katalon Studio:

1. Go to [Katalon Admin](https://admin.katalon.com/)
2. Select **Organization**

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-offline-kse-licenses/orgkat.png" width="356" height="">

3. Select **License > Katalon Studio Enterprise**
4. Click **Create Offline License** on the top right corner

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-offline-kse-licenses/button.png" width="1424" height="">

5. Enter a machine ID and click **Create**.
6. Confirm your action.

   The newly created offline license is named `KSE_<machineID>.lic` and added to the **Offline Licenses** list.

* Check the machine ID and make sure you download and distribute offline licenses to the right users.

### Step 3: Users use offline licenses

Users can use the KSE offline license to activate and use KSE in the offline environment.

1. In the **Katalon Studio Activation** window, click **Offline Activation**.
2. Browse the license file with the corresponding machine ID.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-offline-kse-licenses/activate.png" width="498" height="">

### Expired Offline License

When an offline license expires, one more license is available for usage. To continue using offline licenses, please generate a new one.
