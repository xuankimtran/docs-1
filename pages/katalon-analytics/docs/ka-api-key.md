---
title: "API Keys"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/ka-api-key.html
description: Instructions on how to generate and use a Katalon API Key
---

## Generate a Katalon API Key

You need to generate API Keys in Katalon TestOps in the following circumstances:

* When you want to integrate Katalon Studio with Katalon TestOps in console mode. See [Katalon Studio Integration](https://docs.katalon.com/katalon-analytics/docs/integration-with-katalon-studio.html#enable-integration).
  
  > Notes:
  >
  > In the command-line generator in Katalon Studio, the command-line options for API Keys, including `-apiKey=<Your_API_Key>` and `-apikey=<Your_API_Key>` are both accepted.

* When you want to integrate Katalon TestOps with other platforms such as [Jira](https://docs.katalon.com/katalon-analytics/docs/kt-jira-config.html) and [Jenkins](https://docs.katalon.com/katalon-analytics/docs/ka-integration-jenkins.html), 

* When you want to create a test environment such as [CircleCI](https://docs.katalon.com/katalon-analytics/docs/circleci.html), [AWS EKS](https://docs.katalon.com/katalon-analytics/docs/aws-eks.html), or [create a local test environment with an agent](https://docs.katalon.com/katalon-analytics/docs/agents.html).

To create a new API Key, follow these steps:

1. Sign in to [Katalon TestOps](https://testops.katalon.io/login).

2. Click on the *Avatar* icon at the top right corner.

3. Go to **Notification Settings** > **Katalon API Key**.

    The **Katalon API Key** page appears.

    > Notes:
    >
    > You can also click on [this link](https://testops.katalon.io/user/apikey), then sign in to have access to the **Katalon API Key** page directly.

4. Click **Create API Key** in the top right corner.
  
    The **Create API Key** box pops up.

5. Enter a name for your key, then click **Create**.

You have successfully added a new API key.

### Use a Katalon API Key

1. Go to your **Katalon API Key** page.

    You can see a list of all API Keys here.

2. Click on the *Copy* icon of the API Key you want to use.

    You have copied your API Key.
  
3. Paste the copied API Key to the required platform.

You can now use your API Key.

### Remove a Katalon API Key

1. Go to your **Katalon API Key** page.

    You can see a list of all API Keys here.

2. Click on the *Trash bin* icon of the API Key you want to remove.

3. Click **Delete** to confirm your action.

   > Notice:
   >
   > This action cannot be undone. You cannot use the API Key once it is deleted.
