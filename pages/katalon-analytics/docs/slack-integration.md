---
title: "How to configure Slack integration with Katalon TestOps"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/slack-integration.html
---
Katalon TestOps allows you to integrate with Slack to receive notifications of your test results on Slack.

> Requirements:
>
> * You must be the Owner of an Organization and a Team. See: [Roles and Permissions](https://docs.katalon.com/katalon-analytics/docs/testops-roles-privileges.html).
> * You must be the Admin of a Slack workspace.

## Create an Incoming Webhook on Slack

1. Go to [Slack API](https://api.slack.com/messaging/webhooks) > **Using Webhooks**. 

2. Click on the green **Create your Slack app** button.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-oct-slack-integration/slack-step1-create-apps.png" width=100% alt="slack api create app">

    The **Create an app** box appears.

3. Select your preferred configuration, then name your app and choose your workspace.

4. Click **Create App**.

    You will be automatically navigated to the **Basic Information** page.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-oct-slack-integration/slack-step4-basic-info.png" width=100% alt="slack api basic info page">

5. Click on the **Incoming Webhooks** box.  

    The **Incoming Webhooks** page appears.

6. Switch the toggle **On** to activate Incoming Webhooks.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-oct-slack-integration/slack-step5-activate-incoming-webhook.png" width=100% alt="slack api incoming webhook page">

7. Click **Add New Webhook to Workspace**.

    A new window appears as below. 

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-oct-slack-integration/slack-step5-allow-webhook-on-slack.png" width=100% alt="add webhook to workspace">

8. Select a channel to receive Slack notifications, click **Allow**.

    You will be automatically navigated back to the **Incoming Webhooks** page.
    
9. Scroll down to the **Webhook URL** section.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-oct-slack-integration/slack-step6-add-webhook.png" width=100% alt="webhook url">

    You can see that your channel has been added (e.g., **#qa-demo**).

10. Click **Copy** to copy the Webhook URL.

You use this URL for Slack integration on Katalon TestOps.

## Integrate Slack with Katalon TestOps

1. Sign in to [Katalon TestOps](https://testops.katalon.io/login) and go to your Project.

2. Go to **Configurations** > **Integrations**.

3. Select **Slack** from the dropdown list.

4. Paste the URL you have copied earlier in the **Incoming Webhook URL** section, then click **Test Connection**.

    If the connection is successful, you will receive a message on Slack.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-oct-slack-integration/slack-step9-receive-slack-noti.png" width=100% alt="slack notification of successful integration">
    
5. Click **Save**.

You have enabled Slack integration on Katalon TestOps.

Now every time you run a test on Katalon TestOps, you and your members will receive a Slack message on the Test Run and its results.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/slack-integration/kt_slack_test_run.png" width=100% alt="slack message on test run">
