---
title: "Dependencies Management with Native Gradle Support (P.o.C)"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/dependencies-management-gradle-support.html
---

> Important
>
> This Proof of Concept (PoC) is not ready for production use. We recommend using this PoC for evaluation purpose only.

Previously, Katalon Studio provides [a Gradle Plugin](https://plugins.gradle.org/plugin/com.katalon.gradle-plugin) to help users simplify and automate some tasks in Katalon Studio. However, some users find it cumbersome and the dependency management is pretty barebones.

With the **Gradle** wrapper and native **Gradle** support in Katalon Studio, it becomes more streamlined and robust when you can manage dependencies with Maven or Gradle right in Katalon Studio without a requirement of using Command line or any third-party tools. You are free to decide which gradle version to use in your test project instead of a fixed version of gradle you have installed locally.

This feature is especially benefiecial to Katalon users who use external libraries for multiple test projects, and prefer to use Gradle for managing their build process. Now you can run Gradle tasks with better Gradle editor support and without installing Gradle in Katalon Studio or using an external terminal/command prompt. This substaintially reduces your manual effort when you can manage and download external libraries in fewer steps than before.

Build-in Gradle: [Eclipse Buildship](https://www.eclipse.org/community/eclipse_newsletter/2018/february/buildship.php)

This tutorial shows you how to trial using this PoC feature configure

> Download Katalon Studio v8.0.0.rc [here](https://github.com/katalon-studio/katalon-studio/releases/tag/untagged-4d3c4cf7c0b00ec1ac5c)

## Gradle Settings

The built-in Gradle support is enabled by default for all projects. 

> When you create/open a project for the first time, it takes 2 to 5 minutes to download Gradle.

You can access Gradle settings by going to **Katalon Studio** > **Preferences** > **Gradle**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/gradle/gradle-preferences.png">

To change Gradle settings of an opening project, go to **Project** > **Properties** > **Gradle**. 

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/gradle/project-menu.png" width=30%>

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/gradle/project.png" width=100%>

## Gradle Tasks

To use Gradle tasks, open the **Gradle Tasks** tab at the bottom dock:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/gradle/gradle-tasks.png" width=100%>

* Click **Refresh Tasks for All Projects** button at the top right of the Gradle Tasks tab when you make any change to the `build.gradle` file to sync Gradle tasks.

* To view and use Katalon Gradle tasks, click on the 3 dot buttons and select **Show All Tasks**

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/gradle/context-menu.png" width=50%>

   All Katalon Tasks are available under the other category of the Gradle task tree: 

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/gradle/task-tree.png" width=100%>

* Click on any item on the Gradle task tree to run the dedicated Gradle tasks. For **katalonCopyDependencies** task, you need to select **Project** > **Refresh** to refresh project classpath after the task runs successfully.

## Usage Examples

The `build.gradle` file:

1. You can use `compile` to add dependencies to a project:

```groovy
compile 'io.rest-assured:json-schema-validator:3.2.0'
```

2. Use the following command to exclude dependencies:

```groovy
compile ('io.rest-assured:json-schema-validator:3.2.0') {
   	exclude group: 'org.hamcrest', module: 'hamcrest-core' 
}
```