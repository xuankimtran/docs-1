---
title: "Create an AWS EKS Test Environment" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/aws-eks.html 
description: 
---
TestOps CI allows you to set up your test environment with EKS to schedule and execute tests remotely.

To create a new EKS test environment, in TestOps CI, go to **Test Environment** > **AWS EKS**.

Fill in the required fields to connect to EKS.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/aws-eks/1-config-eks.png" width="" height="">

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/aws-eks/2-config-eks.png" width="" height="">

- **Agent Name**
- **Endpoint, Certificate Authority, Namespace**: This information can be found in EKS.
- **API Key**: your API Key in [Katalon TestOps](https://analytics.katalon.com/user/apikey).
- **Authentication Type**: please choose one of the below options which you have configured in EKS:
  - Username/Password
  - Token
  - EKS


Click **Create** to after finishing these above steps.

Now your AWS EKS test environment has been created.

You can view a list of your EKS test environments here.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/aws-eks/3-list.png" width="" height="">