---
title: "[Cucumber] Run Feature Foler with Tags"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/cucumber-kw-run-feature-folder-tag.html
---

* **Description**: Execute multiple feature files stored in the same features folder.
* **Keyword name**: runFeatureFolder
* **Keyword syntax**: runFeatureFolderWithTags(folderRelativePath, tags, flowControl)
* **Parameters**:
  * Name: folderRelativePath
    * Description: the folder relative path that starts from the current project location.
    * Parameter Type: String
    * Mandatory: Required
  * Name: tags
    * Description: which tags in the feature files should be executed.
    * Parameter Type: String[]
    * Mandatory: Required
  * Name: flowControl
    * Description: an instance com.kms.katalon.core.model.FailureHandling that controls the running flow
    * Parameter Type: FailureHandling
    * Mandatory: Required  
* **Returns**: an instance of CucumberRunnerResult that includes the status of keyword and report folder location.
* **Example**:

```groovy
CucumberKW.runFeatureFolderWithTags('Include/features/BDD Cucumber Tests',"@BA")
```
