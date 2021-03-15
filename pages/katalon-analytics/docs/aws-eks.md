---
title: "Create a Kubernetes Test Environment" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/aws-eks.html 
description: 
---

Create a **Kubernetes Test Environment** to execute or schedule Test Runs with **Katalon TestOps**.

In your project, go to *Configurations* and select *Test Environments*.

Click on *"Create Kubernetes Test Environment"* and fill in the required fields to connect to **Kubernetes**.

- **Agent Name**: Enter a name for your agent.
- **Endpoint, Certificate Authority, Namespace**: This information can be found in **Kubernetes**.
- **API Key**: your API Key in [Katalon TestOps](https://analytics.katalon.com/user/apikey).
- **Authentication Type**: please choose one of the below options which you have configured in EKS:
  - Username/Password
  - Token
  - EKS

Click **Create** to after finishing these above steps.

After creating the environment, you now have the Kubernetes Test Environment ready to schedule a Test Run.

> View a list of Test Environment that you have created in *Test Environments* page.
>
><img src="https://github.com/katalon-studio/docs-images/blob/master/katalon-analytics/docs/aws-eks/Kubernetes-test-environment.png" width="" height="">

## Next steps

- [Create a Script Repository](/katalon-analytics/docs/code-repo)
- [Schedule a Test Run](/katalon-analytics/docs/kt-scheduler)


## Related topics

- [Create a Local Test Environment](https://docs.katalon.com/katalon-analytics/docs/agents.html)
- [Create a Docker environment](https://docs.katalon.com/katalon-analytics/docs/docker.html)
- [Create a CircleCI Environment](https://docs.katalon.com/katalon-analytics/docs/circleci.html)
