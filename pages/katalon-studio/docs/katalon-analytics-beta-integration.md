---
title: "Upload Test Results to Katalon TestOps automatically from Katalon Studio" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/katalon-analytics-beta-integration.html
redirect_from:
    - "/display/KD/Katalon+Analytics+%28Beta%29+Integration/"
    - "/display/KD/Katalon%20Analytics%20%28Beta%29%20Integration/"
    - "/x/KRhO/"
    - "/display/KA/Integration+with+Katalon+Studio/"
    - "/display/KA/Integration%20with%20Katalon%20Studio/"
    - "/katalon-analytics/docs/ka-integration-katalon-studio/"
    - "/katalon-analytics/docs/ka-integration-katalon-studio.html"
    - "/katalon-analytics/docs/view-reports/"
    - "/x/mw3R/"
    - "/katalon-analytics/docs/integration-with-katalon-studio.html"
    - "/katalon-analytics/docs/upload-reports-overview.html"
---

To configure the Katalon TestOps Integration, right after activating:

* Select a team in the configured organization that you have permission to access.

* Select a project under that team you’d like to work on or create your own one if you have permission.

## Settings

In Katalon Studio, go to **Project > Settings > Katalon TestOps**.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/integration-ks/config-integration.png)

You must enable **Katalon TestOps Integration** to submit test execution reports to Katalon TestOps. Follow the below steps to set up the integration properly:

1. Check the **Enable Katalon TestOps Integration** checkbox to retrieve all teams and projects that you have permission to access in the organization you're working on.

   > In case you want to switch to another organization, on the top right corner of the app, select you account > select **Deactivate** > activate again.

   Once Katalon Studio is **successfully connected** to Katalon TestOps, all relevant Katalon TestOps the **Teams** and **Projects** will be retrieved and displayed in the Teams and Projects drop-down menu. You can also **create a  new project** in Katalon TestOps if you're a team owner or admin, simply click the **New Project** button and enter a name for it.

2. Select a team and project to which you will upload your test results. Here you can reload this part by clicking **Fetch Projects**.

3. Click **Apply** and then **OK** to finish your configurations.

To verify if you have overridden the authentication successfully, on the top right corner, select your account > **View Dashboard**. You should be navigated to the project having been configured above.

## Automatically upload test results

After configuring TestOps settings in Katalon Studio, starting running a test suite.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/integration-ks/run-test-ks.png)

Your test results will be automatically uploaded to TestOps Center.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/integration-ks/upload-to.png)
