---
title: "Activate Runtime Engine"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/activate-RE.html
description:
---

Starting from **version 7.0.0**, you need a license that grants you permission to activate and run Katalon Studio or Katalon Studio Enterprise from the command line.

## With Trial License

> The trial license is only for online environments.

There are two ways for users to execute Katalon Studio/Katalon Studio Enterprise with Runtime Engine.

### Launching Katalon Studio and use the command generator

1. Open Katalon Studio and log in to your Katalon account.
2. In the command generator, generate command with the auto-filled Katalon API Key and customized information.
3. Copy and paste in the Terminal.

### Without launching Katalon Studio

1. Generate Katalon API Key. Click [here](https://docs.katalon.com/katalon-analytics/docs/ka-api-key.html#create-an-api-key) for detailed instructions.
2. Open Terminal (for macOS/Linux users) or Command Prompt (for Windows users), enter the command with API Key generated above. Please refer to the detailed document of [Console Mode Execution](/katalon-studio/docs/console-mode-execution.html#katalon-studio-plugins-in-console-mode) for further instructions.

## With Paid License

### Online License

You need API Keys to activate an online license of RE. Each process accounts for a license. The number of processes conducted at a time cannot exceed the license and machine quotas.

All users belong to an organization can use RE online license as long as the total number of active online licenses does not exceed the license quota.

### Offline License

1. On [Katalon TestOps](https://analytics.katalon.com/home), go to **Organization > License > Runtime Engine**.
2. Create an offline license with a computer ID that can be viewed in the Katalon Studio Activation window. The computer registered with Katalon Server is added to the **Registered Machines** list.
3. Download the offline license and put it in the `license` folder. For Runtime Engine, one machine can run multiple parallel sessions simultaneously by putting multiple licenses in the `license` folder.

For Windows users: **C:\Users\<user_name>\.katalon\license**

For Linux users: **/home/<user_name>/.katalon/license**

For Mac users: **/Users/<user_name>/.katalon/license**

> Note: The `.katalon` folder is a hidden folder.
