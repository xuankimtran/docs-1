---
title: "Grant Katalon Licenses"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/use-online-license.html
redirect_from:
  - "/katalon-studio/docs/online-offline-licenses.html"
  - "/katalon-studio/docs/re-offline-licenses.html"
  - "/katalon-studio/docs/how-to-create-kse-offline-license.html"
description:
---

## Online and offline licenses

### Online licenses

An **online license** of Katalon Studio Enterprise (KSE) and Katalon Runtime Engine (KRE) is transferable among registered users of an organization as long as the number of active licenses does not exceed the license quota.

### Offline licenses

An **offline license** allows you to use KSE and KRE without internet. Once you activate an offline license, you cannot revoke or transfer it to a different machine. An offline license expires at the end of your subscription period. It can also be expired earlier than its actual date if you make changes in the offline license file.

When an offline license expires, you can generate a new offline license file to continue using KSE/KRE offline, or you can switch to an online license instead.

> Notes:
>
> You can only convert an annual node-locked license into an offline license.

As a machine ID is required to create an offline license, Katalon generates a machine ID based on the hardware specifications and the user's account logging in to that machine at the generation time.

For example, if User A logs in to Machine A, Katalon generates a machine ID X. At the same time, if User B logs in to Machine A, Katalon generates a machine ID Y. This means that you need two licenses to use KSE/KRE in this case.

## Grant an online license

> Requirements:
>
> You must add team members to your Organization. See: [TestOps User Management](https://docs.katalon.com/katalon-analytics/docs/kt_invite_user_org.html#invite-a-user-to-join-an-organization).
>
> The Owner or Admin of an Organization can grant licenses to any team member. The Owner or Admin can also revoke this action anytime.

### For Katalon Studio Enterprise

Follow these steps:

1. Sign in to [Katalon TestOps](https://testops.katalon.io/login), then go to **Settings** > **License Management**.

    The **Licenses** page appears as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/license-mgt/license.png" width=100% alt="license page">

2. Choose between KSE (Node-locked) and KSE (Floating).

3. Grant an online license to users by adding them in the **Licensed Users** section.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/license-mgt/grant%20.png" width=100% alt="licensed user section">

   Once the licensed users activate KSE, their machine IDs are added in the **Online Licenses** section.

   > Notes:
   >
   > The number of licensed users cannot exceed the license quota.

### For Katalon Runtime Engine

All members of an Organization can use the KRE online licenses as long as the total number of active online licenses does not exceed the license quota.

To optimize license usage and avoid session termination, the Owner and Admin must remember the following rules:

* Each session accounts for one license.
* The number of parallel sessions cannot exceed the license quota.
* The number of registered machine IDs cannot exceed the license quota.
* Users need [API Keys](https://docs.katalon.com/katalon-studio/docs/katalon-apikey-70.html) to activate a KRE online license.

To run KSE using KRE, follow these steps:

1. Open Katalon Studio and log in to your account.

2. In the command generator, generate a command with the auto-filled Katalon API Key and customized information.

    > Notes:
    >
    > From **version 7.7 onwards**, if you belong to more than one Organization purchasing KRE licenses, you can choose which organization to validate your license usage. Katalon retrieves and displays the organizations bound to your Katalon account. Once you have selected an Organization, you pass the Organization ID to the generated command (`-orgID=<Katalon_OrgID>`).

3. Copy and paste the generated command into the Terminal (for MacOS/Linux) or Command Prompt (for Windows).

4. Open the Terminal/Command Prompt and navigate to the Katalon Studio Engine folder `katalonc.exe` (for Windows), or Applications folder (for MacOS), or `katalonc` file (for Linux).

    For example, for MacOS:

    ```groovy
    cd /Applications/Katalon\ Studio\ Engine.app/Contents/MacOS
    ```

5. Enter the following syntax to execute test automation:

    `katalonc -noSplash -runMode=console -consoleLog -noExit -projectPath="C:\Users\Katalon Studio\Project\YourProject.prj" -retry=0 -testSuitePath="Test Suites/TS_RegressionTest" -browserType="Chrome (headless)" -apiKey=abczxzxz -orgID=123xx`

    > Notes:
    >
    > See [Command Syntax](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#katalon-studio-plugins-in-console-mode) for further instructions on working with KRE.

For an Enterprise user with a private network, you might encounter a situation where you fail to execute test scripts or integrate Katalon Studio due to the network security error. In such case, contact your IT team to whitelist the following domains:

* store.katalon.com
* update.katalon.com
* analytics.katalon.com
* testops.katalon.io
* admin.katalon.com
* katalon-test.s3-accelerate.amazonaws.com (used for uploading reports to Katalon TestOps).

See also [Install Runtime Engine](https://docs.katalon.com/katalon-studio/docs/install-RE.html) for installing and executing KRE.

## Grant an offline license

> Notes:
>
> You can only convert node-locked licenses which have a **yearly** billing cycle to offline licenses.
>
> A KSE/KRE license, once converted to an offline license, is bound to a machine until its expiry date (in **60 days**). You should generate an offline license with cautions as you cannot undo this action.

This tutorial is for:

* The Owner/Admins of an Organization that has purchased KSE/KRE licenses.
* Users who need offline licenses.

### Step 1: Users view and send a machine ID to the Owner/Admins

As an user, you need to copy the machine ID on which you use Katalon Studio, then send the machine ID to your Owner/Admins.

Follow these steps:

1. Download and open Katalon Studio.
2. In the **Katalon Studio Enterprise Activation** log, click **Offline Activation** to view and copy the machine ID.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-offline-kse-licenses/view-machineid.png" width="494" height="" alt="kse activation log">

3. Send the machine ID to the Owner/Admins.

### Step 2: Owner/Admins create offline licenses and send them to Users

As an Owner/Admin, you create an offline license by following these steps:

1. Sign in to [Katalon TestOps](https://admin.katalon.com/).
2. Go to **Settings** > **License Management**.
3. Choose between KSE (Node-locked) and KRE (Node-locked).
4. Click on the **Create Offline License** button at the top right corner.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-offline-kse-licenses/button.png" width="1424" height="" alt="create offline license button">

5. Enter the User's machine ID, then click **Create**.

    > Notes:
    >
    > You should check the machine ID and make sure you download and distribute offline licenses to the right users.

6. Confirm your action.

    For KSE, the newly-created offline license is named `KSE_<machineID>.lic` and added in the **Offline Licenses** section.

    For KRE, the newly-created offline license is named `KRE_<machineID>.lic` and added in the **Offline Licenses** section.

### Step 3: Users use offline licenses

#### For Katalon Studio Enterprise

As an user, you download the offline license and store it in your machine, then follow these steps:

1. In the **Katalon Studio Enterprise Activation** log, click **Offline Activation**.
2. Browse the license file with the corresponding machine ID.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-offline-kse-licenses/activate.png" width="498" height="" alt="kse activation log">

You now can use KSE in an offline environment.

#### For Katalon Runtime Engine

As an user, you can use the KRE offline license to execute KSE from the command-line interface and in the offline environment.

* For **Execute a single session**, put an offline license file (named `KRE_<machineID>.lic`) in the **license** folder.
* For **Execute multiple sessions in parallel**, put multiple offline license files in the **license** folder.

Depending on your operating system, you can find the **license** folder as follows:

* For Windows: **C:\Users\<user_name>\.katalon\license**.

  <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/activate-RE/license.png" width="" height="">

* For Linux: **/home/<user_name>/.katalon/license**

* For MacOS: **/Users/<user_name>/.katalon/license**

  > Notes:
  >
  > **.katalon** is a hidden folder.
  