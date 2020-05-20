---
title: "Grant and Use a Katalon Runtime Engine Offline License"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/re-offline-licenses.html
description:
---
> Only **node-locked** Katalon Runtime Engine (KRE) licenses with a **yearly** billing cycle can be converted to offline licenses.

A KRE license once converted to an offline license binds to a machine until it expires (in **60** days). It would be best if you were careful in deciding to generate an offline license since this decision is irreversible.

There are two roles in this tutorial:

* Owner/Admins of the organization that have purchased KSE licenses.
* Users need offline licenses.

  > Here we only refer to organization roles since a Katalon user may have both roles

### Step 1: Users view and send a machine ID to Owner/Admins

To copy and send the machine ID on which Katalon Studio is executed, Users need to do the following steps:

1. Download and open **Katalon Studio**
2. In the **Katalon Studio Activation** window, click **Offline Activation** to view and copy the machine ID

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-offline-kse-licenses/view-machineid.png" width="494" height="">

3. Send the machine ID to the Organization Owner/Admins

### Step 2: Owner/Admins create and send back offline licenses

* Create an Offline license for the computer that will execute Katalon Studio from the command line:

1. Go to [Katalon TestOps](https://analytics.katalon.com/home)
2. Select **Organization**

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-offline-kse-licenses/orgkat.png" width="356" height="">

3. Select **License > Katalon Runtime Engine- Node-locked**
4. Click **Create Offline License** on the top right corner

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/re-offline-licenses/button.png" width="" height="">

5. Enter a machine ID and click **Create**
6. Confirm your action. The newly created offline license is added to the **Offline Licenses** list.
7. Download the offline license and store it on its machine. The newly created offline license is named `KRE_<machineID>.lic`.

### Step 3: Users use offline licenses

Users can use the KRE offline licenses to execute Katalon Studio/Katalon Studio Enterprise from the command-line and in the offline environment.

* **Execute a single session**: Put the offline license file named `KRE_<machineID>.lic` in the **license** folder.

* **Execute multiple sessions in parallel**: Put multiple license files in the **license** folder.

The **license** folder can be found:

* Windows: **C:\Users\<user_name>\.katalon\license**

  <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/activate-RE/license.png" width="" height="">

* Linux: **/home/<user_name>/.katalon/license**

* macOS: **/Users/<user_name>/.katalon/license**

  > Note: **.katalon** is a hidden folder.
