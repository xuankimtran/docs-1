---
title: "API Keys"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/ka-api-key.html
description: Instructions of how to generate and use API Key in KA
---

## Katalon API key's usage

API keys generated in Katalon TestOps are required in the following circumstances:

* Integrating Katalon Studio with Katalon TestOps in console mode. [Learn more](https://docs.katalon.com/katalon-analytics/docs/integration-with-katalon-studio.html#enable-integration).
  
  > Note: In the command-line generator in Katalon Studio, the command-line options of API Key, including `-apiKey=<Your_API_Key>` and `-apikey=<Your_API_Key>` are both accepted.

* API Keys can be used for representing a user's credentials to integrate Katalon TestOps with other platforms like [Jira](https://docs.katalon.com/katalon-analytics/docs/kt-jira-config.html) and [Jenkins](https://docs.katalon.com/katalon-analytics/docs/ka-integration-jenkins.html), or to create a test environment with [CircleCI](https://docs.katalon.com/katalon-analytics/docs/circleci.html), [AWS EKS](https://docs.katalon.com/katalon-analytics/docs/aws-eks.html), or [local Agent](https://docs.katalon.com/katalon-analytics/docs/agents.html).

## How to create a new API Key

Create an API key from your **Katalon TestOps** account:

1. Log into [Katalon TestOps](https://analytics.katalon.com/)
2. Click on your profile icon
3. On the menu tab, select **API Key**
4. In the **API Key** view, click on the **Create API Key** button
5. In the pop-up, enter a key name and click **Create**. You have just added a new API key successfully.
6. To copy your API key, click on the icon of **Copy to clipboard**, then paste it in required places.

## How to remove an existing API Key

1. From the **API Key** view, click on the **Remove** button of the key you want to remove
2. Click **Delete** to confirm your removal
   > Note: This action cannot be undone. Once a key is removed, it cannot be used anymore.
