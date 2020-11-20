---
title: "Dependencies Management with Native Gradle Support (P.o.C)"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/dependencies-management-gradle-support.html
---

> Important
>
> This Proof of Concept (PoC) is not ready for production use. We recommend using this PoC for evaluation purposes only.

Previously, Katalon Studio provides a [Gradle Plugin](https://plugins.gradle.org/plugin/com.katalon.gradle-plugin) to simplify and automate some tasks in Katalon Studio; however, some users find it cumbersome, and dependencies management is pretty bare-bones.

Empowered by the [Eclipse Buildship](https://www.eclipse.org/community/eclipse_newsletter/2018/february/buildship.php), the Gradle wrapper and native Gradle support in Katalon Studio makes dependencies management with Maven or Gradle more streamlined and robust. You are no longer required to use any Command-line or third-party tools and free to decide which Gradle version to use in your test project instead of being limited to use only the fixed version that you have installed on your local machine earlier. 

This feature is particularly beneficial to Katalon users who use external libraries for multiple test projects and prefer to use Gradle for managing their build process. You can now run Gradle tasks with better Gradle editor support without installing Gradle in Katalon Studio or using an external terminal/command prompt. It substantially reduces your manual effort when you can manage and download external libraries in fewer steps than before. 

This manual introduces what built-in Gradle support looks like and how to use it in Katalon Studio.

> Download Katalon Studio v8.0.0.rc [here](https://github.com/katalon-studio/katalon-studio/releases/tag/untagged-4d3c4cf7c0b00ec1ac5c)

## Gradle Settings

Katalon Studio turns on the built-in Gradle integration by default for all projects.

> When you create/open a project for the first time, it takes 2 to 5 minutes to download Gradle.



You can access Gradle settings by going to **Katalon Studio** > **Preferences** > **Gradle**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/gradle/gradle-preferences.png">

To change the Gradle settings of an opening project, go to **Project** > **Properties** > **Gradle**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/gradle/project-menu.png" width=30%>

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/gradle/project.png" width=100%>

## Gradle Tasks

To use Gradle tasks, open the **Gradle Tasks** tab at the bottom dock:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/gradle/gradle-tasks.png" width=100%>

* To sync Gradle tasks when you change the `build.gradle` file, on the top right corner, click the **Refresh Tasks for All Projects** button.

* To view and use Katalon Gradle tasks, on the top right corner, click on the three-dot button and select **Show All Tasks**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/gradle/context-menu.png" width=50%>

   All Katalon Tasks are available under the **other** category of the Gradle task tree: 

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/gradle/other-gradle.png" width=100%>

* Click on any item on the Gradle task tree to run the dedicated Gradle tasks. For the **katalonCopyDependencies** task, you need to select **Project** > **Refresh** to refresh the project classpath after successfully running the task.

## Usage Examples of katalonCopyDependencies task

On Tests Explorer, open the `build.gradle` file, in its editor:

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