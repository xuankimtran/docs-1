---
title: "[Cucumber] Run Feature Folder with Tags"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/cucumber-kw-run-feature-folder-tag.html
---

Katalon Studio supports executing feature files in a folder with the `runFeatureFolderWithTags` function, using the following tag expressions:

<table>
  <thead>
    <tr>
      <th><b>Expression</b></th>
      <th><b>Description</b></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <code>@tag1 and @tag2</code>
      </td>
      <td>Scenarios tagged with both <code>@tag1</code> and <code>@tag2</code>.</td>
    </tr>
    <tr>
      <td>
        <code>@tag1 or @tag2</code>
      </td>
      <td>Scenarios tagged with either <code>@tag1</code> or <code>@tag2</code>.</td>
    </tr>
  </tbody>
</table>

> To learn more about tag expressions, refer to this Cucumber document: [Cucumber tag expression](https://cucumber.io/docs/cucumber/api/#tag-expressions).

## Using the AND tag expression

* **Description**: query the feature files in the specified folder, and execute the scenarios associated with all the input tags.
* **Keyword name**: runFeatureFolderWithTags.
* **Keyword syntax**: runFeatureFolderWithTags(folderRelativePath, tags, flowControl).
* **Parameters**:
  * Name: folderRelativePath
    * Description: the folder relative path that starts from the current project location.
    * Parameter Type: `String`.
    * Mandatory: required.
  * Name: tags
    * Description: the tags of the scenarios that you want to execute.
    * Parameter Type: `String`, `String[]`, or `String...` (Varargs).
    * Mandatory: required.
  * Name: flowControl (only valid when tags are of `String[]` type)
    * Description: a `com.kms.katalon.core.model.FailureHandling` instance that controls the running flow.
    * Parameter Type: `FailureHandling`.
    * Mandatory: optional.
* **Returns**: an instance of `CucumberRunnerResult` that includes the status of keyword and report folder location.
* **Example**:

  **Example #1**: tags of `String` type
  ```groovy
  CucumberKW.runFeatureFileWithTags("Include/features/BDD Cucumber Tests/", "@tag1 and @tag2")
  ```

  **Example #2**: tags of `String[]` type
  ```groovy
  String[] logTags = ["@tag1", "@tag2"] as String[]
  CucumberKW.runFeatureFileWithTags("Include/features/BDD Cucumber Tests/", logTags, FailureHandling.STOP_ON_FAILURE)
  ```

  **Example #3**: tags of `String...` type (Varargs)
  ```groovy
  CucumberKW.runFeatureFolderWithTags("Include/features/BDD Cucumber Tests/", "@tag1", "@tag2")
  ```

## Using the OR tag expression

* **Description**: query the feature files in the specified folder, and execute the scenarios associated with one of the input tags.
* **Keyword name**: runFeatureFolderWithTags.
* **Keyword syntax**: runFeatureFolderWithTags(folderRelativePath, tags, flowControl).
* **Parameters**:
  * Name: folderRelativePath
    * Description: the folder relative path that starts from the current project location.
    * Parameter Type: `String`.
    * Mandatory: required.
  * Name: tags
    * Description: the tags of the scenarios that you want to execute.
    * Parameter Type: `String` or `String[]`.
    * Mandatory: required.
  * Name: flowControl (only valid when tags are of `String[]` type)
    * Description: a `com.kms.katalon.core.model.FailureHandling` instance that controls the running flow.
    * Parameter Type: `FailureHandling`.
    * Mandatory: optional.
* **Returns**: an instance of `CucumberRunnerResult` that includes the status of keyword and report folder location.
* **Example**:

  **Example #1**: tags of `String` type
  ```groovy
  CucumberKW.runFeatureFolderWithTags("Include/features/BDD Cucumber Tests/", "@tag1 or @tag2")
  ```

  **Example #2**: tags of `String[]` type
  ```groovy
  String[] logTags1 = ["@tag1, @tag2"] as String[]
  CucumberKW.runFeatureFolderWithTags("Include/features/BDD Cucumber Tests/", logTags1, FailureHandling.STOP_ON_FAILURE)
  // Or 
  String[] logTags2 = ["@tag1 or @tag2"] as String[]
  CucumberKW.runFeatureFolderWithTags("Include/features/BDD Cucumber Tests/", logTags2, FailureHandling.STOP_ON_FAILURE)
  ```