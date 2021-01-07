---
title: "How to change default JRE 8 to higher versions"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/how-to-change-default-JRE-8-to-higher-versions.html
description:
---
This guide will take you through the steps to change Katalon’s embedded JRE as Java Compiler 8 to another vendor and higher versions (from version 8 to version 14) in **Katalon Studio** and **Katalon Runtime Engine**.

### In Katalon Studio

To change to higher versions, do as follows:

- Open **Windows/Preferences**, select **Installed JRE** section

   <img alt="Installed JRE" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/change-default-JRE-8-to-higher-versions/jre11_1.jpg" width=90%>

- Click on the **Add External...** button and locate the JRE/JDK 11 location

   <img alt="Add button" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/change-default-JRE-8-to-higher-versions/photo_2020-04-07%2012.07.55.jpeg" width=90%>

- Change the default JDK/JRE from JRE8 to JDK/JRE 11
   
   <img alt="Change default" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/change-default-JRE-8-to-higher-versions/photo_2020-04-07%2012.07.58.jpeg" width=90%> 

- Download **javax-api.jar** file and copy to Drivers folder:

   <img alt="Change default" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/change-default-JRE-8-to-higher-versions/photo_2020-04-07%2012.18.44.jpeg" width=90%>

- Run a test case and see the result

   <img alt="Console log" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/change-default-JRE-8-to-higher-versions/photo_2020-04-07%2012.08.01.jpeg" width=90%>

In case you want to check your Java version, here's the script:

```groovy
println System.getProperty('java.version')
```

### In Katalon Runtime Engine

To add another JRE, you need to add the environment variable: **KATALON_JAVA_HOME= &lt;location new JRE&gt;**

Below is a sample command on macOS and Linux for your reference:

```
export KATALON_JAVA_HOME=/Library/Java/JavaVirtualMachines/zulu-11.jdk/Contents/Home
./katalonc ...
```