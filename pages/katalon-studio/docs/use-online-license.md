---
title: "How to Grant Online Licenses"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/use-online-license.html
description:
---

Before assigning a license, the organization Owner/Admin must [add the team member(s) to the organization in the Katalon TestOps](https://docs.katalon.com/katalon-analytics/docs/user-management.html#user-related-permissions). Once added, the Admin can assign a Katalon license to any team member, or withdraw a license if no longer needed.

### Katalon Studio Enterprise

1. In [Katalon TestOps](https://analytics.katalon.com/home), select your **Organization > Licenses**.
2. On **Katalon Studio Enterprise** view, register the on-demand users by adding them to the **Registered Users** list.

   When the registered users activate Katalon Studio Enterprise, the machine IDs are added to the **Online Licenses** list in Katalon TestOps.

   > The number of registered users cannot exceed the license quota.

Learn about [how to create a Katalon Studio Enterprise offline license](https://docs.katalon.com/katalon-studio/docs/how-to-create-kse-offline-license.html).

### Katalon Runtime Engine

Any members of an Organization can use the Katalon Runtime Engine online licenses that the Organization has purchased.

To avoid sessions termination or optimize license usage, the Organization Owner/Admins should remember the following rules:

* Each process accounts for one license.
* The number of parallel processes conducted cannot exceed the license quota.
* The number of registered machines cannot exceed the license quota.
* Users need API Keys to activate an online RE license.

All users of an organization can use RE online licenses as long as the total number of active online licenses does not exceed the license quota.

To run Katalon Studio or Katalon Studio Enterprise with Katalon Runtime Engine, you need to:

1. Log in to your Katalon account on Katalon Studio.
2. In the command generator, generate a command with the auto-filled Katalon API Key and customized information.
3. Copy and paste the generated command into **Terminal** (for macOS/Linux) or **Command Prompt** (for Windows).
4. Open the command prompt and navigate to the folder of Katalon Studio Engine: `katalonc.exe` (Windows), Applications folder (Mac OS), or `katalonc` (Linux) file.

    **macOS:**

    ```groovy
    cd /Applications/Katalon\ Studio\ Engine.app/Contents/MacOS
    ```

5. Enter the following syntax to execute automation test:

    For example: `katalonc -noSplash -runMode=console -consoleLog -noExit -projectPath="C:\Users\Katalon Studio\Project\YourProject.prj" -retry=0 -testSuitePath="Test Suites/TS_RegressionTest" -browserType="Chrome (headless)" -apiKey=abczxzxz`

    > [Katalon API Key](https://docs.katalon.com/katalon-analytics/docs/ka-api-key.html#create-an-api-key) is required for activating RE.
    >
    > Please refer to [Command Syntax](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#katalon-studio-plugins-in-console-mode) for further instructions on working with RE.

For Enterprise users with a private network, you may encounter a situation where you fail to execute test scripts or integrate Katalon Studio due to the network security error. Please contact your IT team to whitelist the following domains:

* store.katalon.com
* update.katalon.com
* analytics.katalon.com
* testops.katalon.com

Learn more about how to install and execute Katalon Runtime Engine [here](https://docs.katalon.com/katalon-studio/docs/install-RE.html).
