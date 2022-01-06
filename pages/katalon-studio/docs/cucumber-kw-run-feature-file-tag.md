---
title: "[Cucumber] Run Feature File with Tags"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/cucumber-kw-run-feature-file-tag.html
---

Katalon Studio supports executing a single Feature file with the `runFeatureFileWithTags` function, using the following tag expressions:

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
      <td>Scenarios tagged with both <code>@tag1</code> or <code>@tag2</code>.</td>
    </tr>
  </tbody>
</table>

> To learn more about tag expressions, refer to this Cucumber document: [Cucumber tag expression](https://cucumber.io/docs/cucumber/api/#tag-expressions).

Depending on the type of tag parameter passed during the function call, the function is executed with the corresponding tag expression.

## Using the AND tag expression

* **Description**: Execute the scenarios associated with all the input tags.
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
    * Mandatory: Optional  
* **Returns**: an instance of CucumberRunnerResult that includes the status of keyword and report folder location.
* **Example**:

```groovy
CucumberKW.runFeatureFileWithTags('Include/features/BDD Cucumber Tests/Jira Integration/KD-31800.feature', ["@BA","@regressiontest"] as String[])
```

## Using the OR tag expression

* **Description**: Execute the scenarios associated with one of the input tags.
* **Keyword name**: runFeatureFileWithTags
* **Keyword syntax**: runFeatureFileWithTags(relativeFilePath, tags)
* **Parameters**:
  * Name: relativeFilePath
    * Description: the folder relative path that starts from the current project location.
    * Parameter Type: String
    * Mandatory: Required
  * Name: tags
    * Description: which tags in the feature files should be executed.
    * Parameter Type: String varargs (String...)
    * Mandatory: Required
* **Returns**: an instance of CucumberRunnerResult that includes the status of keyword and report folder location.
* **Example**:

```groovy
CucumberKW.runFeatureFileWithTags('Include/features/BDD Cucumber Tests/Jira Integration/KD-31800.feature', "@BA, @regressiontest")
```