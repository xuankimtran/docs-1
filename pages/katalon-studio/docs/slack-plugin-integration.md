---
title: "Slack Integration" 
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
> * The **Slack Integration** plugin for Katalon Studio installed. You can find the plugin here: [Katalon Store](https://store.katalon.com/product/4/Slack-Integration). 

## Create a Slack API app for integration

1. To create a Slack API app, open a Slack workspace and navigate to the [Slack API app](https://api.slack.com/apps) site to create a new app from scratch.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/slack-plugin-integration/Slack-create-app-from-scratch.png" width=70% alt="Create an app from scratch">

2. Next, you need to configure the app. In the **Feature** sidebar, navigate to the **OAuth & Permissions** section, scroll down to the **Scopes** pane and add some **Bot Token Scopes**.

    We need to grant the app these scopes: `app_mentions:read`, `calls:write`, `chat:write`, and `chat:write.customize`.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/slack-plugin-integration/Slack-add-scope.png" width=70% alt="Add scopes">

3. To install the app, scroll up to the **OAuth Tokens for Your Workspace** pane and click on the **Install to Workspace** button. 

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/slack-plugin-integration/Slack-app-api-install-app.png" width=70% alt="Install to Workspace button">

4. After the installation, a **Bot User OAuth Token** is displayed. Click on the **Copy** button to copy the token to your clipboard.

    Katalon Studio requires this token to integrate with a Slack API app.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/slack-plugin-integration/Slack-bot-OAuth-token.png" width=70% alt="Copy the OAuth token">

5. Select a channel in your Slack workspace. In the message field, type in "`/invite`" and select **Add apps to this channel**. Enter your app's name.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/slack-plugin-integration/Slack-add-app-to-channel.png" width=70% alt="Add apps to this channel">

## Configure Slack Integration Plugin

1. Open Katalon Studio, in the main menu, select **Project > Settings > Plugin > Slack**. Check the **Using Slack** checkbox and input the required information. Click the **Test Connection** button to ensure Katalon Studio is integrated with the Slack API app. Click **Apply** when done.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/slack-plugin-integration/KS-Plugin-Slack.png" width=70% alt="Configure Slack plugin">

2. After the configuration, run your tests and verify the Summary execution results on the Slack channel.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/slack-plugin-integration/Slack-Test-result-summary.png" width=70% alt="Configure Slack plugin">
