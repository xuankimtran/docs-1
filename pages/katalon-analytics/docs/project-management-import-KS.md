---
title: "Upload Test Results from Katalon Studio"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/project-management-import-KS.html
redirect_from:
    - "/display/KA/From+Katalon+Studio/"
    - "/display/KA/From%20Katalon%20Studio/"
    - "/x/wBxO/"
    - "/katalon-analytics/docs/project-management-import-KS/"
    - "/katalon-studio/tutorials/upload_test_execution_reports_katalon_analytics.html"
description:
---
> Note: Katalon Studio version 7.0 supports submitting test results with captured videos to Katalon TestOps.

## Automatically

1. In Katalon Studio, select **Project > Settings > Katalon TestOps** or click into the **TestOps** icon on the Main Toolbar to open the project setting dialogue.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/from-katalon-studio/KS-main-toolbar.png)

2. Enter your Katalon account, then click **Connect**.

3.  Enable the integration, and you will be able to select your Team and Project to upload test results.

4. Click **OK** to save the project settings.

5. Select a Test Case or Test Suite.

6. You will see a button **View Execution History** to access to TestOps directly.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/from-katalon-studio/KS-view-test-result-button.png)

7. You will see the test results are automatically uploaded into Katalon TestOps.

## Manually

Even though Katalon Studio supports to upload test results automatically when connects successfully with TestOps, but you can manually upload test results to your target team and project.

1. In Katalon Studio, you open a test suite, and navigate to the **Result** tab.

2. Select **Katalon TestOps**, and click **Upload**.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/from-katalon-studio/ks-upload-test-result.png)

2. When Katalon TestOps dialog pops up, select the team and project you want to upload, then select **Upload**.

![manually](https://user-images.githubusercontent.com/43736150/66178577-03815f00-e690-11e9-8887-0b36ec35370a.png)

Once having uploaded the test results successfully, you can double-check on Katalon TestOps.
