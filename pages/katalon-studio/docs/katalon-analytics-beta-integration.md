---
title: "Integrate Katalon Studio with Katalon TestOps" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/integration-with-katalon-studio.html
redirect_from:
    - "/display/KD/Katalon+Analytics+%28Beta%29+Integration/"
    - "/display/KD/Katalon%20Analytics%20%28Beta%29%20Integration/"
    - "/x/KRhO/"
    - "/display/KA/Integration+with+Katalon+Studio/"
    - "/display/KA/Integration%20with%20Katalon%20Studio/"
    - "/katalon-analytics/docs/integration-with-katalon-studio/"
    - "/katalon-analytics/docs/ka-integration-katalon-studio/"
    - "/katalon-analytics/docs/ka-integration-katalon-studio.html"
    - "/x/mw3R/"
    - "/katalon-studio/docs/katalon-analytics-beta-integration.html"
---

To configure the Katalon TestOps Integration, right after activating:

* Select a team in the configured organization that you have permission to access.

* Select a project under that team you’d like to work on or create your own one if you have permission.

## Settings

In Katalon Studio, go to **Project > Settings > Katalon TestOps**.

You must enable **Katalon TestOps Integration** to submit test execution reports to Katalon TestOps. Follow the below steps to set up the integration properly:

1. Check the **Enable Katalon TestOps Integration** checkbox to retrieve all teams and projects that you have permission to access in the organization you're working on.

   > In case you want to switch to another organization, on the top right corner of the app, select you account > select **Deactivate** > activate again.

   Once Katalon Studio is **successfully connected** to Katalon TestOps, all relevant Katalon TestOps the **Teams** and **Projects** will be retrieved and displayed in the Teams and Projects drop-down menu. You can also **create a  new project** in Katalon TestOps if you're a team owner or admin, simply click the **New Project** button and enter a name for it.

2. Select a team and project to which you will upload your test results. Here you can reload this part by clicking **Fetch Projects**.

3. Click **Apply** and then **OK** to finish your configurations.

To verify if you have overridden the authentication successfully, on the top right corner, select your account > **View Dashboard**. You should be navigated to the project having been configured above.

## Access Katalon TestOps

### View Reports

In the **Result** Tab of a Test Suite, click the **Katalon TestOps** button, then select **Access TestOps** to access the **Execution** tab. You can also view more reports in the **Reports** tab in Katalon TestOps.

### View Execution History of a specific Test Case or Test Suite

You can also view a specific Test Case or Test Suite entire execution history in Katalon TestOps by clicking the **View Execution History** button on the Test Case or Test Suite Views.  

### Store Katalon Studio's project code in Katalon TestOps

Starting in **version 7.0**, to store your Katalon Studio's Project Code in Katalon TestOps, from any screens of your project in Katalon Studio, click <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/katalon-analytics-beta-integration/upload-project-code.png" width="28" height="20.6"> icon, select the preferred Katalon TestOps team and project to store the Katalon Studio project code, then enter a Test Projects name and click **Upload**.

### Create Test Plan in Katalon TestOps right from Katalon Studio

Starting in **version 7.0**, on the test suite collection view, click the **Create Test Plan** button to:

* Zip and upload the current Project code.
* Create a corresponding Test Plan on Katalon TestOps with the above Test Project.
