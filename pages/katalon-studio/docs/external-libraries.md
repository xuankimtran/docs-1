---
title: "Libraries Management" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/external-libraries.html 
redirect_from:
    - "/display/KD/External+Libraries/"
    - "/display/KD/External%20Libraries/"
    - "/x/wQAo/"
    - "/katalon-studio/docs/external-libraries/"
    - "/katalon-studio/tutorials/import_java_library.html"
description: 
---

Katalon Studio allows using external Java `.jar` libraries either through project settings or adding them to a designated folder. You can leverage this to extend the capabilities of Katalon Studio and handle specific situations when needed. This article will show you how to add external libraries to Katalon Studio or replace the buil-in libraries with the external ones in a test project.

## Add External Libraries

You can add external libraries to a Katalon Studio's project in three different ways:

* Use Gradle.
* Go to Libraries Management of the Project Settings of a project.
* Copy and past a library's `.jar` file to Driver folder of a project.

### Use Gradle

Katalon Studio supports automatically downloading libraries from Maven repositories using Gradle. [Learn more](https://github.com/katalon-studio/gradle-plugin)

### Use Katalon Studio's project settings

1. In Katalon Studio, go to **Project** > **Settings** > **External Libraries** (In version 7.8 and later, go to **Project** > **Settings** > **Library Management** ). 
2. In **External Libraries**, click **Add** to browse your `.jar` file(s) (and its dependencies if any).  
3. Click on **Apply** and **OK** to save the settings.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/database-settings/add-external-lib.png" width=70%>

After saving the settings, Katalon will add the library file(s) to the project's **Drivers** folder and load the libraries.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/database-settings/db-in-driver.png" width=70%>

To remove an added external libraries, select a library, click **Remove** and click **OK**.

### Manually copy and paste .jar files to the Drivers folder

You can also manually copy and paste your `.jar` file (and its dependencies if any) into the **Drivers** folder of a project. You have to restart Katalon Studio (close and open the project again) to reload its class paths.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/database-settings/location.png" width=70%>

When your `.jar` library is recognized by the test engine, you should be able to use it. Refer to **[How to create a Custom Keyword](/katalon-studio/tutorials/create-custom-keyword/)** for information on how to use the email validation functionality from Apache open-source library **commons-validator-1.5.1.jar.**

## Exclude built-in libraries

With the ability to remove built-in libraries stored in the `.classpath` file of a project folder, you can replace a built-in library with an external one for flexible libraries usage in a test project.

**Requirements**

* An active Katalon Studio Enterprise license.
* Katalon Studio version 7.8.

1. Open **Project** > **Settings** > **Library Management** 
2. In the **Exclude the following built-in libraries** section, click **Add** to add a built-in library’s name that will be removed.
3. In the **External Libraries** section, click **Add** to browse an external library to replace the excluded one.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/database-settings/exclude-built-in-new.png" width=70%>