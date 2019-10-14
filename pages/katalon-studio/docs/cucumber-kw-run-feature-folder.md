---
title: "[Cucumber] Run Feature Foler"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/cucumber-kw-run-feature-folder.html
---

* **Description**: Execute multiple feature files stored in the same features folder.
* **Keyword name**: runFeatureFolder
* **Keyword syntax**: runFeatureFolder(folderRelativePath, flowControl)
* **Parameters**:
  * Name: folderRelativePath
    * Description: the folder relative path that starts from the current project location.
    * Parameter Type: String
    * Mandatory: Required
  * Name: flowControl
    * Description: an instance com.kms.katalon.core.model.FailureHandling that controls the running flow.
    * Parameter Type: FailureHandling
    * Mandatory: Required
* **Returns**: an instance of CucumberRunnerResult that includes the status of keyword and report folder location.
* **Example**:

```groovy
CucumberKW.runFeatureFile('Include/features/New Feature File.feature')
```
