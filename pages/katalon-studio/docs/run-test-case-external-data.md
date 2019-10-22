---
title: "Run Test Case with an external data source"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/run-test-case-external-data.html
description: Guidelines about how to run test case with an external data in Katalon Studio
---
Katalon Studio provides the ability to execute automation test with external data sources.

## Import an Excel file to Test Data

Refer to [this article](https://docs.katalon.com/katalon-studio/docs/manage-test-data.html#create-an-excel-test-data) to learn how to create a new Excel Test Data in Katalon Studio. Data from the selected Excel file will be populated into the preview section like the below example.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/run-test-case-external-data/1-new-excel-test-data.png)

## Create a new Test Suite with Test Case Variables

Open a Test Suite, select **Add** from the command toolbar. All test cases in Katalon Studio will be displayed in the **Test Case Browser** dialog. The selected test case will be added to the test case list like the following example.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/run-test-case-external-data/2-new-test-suite.png)

## Manage Data Binding

1. In the test suite editor, click **Show Data Binding** to expand the **Data Binding** section with the **Test Data** and **Variable Binding** tables.

    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/run-test-case-external-data/3-show-data-binding.png)

2. In the **Test Data** table, select **Add** > select the data to be used for execution > the selected test data are added to the list accordingly.

    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/run-test-case-external-data/4-display-data-binding.png)

3. In the **Data Binding** table which displays all variables of the selected test case, select all rows > choose **Set Type** > select **Data Column** as their types.

    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/run-test-case-external-data/5-set-type.png)

4. Click **Set Test Data** to decide which test data from the list to be used for execution.

    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/run-test-case-external-data/6-set-test-data.png)

5. Click each cell in the **Value** column to specify the data field in the selected data file. For example:

    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/run-test-case-external-data/7-after-setting.png)

6. After finishing all the steps above, save and run your test suite to see the following result:

    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/run-test-case-external-data/8-result.png)

> **Quick tip:**
>
> With the **Map All** button, you can quickly map the public variables of the selected test case with respective columns in the test data. To automatically bind the variable to the data, the variables and the respective columns in Test Data should share **the same name**.\
>
> For example, the 'Username' and 'Password' variables of the selected test case can be mapped automatically with the 'Username' and 'Password' columns of the test data accordingly when you click **Map All**.
>
>![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/design-a-test-suite/image2017-8-31-143A333A23.png)
