---
title: "Passing feature file and scenario tags at runtime when building with Jenkins"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/how-to-guides/jenkins-tags-runtime.html
description:
---
When running automated tests, you might want to classify different features and scenarios into different tags for better management.

This tutorial will guide you through how to set your scenario tags to be executed at runtime when Jenkins Build triggers your tests.

> Requirement:
>
> * Jenkins is already installed. See Jenkins documentation on [Installing Jenkins](https://www.jenkins.io/doc/book/installing/).
> * Katalon TestOps plugin is already installed on Jenkins. See [How to use Katalon TestOps plugin for Jenkins on Windows](https://docs.katalon.com/katalon-studio/docs/jenkins-plugin-windows.html#run-a-freestyle-jenkins-project).
> * An active Katalon Runtime Engine license.

### Create Global Variables

You can change Global Variable values in a Test Suite during runtime without affecting other Test Suites. Therefore, using a Global Variable as a parameter in the keyword `runFeatureFolderWithTags` can save your time when you have many tags to manage.

1. In the **Tests Explorer**, go to **Profiles** to open your desired Profiles. Click **Add** to create a Global Variable which values are tags. See [Global Variables](https://docs.katalon.com/katalon-studio/docs/execution-profile-v54.html#global-variables).

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-tag-runtime/globalvariable-tags.png" alt="add global variable" width=70%>

2. Write a test case with the following keyword: `runFeatureFolderWithTags(folderRelativePath, tags)`.

    * folderRelativePath: the folder relative path that starts from the current project location.
    * tags: the Global Variable defined in step 1.

    **Example**:
    
    ```groovy
    CucumberKW.runFeatureFolderWithTags('Include/features/BDD Cucumber Tests', GlobalVariable.username)
    ```

    > Notes:
    >
    > To learn more about this keyword, see [[Cucumber] Run Feature Folder with Tags](https://docs.katalon.com/katalon-studio/docs/cucumber-kw-run-feature-folder-tag.html).

3. Add this test case to a test suite and execute it from Jenkins. With the Global Variable created, you can choose which feature files folder to run with your desired tags values.

### Update Global Variables during runtime

To change the Global Variable by your desired scenario tags during runtime, use the following command syntax `-g_XXX`, for example, `-g_userName="admin"`.

Read more about running Cucumber feature files at [BDD Testing Framework (Cucumber integration)](https://docs.katalon.com/katalon-studio/docs/cucumber-features-file.html).