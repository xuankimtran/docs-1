---
title: "Activate Runtime Engine"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/activate-RE.html
description:
---

Starting from **version 7.0.0**, you need a Runtime Engine (RE) [license](https://docs.katalon.com/katalon-studio/docs/license.html) to activate and run Katalon Studio (KS) or Katalon Studio Enterprise (KSE) from the command line.

Currently, free license is not available for Runtime Engine.

## With Trial License

> Trial licenses only work in online environments.

To run KS/KSE with RE, you need to:

1. Log in to your Katalon account on Katalon Studio.
2. In the command generator, generate a command with the auto-filled Katalon API Key and customized information.
3. Copy and paste the generated command into **Terminal** (for macOS/Linux users) or **Command Prompt** (for Windows users).

    For example: `katalonc -noSplash -runMode=console -consoleLog -noExit -projectPath="C:\Users\Katalon Studio\Project\YourProject.prj" -retry=0 -testSuitePath="Test Suites/TS_RegressionTest" -browserType="Chrome (headless)" -apiKey=abczxzxz`

    > [Katalon API Key](https://docs.katalon.com/katalon-analytics/docs/ka-api-key.html#create-an-api-key) is required for activating RE.
    >
    > Please refer to [Command Syntax](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#katalon-studio-plugins-in-console-mode) for further instructions on working with RE.

## With Paid License

For a detailed introduction to our licenses, refer to [this document](https://docs.katalon.com/katalon-studio/docs/license.html).

### Online License

* You need API Keys to activate an online RE license.
* Each process accounts for one license.
* The number of parallel processes conducted cannot exceed the license quota.
* The number of registered machines cannot exceed the license quota.

All users of an organization can use RE online licenses as long as the total number of active online licenses does not exceed the license quota.

For Enterprise users with a private network, you may encounter a situation where you fail to execute test scripts or integrate Katalon Studio due to the network security error. Please contact your IT team to whitelist the following domains:

* store.katalon.com
* update.katalon.com
* analytics.katalon.com
* testops.katalon.com

### Offline License

Offline license is only available for annual subscription. The valid period for each offline license is 60 days.

1. In [Katalon TestOps](https://analytics.katalon.com/home), go to **Organization > License > Runtime Engine**.
2. Create an offline license with a computer ID that can be viewed in the Katalon Studio Activation window. The computer registered with Katalon Server is added to the **Registered Machines** list.
3. Download the offline license and put it in the `license` folder. For Runtime Engine, one machine can run multiple parallel sessions simultaneously by putting multiple licenses in the `license` folder.

For Windows users: **C:\Users\<user_name>\.katalon\license**

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/activate-RE/license.png" width="" height="">

For Linux users: **/home/<user_name>/.katalon/license**

For Mac users: **/Users/<user_name>/.katalon/license**

> Note: The `.katalon` folder is a hidden folder.
