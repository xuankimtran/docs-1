---
title: "Slack Plugin Integration" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/slack-plugin-integration.html
redirect_from:
    - "/katalon-studio/docs/slack-integration.html"
    - "/display/KD/Slack+Integration/"
    - "/display/KD/Slack%20Integration/"
    - "/x/boUw/"
    - "/katalon-studio/docs/slack-integration/"
description: 
---

Slack Integration Plugin allows you to receive test execution with Katalon Studio in real-time.

This plugin is supporting both public and private channels at the moment. With the plugin, all test results in Katalon Studio will be automatically transferred to your desired Slack channels.

This guide shows you how to create a Slack API app and configure Slack Integration Plugin in Katalon Studio.

> Requirements:
>
> * An active Katalon Studio Enterprise license.
> * A Slack workspace already configured.

## Create a Slack API app for integration

1. To create a Slack API app, open a Slack workspace and navigate to the [Slack API app](https://api.slack.com/apps) site to create a new app from scratch.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/slack-plugin-integration/Slack-create-app-from-scratch.png" width=70% alt="Create an app from scratch">

2. Next, you need to configure the app. In the **Feature** sidebar, navigate to the **OAuth & Permissions** section, scroll down to the **Scopes** pane and add these **Bot Token Scopes**: `app_mentions:read`, `calls:write`, `chat:write`, and `chat:write.customize`.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/slack-plugin-integration/Slack-add-scope.png" width=70% alt="Add scopes">

3. To install the app, scroll up to the **OAuth Tokens for Your Workspace** pane and click on the **Install to Workspace** button. 

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/slack-plugin-integration/Slack-app-api-install-app.png" width=70% alt="Install to Workspace button">

4. After the installation, a **Bot User OAuth Token** is displayed. Click on the **Copy** button to copy the token to your clipboard.

    Katalon Studio requires this token to integrate with a Slack API app.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/slack-plugin-integration/Slack-bot-OAuth-token.png" width=70% alt="Copy the OAuth token">

5. Select a channel in your Slack workspace. In the message field, type in "`/invite`" and select **Add apps to this channel**. Enter your app's name.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/slack-plugin-integration/Slack-add-app-to-channel.png" width=70% alt="Add apps to this channel">

## Enable Slack Integration

1. Install the [Slack Integration](https://store.katalon.com/product/4/Slack-Integration) plugin from Katalon Store. After installing the plugin, open Katalon Studio and select **Your Account > Reload Plugins**.
    You can refer to the [Reload Plugins](https://docs.katalon.com/katalon-store/docs/user/access-store-in-KS.html#reload-plugins) for detailed instructions.

2. In the main menu, select **Project > Settings > Plugin > Slack**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/slack-plugin-integration/KS-Settings-Slack.png" width=70% alt="KS Slack settings">

3. To enable Slack Integration, check the **Using Slack** checkbox.

4. In the **Authentication** section, input the required information:
* **Authentication Token**: The **Bot User OAuth Token** of your Slack API app.
* **Channel/Group**: The Slack channel where the app is added.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/slack-plugin-integration/KS-Slack-plugin-input.png" width=70% alt="Slack settings input">

5. Click the **Test Connection** button to ensure Katalon Studio is integrated with the Slack API app. Click **Apply** when done.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/slack-plugin-integration/KS-Slack-plugin-test-connection.png" width=70% alt="Check Slack connection">

6. After the configuration, whenever an execution in KS is finished, your Slack API app will automatically send real-time summary execution results to the configured Slack channel.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/slack-plugin-integration/Slack-Test-result-summary.png" width=70% alt="Configure Slack plugin">
