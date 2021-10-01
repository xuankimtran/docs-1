---
title: "How to configure Kobiton integration with Katalon TestOps"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/kt_kobiton_integration.html
---

You can enable Kobiton integration in Katalon TestOps to enhance your real-device testing experiences.

> Requirements:
>
> You have already registered a [Kobiton](https://kobiton.com/) account.

## Integrate Kobiton with Katalon TestOps

Follow these steps:

1. Sign in to [Katalon TestOps](https://testops.katalon.io/login) and go to your Project.
2. Go to **Configurations** > **Integrations**.

    The **Integrations** page appears as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-schedule-test-runs/schedule-test-run-button.png" width=100% alt="kobiton highlight dropdown">

3. Select **Kobiton** in the dropdown list.

4. Fill in the required information.

    * **Kobiton Device URL**: enter your Kobiton Device URL.
    * **Username**: enter your Kobiton username.
    * **Kobiton's API Key**: enter your Kobiton's API key.  

5. Click **Test Connection**, then click **Save**.

You have enabled Kobiton integration. Now you can run tests with a Kobiton device in Katalon TestOps.

## Run tests with a Kobiton device

> Requirements:
>
> You have created a Script Repository for Kobiton's tests on Katalon TestOps. See: [Upload Test Scripts to a Script Repository](https://docs.katalon.com/katalon-analytics/docs/code-repo.html).

After creating a Script Repository, you can schedule test runs with a Kobiton device by configuring the advanced settings in the **Schedule Test Runs** dialog. See: [Schedule Test Runs](https://docs.katalon.com/katalon-analytics/docs/create-plan.html#advanced-settings).

You can also execute test runs manually. See: [Execute Test Runs manually](https://docs.katalon.com/katalon-analytics/docs/kt-scheduler.html).
