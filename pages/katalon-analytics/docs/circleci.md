---
title: "Create CircleCI Test Environment"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/circleci-agent.html 
description: 
---
TestOps CI allows you to set-up your test environment with CircleCI to schedule and execute tests remotely.

To create a new CircleCI testenvironment, in TestOps CI, go to **Test Environment** > **CircleCI**.

Fill in the required fields to connect to CircleCI.

- **Agent Name**
- **URL**: https://circleci.com
- **Token**: your API in [CircleCI](https://circleci.com/account/api)
- **API Key**: your API key in [Katalon TestOps](https://analytics.katalon.com/user/apikey)

After connecting to CircleCI, select your project and branch.

Click the **Create** button to create a new CircleCI test enviroment.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/circleci-agent/1-connect.png" width="" height="">

After you have created your Circle test environment, it appears in the list as below.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/circleci-agent/2-list.png" width="" height="">

For a samle project, please visit [here](https://github.com/katalon-studio-samples/testops-circleci-sample).