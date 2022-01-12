---
title: "[Cucumber] Run Feature File with Tags"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/cucumber-kw-run-feature-file-tag.html
---

Katalon Studio supports executing a single feature file with the `runFeatureFileWithTags` function, using the following tag expressions:

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

* **Description**: execute the scenarios associated with all the input tags.
* **Keyword name**: runFeatureFileWithTags.
* **Keyword syntax**: runFeatureFileWithTags(relativeFilePath, tags, flowControl).
* **Parameters**:
  * Name: relativeFilePath
    * Description: the relative path to the feature file that starts from the current project location.
    * Parameter Type: `String`.
    * Mandatory: required.
  * Name: tags
    * Description: the tags of the scenarios that you want to execute.
    * Parameter Type: `String`, `String[]`, or `String...` (Varargs).
    * Mandatory: required.
  * Name: flowControl (only valid when tags are of `String[]` type)
    * Description: an `instance com.kms.katalon.core.model.FailureHandling` that controls the running flow.
    * Parameter Type: `FailureHandling`.
    * Mandatory: optional.
* **Returns**: an instance of `CucumberRunnerResult` that includes the status of keyword and report folder location.
* **Example**:

  **Example #1**: tags of `String` type
  ```groovy
  CucumberKW.runFeatureFileWithTags("Include/features/New Feature File.feature", "@tag1 and @tag2")
  ```

  **Example #2**: tags of `String[]` type
  ```groovy
  String[] logTags = ["@tag1", "@tag2"] as String[]
  CucumberKW.runFeatureFileWithTags("Include/features/New Feature File.feature", logTags, FailureHandling.STOP_ON_FAILURE)
  ```

  **Example #3**: tags of `String...` type (Varargs)
  ```groovy
  CucumberKW.runFeatureFileWithTags("Include/features/New Feature File.feature", "@tag1", "@tag2")
  ```
## Using the OR tag expression

* **Description**: execute the scenarios associated with one of the input tags.
* **Keyword name**: runFeatureFileWithTags
* **Keyword syntax**: runFeatureFileWithTags(relativeFilePath, tags, flowControl).
* **Parameters**:
  * Name: relativeFilePath
    * Description: the relative path to the feature file that starts from the current project location.
    * Parameter Type: `String`
    * Mandatory: required
  * Name: tags
    * Description: the tags of the scenarios that you want to execute.
    * Parameter Type: `String` or `String[]`.
    * Mandatory: required
  * Name: flowControl (only valid when tags are of `String[]` type)
    * Description: an instance `com.kms.katalon.core.model.FailureHandling` that controls the running flow.
    * Parameter Type: `FailureHandling`.
    * Mandatory: optional.
* **Returns**: an instance of `CucumberRunnerResult` that includes the status of keyword and report folder location.
* **Example**:

  **Example #1**: tags of `String` type
  ```groovy
  CucumberKW.runFeatureFileWithTags("Include/features/New Feature File.feature", "@tag1 or @tag2")
  ```

  **Example #2**: tags of `String[]` type
  ```groovy
  String[] logTags1 = ["@tag1, @tag2"] as String[]
  CucumberKW.runFeatureFileWithTags("Include/features/New Feature File.feature", logTags1, FailureHandling.STOP_ON_FAILURE)
  // Or 
  String[] logTags2 = ["@tag1 or @tag2"] as String[]
  CucumberKW.runFeatureFileWithTags("Include/features/New Feature File.feature", logTags2, FailureHandling.STOP_ON_FAILURE)
  ```