---
title: "[Cucumber] Run Feature File"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/cucumber-kw-run-feature-file.html
---
* **Description**: Execute a single Feature File.
* **Keyword name**: runFeatureFile
* **Keyword syntax**: runFeatureFile(relativeFilePath, flowControl)
* **Parameters**:
  * Name: relativeFilePath
    * Description: a relative file path of the feature file
    * Parameter Type: String
    * Mandatory: Required
  * Name: flowControl
    * Description: an instance com.kms.katalon.core.model.FailureHandling that controls the running flow
    * Parameter Type: FailureHandling
    * Mandatory: Optional
* **Returns**: an instance of CucumberRunnerResult that includes the status of keyword and report folder location.
* **Example**:

```groovy
CucumberKW.runFeatureFile('Include/features/New Feature File.feature')
```
