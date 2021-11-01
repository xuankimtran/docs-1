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

Slack Integration with Katalon Studio allows you to send test execution reports using a Slack API app.

This guide shows you how to integrate a Slack API app with Katalon Studio.

> **Prerequisites**
>
> * An active Katalon Studio Enterprise license.
> * The **Slack Integration** plugin for Katalon Studio installed. You can install the plugin here: [Slack Integration](https://store.katalon.com/product/4/Slack-Integration).

## Create a Slack API app for integration

1. To create a Slack API app, navigate to the [Slack API app](https://api.slack.com/apps) site and create a new app from scratch.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/slack-plugin-integration/Slack-create-app-from-scratch.png" width=70% alt="Create an app from scratch">

2. Next, you need to configure the app. Navigate to the **OAuth & Permissions** section, scroll down to the **Scopes** pane and add some **Bot Token Scopes**.

    We need to grant the app these scopes: `app_mentions:read`, `calls:write`, `chat:write`, and `chat:write.customize`.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/slack-plugin-integration/Slack-add-scope.png" width=70% alt="Add scopes">

    > To learn more about Slack permission scopes, refer to this guide on the Slack documentation site: [Slack Permission Scopes](https://api.slack.com/scopes).

3. To install the app, scroll up to the **OAuth Tokens for Your Workspace** pane and click on the **Install to Workspace** button. 

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/slack-plugin-integration/Slack-app-api-install-app.png" width=70% alt="Install to Workspace button">

4. After the installation, a **Bot User OAuth Token** is displayed. Click on the **Copy** button to copy the token to your clipboard.

    Katalon Studio requires this token to integrate with a Slack API app.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/slack-plugin-integration/Slack-bot-OAuth-token.png" width=70% alt="Copy the OAuth token">

5. Select a channel in your Slack workspace. In the message field, type in "`/invite`" and select **Add apps to this channel**. Enter your app's name.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/slack-plugin-integration/Slack-add-app-to-channel.png" width=70% alt="Add apps to this channel">

## Configure Slack plugin

1. Open Katalon Studio, in the main menu, select **Project > Settings > Plugin > Slack**. Check the **Using Slack** checkbox and input the required information. Click the **Test Connection** button to ensure Katalon Studio is integrated with the Slack API app. Click **Apply** when done.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/slack-plugin-integration/KS-Plugin-Slack.png" width=70% alt="Configure Slack plugin">

2. After the configuration, run your tests and verify the test report messages on the Slack channel.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/slack-plugin-integration/Slack-Test-result-summary.png" width=70% alt="Configure Slack plugin">
