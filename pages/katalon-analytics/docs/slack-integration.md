---
title: "How to configure Slack integration with Katalon TestOps"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/slack-integration.html
---
Katalon TestOps allows you to integrate with Slack to receive notification messages of your test execution results.

## Prerequisites

This feature is only accessible to the Owner of the Organization. We can learn how to create an Incoming Webhook [here](https://api.slack.com/messaging/webhooks).

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/slack-integration/kt_message_webhook.png)

In the left sidebar of the page [Sending messages using Incoming Webhooks](https://api.slack.com/messaging/webhooks), choose **Using Webhooks**, and click the button **Create your Slack app**.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/slack-integration/kt_create_slack_app.png)

The table **Create a Slack App** displays, type the **App Name**, choose a **Development Slack Workspace** from the list, click **Create App**.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/slack-integration/kt_table_create_slack_app.png)

The table **Basic Information** displays, click button **Incoming Webhooks**.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/slack-integration/kt_click_incoming_webhooks.png)

The table **Incoming Webhooks** displays, at the item **Active Incoming Webhooks**, click button **On**.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/slack-integration/kt_incom_webhook_on.png)

Click button **Add New Webhook to Workspace**.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/slack-integration/kt_add_new_webhook.png)

Choose a channel to post to an app and click the button **Allow**.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/slack-integration/kt_slack_channel_post.png)

The board **Incoming Webhooks** display, click the button **Copy** below for coping URL.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/slack-integration/kt_copy_webhook_url.png)

## Configure in TestOps 

Navigate to **Slack Settings** under **Configurations**.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/slack-integration/kt_slack_integration.png)

Enter an **Incoming Webhook URL** by pasting the URL which we have just copied. Click the button **Save** for saving the URL and click the button **Test Connection** for connecting to Slack.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/slack-integration/kt_save_test_connect.png)

You will receive notification messages in Slack once you have configured the integration.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/slack-integration/kt_slack_message.png)