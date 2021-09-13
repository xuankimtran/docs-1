---
title: "Passing feature file tags at runtime when building with Jenkins"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/how-to-guides/jenkins-tags-runtime.html
description:
---
When running automated tests, you might want to classify different scenarios into different tags for better management.

This tutorial will guide you through how to set your scenario tags to be executed at runtime when Jenkins Build triggers your tests.

> Requirement:
>
> * Jenkins is already installed. See Jenkins documentation on [Installing Jenkins](https://www.jenkins.io/doc/book/installing/).
> * An active Katalon Runtime Engine license.

### Create Global Variables during runtime

You can change Global Variable values during runtime without affecting other Test Suites. Therefore, using a Global Variable as a parameter in the keyword `runFeatureFolderWithTags` can save your time when you have a huge amount of tags to manage.

1. Open your desired Profiles. Click **Add** to create a Global Variable whose values are tags. See [Global Variables](https://docs.katalon.com/katalon-studio/docs/execution-profile-v54.html#global-variables).

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-tag-runtime/globalvariable-tags.png" alt="add global variable" width=70%>

2. Write a test case with the following keyword: `runFeatureFolderWithTags(folderRelativePath, tags)`.

    * folderRelativePath: the folder relative path that starts from the current project location.
    * tags: the Global Variable defined in step 1.

    **Example**:
    
    ```groovy
    CucumberKW.runFeatureFolderWithTags('Include/features/BDD Cucumber Tests',GlobalVariable.username)
    ```

    > Notes:
    >
    > To learn more about this keyword, see [[Cucumber] Run Feature Folder with Tags](https://docs.katalon.com/katalon-studio/docs/cucumber-kw-run-feature-folder-tag.html).

3. Add this test case to a test suite and execute it from Jenkins. To learn more about how to execute tests from Jenkins, see [How to use Katalon TestOps plugin for Jenkins on Windows](https://docs.katalon.com/katalon-studio/docs/jenkins-plugin-windows.html).

### Update Global Variables during runtime

To change the Global Variable by your desired scenario tags during runtime, use the following command syntax `-g_XXX`, for example, `-g_userName="admin"`.

Read more about running Cucumber feature files at [BDD Testing Framework (Cucumber integration)](https://docs.katalon.com/katalon-studio/docs/cucumber-features-file.html).