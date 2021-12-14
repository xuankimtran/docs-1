---
title: "Create a Kubernetes Test Environment" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/aws-eks.html 
description: 
---

In Katalon TestOps, you can create a Kubernetes (EKS) Test Environment  to execute or schedule Test Runs.

Follow these steps:

1. Sign in to [Katalon TestOps](https://testops.katalon.io/login).
2. Go to your Project > **Configurations** > **Test Environments** > **Kubernetes**.

3. Click **Create Kubernetes Test Environment** at the top right corner.

4. Fill in the required information.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-aug-aws-eks/create-kubernetes-page-2.png" width=100% alt="create kubernetes page">

* In the **Agent Name** section, enter a name for your Agent.
* In the **URL**, **Certificate Authority** and **Namespace** sections, enter your Kubernetes information.
* In the **Katalon API Key** section, enter your [API Key](https://analytics.katalon.com/user/apikey).
* In the **Authentication Type** section, choose one of the following options:
  * Username/Password
  * Token
  * AWS EKS

  > Notes:
  >
  > You have already configured Authentication Type in EKS.

5. Click **Test Connection**, then click **Create** to complete.

6. Go to **Test Environments** > **Kubernetes** to see the list of Kubernetes test environments you have created.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-aug-aws-eks/kubernetes-test-environment-page-list-2.png" width="" height="" alt text=" kubernetes environment list">

Next steps:

1. [Upload Test Scripts from a Git Repository](https://docs.katalon.com/katalon-analytics/docs/git-test-project.html).
2. [Schedule Test Runs](https://docs.katalon.com/katalon-analytics/docs/create-plan.html).

See also:

* [Create a Local Test Environment with an Agent](https://docs.katalon.com/katalon-analytics/docs/agents.html).
* [Set up an Agent to execute tests on Docker environment](https://docs.katalon.com/katalon-analytics/docs/docker.html).
