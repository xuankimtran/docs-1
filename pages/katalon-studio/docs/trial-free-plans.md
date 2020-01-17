---
title: "Katalon Trial and Free Plans"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/trial-free-plans.html
description:
---

## Trial License

Valid email registration is eligible for a **30-day** trial of both **Katalon Studio Enterprise** and **Katalon Runtime Engine**'s floating licenses. The trial licenses are automatically generated and activated when you first log into the Katalon Studio application.

Each trial license can be activated on only one machine at a time. When your trial period expires, you need to subscribe to the paid license of each product to continue using it. Otherwise, the Katalon Studio free license will be automatically activated.

> Katalon Studio Enterprise and Katalon Runtime Engine **trial** licenses can only be registered with **business** emails. Trial licenses do NOT support offline activation and usage.

To purchase licenses, please follow [this instruction](https://docs.katalon.com/katalon-studio/docs/license-subscription.html).

### Activate Katalon Studio Enterprise with Trial License

1. Download and Open Katalon Studio.
2. Log into your Katalon account. The trial is automatically activated for Katalon users with a business email.

You can start using Katalon Studio Enterprise for 30 days.

### Activate Katalon Runtime Engine with Trial License

> Trial licenses only work in online environments.

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

## Free License

The free license granted for each Katalon account only includes the standard Katalon Studio with starter features. Currently, the free license for Katalon Runtime Engine is not available. If you wish to execute Katalon Studio in console mode, you need to subscribe to a Katalon Runtime Engine license. You can upgrade the free Katalon Studio to Katalon Studio Enterprise with a paid license without having to re-download.
