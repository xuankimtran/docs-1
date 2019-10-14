---
title: "[Cucumber] Run Feature File with Tags"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/cucumber-kw-run-feature-file-tag.html
---
* **Description**: Execute a single Feature File.
* **Keyword name**: runFeatureFileWithTags
* **Keyword syntax**: runFeatureFileWithTags(relativeFilePath, tags, flowControl)
* **Parameters**:
  * Name: relativeFilePath
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
CucumberKW.runFeatureFileWithTags('Include/features/BDD Cucumber Tests/Jira Integration/KD-31800.feature', "@BA","@regressiontest")
```
