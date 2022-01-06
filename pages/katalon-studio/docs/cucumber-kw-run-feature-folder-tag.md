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
      <td>Scenarios tagged with both <code>@tag1</code> or <code>@tag2</code>.</td>
    </tr>
  </tbody>
</table>

> To learn more about tag expressions, refer to this Cucumber document: [Cucumber tag expression](https://cucumber.io/docs/cucumber/api/#tag-expressions).

## Using the AND tag expression

* **Description**: Query the feature files in the specified folder, and execute the scenarios associated with all the input tags.
* **Keyword name**: runFeatureFolderWithTags.
* **Keyword syntax**: runFeatureFolderWithTags(folderRelativePath, tags, flowControl).
* **Parameters**:
  * Name: folderRelativePath
    * Description: the folder relative path that starts from the current project location.
    * Parameter Type: String.
    * Mandatory: Required.
  * Name: tags
    * Description: which tags in the feature files should be executed.
    * Parameter Type: String[].
    * Mandatory: Required.
  * Name: flowControl
    * Description: a `com.kms.katalon.core.model.FailureHandling` instance that controls the running flow.
    * Parameter Type: FailureHandling.
    * Mandatory: Optional.
* **Returns**: an instance of CucumberRunnerResult that includes the status of keyword and report folder location.
* **Example**:

```groovy
CucumberKW.runFeatureFolderWithTags('Include/features/BDD Cucumber Tests',['@BA','@regressiontest'] as String[])
```

## Using the OR tag expression

* **Description**: Query the feature files in the specified folder, and execute the scenarios associated with one of the input tags.
* **Keyword name**: runFeatureFolderWithTags
* **Keyword syntax**: runFeatureFolderWithTags(folderRelativePath, tags)
* **Parameters**:
  * Name: folderRelativePath
    * Description: the folder relative path that starts from the current project location.
    * Parameter Type: String.
    * Mandatory: Required.
  * Name: tags
    * Description: which tags in the feature files should be executed.
    * Parameter Type: String varargs (String...).
    * Mandatory: Required.
* **Returns**: an instance of CucumberRunnerResult that includes the status of keyword and report folder location.
* **Example**:

```groovy
CucumberKW.runFeatureFolderWithTags('Include/features/BDD Cucumber Tests', '@BA','@regressiontest')
```
