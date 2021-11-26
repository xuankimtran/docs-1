---
title: "Selenium/TestNG/JUnit Migration to Katalon Studio"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/selenium-testng-junit-migration.html
---

From Katalon Studio version 7.4.0 onwards, you can migrate your test cases from Selenium, TestNG, or JUnit projects to Katalon Studio. With the supported features and keywords,you can execute and maintain your existing Selenium, TestNG and Junit projects with Katalon without starting everything from scratch.

Katalon Studio supports:
* Selenium version 3.x
* TestNG version 6.11
* JUnit version 4.12

> Requirements:
> * Katalon Studio version 7.4.0 onwards.

> You can download our Github sample project for TestNG migration: [TestNG Migration](https://github.com/katalon-studio-samples/TestNG-Migration).
## Supported features & keywords to facilitate the migration
### Java class files

You can create, view and edit Java class files. 

To create a new Java class file, in the **Tests Explorer** panel, go to the **Include > scripts > groovy** folder, right-click and choose **New > Java Class**. Choose a package and enter class name in the **New** dialog.
   
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/Selenium-TestNG-Migration/new-java-class.png" width="362" alt="Create Java Class files">

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/Selenium-TestNG-Migration/java1.png" width="285" alt="Sample Java Class file">
   
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/Selenium-TestNG-Migration/java-script.png" width="501" alt="Sample Java Class file">

## Built-in TestNG/JUnit keywords
### Install TestNG/JUnit Keywords plugin

You can enable the built-in keywords in the manual view by using the **TestNG/JUnit Keywords** plugin. You can download the plugin from Katalon Store here: [TestNG/JUnit Keywords](https://store.katalon.com/product/180/TestNG-JUnit-Keywords). 

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/Selenium-TestNG-Migration/testng-kw.png" width="260" height="">

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/Selenium-TestNG-Migration/testng-kw-2.png" width="334" height="">

After installing the plugin, go to Katalon Studio and click **Reload Plugins**.

If you want to use this plugin offline, you can refer to this document:[Use Private Plugins](https://docs.katalon.com/katalon-studio/docs/kse-use-plugins.html#use-private-plugins). Because the **TestNG/JUnit Keywords** plugin is a **platform** plugin, you need to move the plugin package .jar file in the `<project_name>/Plugins/platform` folder.
### TestNG/JUnit Keywords

TestNG/JUnit Keywords Plugin offers 3 built-in keywords to help you run TestNG/JUnit tests as follows:

<details><summary><code>runTestNGTestClasses</code></summary>

**Syntax**: `runTestNGTestClasses(List testClasses)`

**Description**: run TestNG test classes and generate TestNG report at the running report folder.

**Parameters**:
<br>
<table>
<thead>
  <tr>
    <th>Parameters</th>
    <th>Type</th>
    <th>Description</th>
    <th>Mandatory</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>testClasses</td>
    <td>List</td>
    <td>List of TestNG test classes</td>
    <td>Required</td>
  </tr>
  <tr>
    <td>flowControl</td>
    <td>FailureHandling</td>
    <td>Specify failure handling schema to determine whether the execution should be allowed to continue or stop. <br>To learn more about failure handling settings, you can refer to this document: <a href="https://docs.katalon.com/katalon-studio/docs/failure-handling.html#default-failure-handlingbehavior" target="_blank" rel="noopener noreferrer">Failure handling</a>.</td>
    <td>Optional</td>
  </tr>
</tbody>
</table>

</details>

<details><summary><code>runTestNGTestSuites</code></summary>


**Syntax**: `runTestNGTestSuites(List testSuites)`

**Description**: run TestNG test suites and generate TestNG report at the running report folder.

**Parameters**:

<table>
<thead>
  <tr>
    <th>Parameters</th>
    <th>Type</th>
    <th>Description</th>
    <th>Mandatory</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>testSuites</td>
    <td>List</td>
    <td>List of TestNG test suites as .xml files</td>
    <td>Required</td>
  </tr>
  <tr>
    <td>flowControl</td>
    <td>FailureHandling</td>
    <td>Specify failure handling schema to determine whether the execution should be allowed to continue or stop. <br>To learn more about failure handling settings, you can refer to this document: <a href="https://docs.katalon.com/katalon-studio/docs/failure-handling.html#default-failure-handlingbehavior" target="_blank" rel="noopener noreferrer">Failure handling</a>.</td>
    <td>Optional</td>
  </tr>
</tbody>
</table>
</details>


<details><summary><code>runJUnitTestCases</code></summary>

**Syntax**: `runJUnitTestClasses(List TestClasses)`

**Description**: run JUnit test cases and generate JUnit report at the running report folder.

**Parameters**:

<table>
<thead>
  <tr>
    <th>Parameters</th>
    <th>Type</th>
    <th>Description</th>
    <th>Mandatory</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>testClasses</td>
    <td>List</td>
    <td>List of JUnit test classes</td>
    <td>Required</td>
  </tr>
  <tr>
    <td>flowControl</td>
    <td>FailureHandling</td>
    <td>Specify failure handling schema to determine whether the execution should be allowed to continue or stop. <br>To learn more about failure handling settings, you can refer to this document: <a href="https://docs.katalon.com/katalon-studio/docs/failure-handling.html#default-failure-handlingbehavior" target="_blank" rel="noopener noreferrer">Failure handling</a>.</td>
    <td>Optional</td>
  </tr>
</tbody>
</table>

</details>

## Migrate Selenium/TestNG/JUnit projects to Katalon Studio

> Requirements:
>
> Install Gradle version 5 or prior. You can download from the Gradle website here: [Gradle](https://gradle.org/).

To migrate Selenium/TestNG/JUnit scripts to a Katalon Studio project, do as follows:

1. Create a new project in Katalon Studio. Go to **File > New > Project**

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/Selenium-TestNG-Migration/KS-Selenium-Create-new-project.png" width="70%" height="" alt="Create a new project">

2. Build project dependencies.

   2.1 Open the .gradle file and add Java dependencies of your Selenium/TestNG/JUnit project.
      
      > Notes:
      > 
      > * You only need to add the JUnit/TestNG project dependencies that are not Selenium dependencies.
      > * Katalon Studio has bundled TestNG, JUnit and Selenium dependencies, you don't need to declare those dependencies again. 

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/Selenium-TestNG-Migration/build-gradle.png" width="629" height="" alt="Selenium migration gradle">

   2.2 Open the **Command Prompt** or **Terminal** and navigate to the folder of your project. Enter `gradle katalonCopyDependencies`, then wait for the Gradle to build successfully.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/Selenium-TestNG-Migration/build-success.png" width="70%" alt="Selenium migration build successful">

   2.3 Reopen the project to reload all the dependencies.

3. Copy and paste the source code of your Selenium/TestNG/JUnit project in the `Include/scripts/groovy` folder of your Katalon project. 

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/Selenium-TestNG-Migration/KS-Selenium-Copy-the-source-code.gif" width="70%" alt="Add TestND source code">

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/Selenium-TestNG-Migration/step5.png" width="322" alt="Add TestND source code">

4. Copy and paste other resources of your Selenium/TestNG/JUnit project in the `Include` folder of your Katalon project (if any).
   
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/Selenium-TestNG-Migration/KS-Selenium-Add-resources.gif" width="70%" alt="Add TestNG resoureces">

5. To reload the source code and resources from your your Selenium/TestNG/JUnit project, right-click at the `Include` folder, then click **Refresh**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/Selenium-TestNG-Migration/KS-Selenium-Reload-source-code.png" width="322" alt="Reload TestNG source code and resoureces">

6. Create a test case that includes TestNG keywords to run TestNG test suites or JUnit test classes.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/Selenium-TestNG-Migration/step7.png" width="629" alt="Selenium migration step 7">

> Notes:
> 
> For real-time monitoring and better reporting capabilities, consider integrating your project with Katalon TestOps. See also [Upload Test Results to Katalon TestOps from Katalon Studio](https://docs.katalon.com/katalon-studio/docs/katalon-analytics-beta-integration.html).

You can also follow the steps in this video tutorial to migrate Selenium/TestNG/JUnit scripts to a Katalon Studio project.

<iframe width="560" height="315" src="https://www.youtube.com/embed/jpnAMZQtuiI" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

