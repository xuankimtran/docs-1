---
title: "Create a CircleCI Test Environment"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/circleci.html 
description: 
---
In Katalon TestOps, you can set up a CircleCI Test Environment to schedule and execute tests remotely.

> Requirements:
>
> * You have created a CircleCI account with a Github account.
> * You have forked your Project to your Repository associated with your GitHub account. You can also fork this sample project, [TestOps CircleCI sample](https://github.com/katalon-studio-samples/testops-circleci-sample) for testing.
> * You have followed your Project in CircleCI.

## Configure a CircleCI Test Environment

Follow these steps:

1. Sign in to [Katalon TestOps](https://testops.katalon.io/login) and go to your Project.
2. Go to **Configurations** > **Test Environments** > **CircleCI**.
3. Click **Create CircleCI Test Environment**.
4. Fill in the required information to connect to CircleCI.
    * **Agent Name**: enter your Agent.
    * **URL**: auto-filled (https://circleci.com).
    * **Personal API Token**: enter your [CircleCI's API](https://circleci.com/account/api).
    * **Katalon API Key**: enter your [Katalon API key](https://analytics.katalon.com/user/apikey).

5. Click **Connect**.

    The **Followed Project** and **Branch** sections appear after you have connected to CircleCI successfully.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/circleci-agent/create-circleci-page.png" width="" height="" alt="create circle ci page">

    > Notes:
    >
    > The Project you have followed in CircleCI and its Branch would automatically appear here.

6. Click **Create**.

You have successfully created a CircleCI Test Environment. 

Go to **Configurations** > **Test Environments** > **CircleCI** to see the list of CircleCI Test Environments.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/circleci-agent/circleci-agent.png" width="" height="" alt="circleci list">
