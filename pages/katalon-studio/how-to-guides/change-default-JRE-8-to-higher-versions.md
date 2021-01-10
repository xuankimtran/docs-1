---
title: "How to change default JRE 8 to higher versions"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/how-to-guides/change-default-JRE-8-to-higher-versions.html
description:
---
[Java runtime environment (JRE)](https://www.oracle.com/java/technologies/javase/jre8-readme.html) - in short, is everything software developers and vendors need to execute Java code or applications.

In general, upgrading JRE 8 to higher versions helps:
- Fix bugs in JRE 8.
- Enhance existing features.
- Add new features.

> Refer to [Oracle release note](https://www.oracle.com/java/technologies/javase/jdk-relnotes-index.html) of each version for more details.

This guide takes you through the steps to change Katalon’s embedded JRE as Java Compiler 8 to another vendor and higher versions (from version 8 to version 14) in **Katalon Studio** and **Katalon Runtime Engine**.

## Prerequisites

You need:
- An active [Katalon Runtime Engine](https://docs.katalon.com/katalon-studio/docs/license.html#katalon-runtime-engine) license.
- A [Katalon API Key](https://docs.katalon.com/katalon-analytics/docs/ka-api-key.html).
- Katalon Studio version 7.9 onwards.

Your machine should:

Install the exact JRE version you want to upgrade (within version 8 to version 14).

- Download [JRE 9](https://www.oracle.com/br/java/technologies/javase/javase9-archive-downloads.html).
- Download [JRE 10](https://www.oracle.com/java/technologies/java-archive-javase10-downloads.html).
- Download [JRE 11](https://www.oracle.com/java/technologies/javase/jdk11-archive-downloads.html).
- Download [JRE 12](https://www.oracle.com/java/technologies/javase/jdk12-archive-downloads.html).
- Download [JRE 13](https://www.oracle.com/java/technologies/javase-jdk13-downloads.html).
- Download [JRE 14](https://www.oracle.com/java/technologies/javase/jdk14-archive-downloads.html).

## Change default JRE 8 to higher versions

### Katalon Studio

   To conduct, do as follows:

   1. Open **Windows/Preferences**, select **Installed JRE** section.

      <img alt="Installed JRE" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/change-default-JRE-8-to-higher-versions/jre11_1.jpg" width=90%>

   2. Click on the **Add External...** button and locate the location of JRE or JDK 11.

      <img alt="Add button" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/change-default-JRE-8-to-higher-versions/photo_2020-04-07%2012.07.55.jpeg" width=90%>

   3. Change the default JDK or JRE from JRE 8 to JDK or JRE 11.
   
      <img alt="Change default" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/change-default-JRE-8-to-higher-versions/photo_2020-04-07%2012.07.58.jpeg" width=90%> 

   4. Download **javax-api.jar** file and copy to **Drivers** folder:

      <img alt="Change default" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/change-default-JRE-8-to-higher-versions/photo_2020-04-07%2012.18.44.jpeg" width=90%>

   5. Run a test case and see the result.

      <img alt="Console log" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/change-default-JRE-8-to-higher-versions/photo_2020-04-07%2012.08.01.jpeg" width=90%>

   In case you want to check your Java version, here's the script:

   ```groovy
   println System.getProperty('java.version')
   ```

### Katalon Runtime Engine

   To add another JRE, you need to add the environment variable: **KATALON_JAVA_HOME= &lt;location new JRE&gt;**

   Below is a sample command on macOS and Linux for your reference:
   ```
   export KATALON_JAVA_HOME=/Library/Java/   JavaVirtualMachines/zulu-11.jdk/Contents/Home
   ./katalonc ...
   ```
### Q&As
   1. **Q: If I upgrade to version 9 in Katalon Studio and version 10 in Katalon Runtime Engine, the code or application in which tool will affect?**
   
      *A: It depends on the required environment of Katalon Studio and Katalon Runtime Engine.*
   
   2. **Q: Is it possible to change to lower JRE versions?**
      
      *A: Changing from a higher version to the lower one is risky because of not backward compatible, so our suggestion is "NO".*
