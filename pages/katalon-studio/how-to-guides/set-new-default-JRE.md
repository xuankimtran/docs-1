---
title: "Set a new default JRE for test projects"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/how-to-guides/set-new-default-JRE.html
description:
---

Katalon Studio uses the default embedded Java Runtime Environment (JRE) v8 to run a Katalon Studio instance and compile test projects. You can learn more about JRE v8 in the Oracle document here: [JRE v8](https://www.oracle.com/java/technologies/javase/jre8-readme.html).

From Katalon version 7.9.0 onwards, you can set your desired JRE package as the default one to compile and run test projects. You can also override the default configuration in console mode by using the environment variable.

> Notes:
>
> * This change applies to the JRE used to run your test projects, not the JRE used to run Katalon Studio.

This guide takes you through the steps to:
- Set a new default JRE for a Katalon Studio instance.
- Apply the new JRE to a test project.
- Run tests with another JRE in the command line.

## Set a new default JRE for a Katalon Studio instance

> Requirements:
> 
> * Katalon Studio version 7.9.0 onwards.
> * The desired JRE version (from v8 to v14) installed on your machine.

First, you need to set your desired JRE as the default JRE in Katalon Preferences. In this example, we set JRE 11 as the default one. Do as follows:

1. Open **Preferences** > **Java** > **Installed JREs**. 
   
   > Quick tips:
   >
   > Type "jre" in the search bar.

2. Click on button **Add...**.

   <img alt="Adding JRE" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/how-to-guides/change-jre/add-jre.png" width=90%>

3. In the displayed **Add JRE** dialog, select **Standard VM**.

   <img alt="select standard-VM" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/how-to-guides/change-jre/standard-vm.png" width=90%>

4. Browse to the `Home` folder of the JRE you wish to add and give it a name. Here, we name it JRE 11. Click **Finish**.

   <img alt="Browse to the JRE location" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/how-to-guides/change-jre/browse-jre.png" width=90%>

5. In the **Installed JREs** interface, check the newly added JRE to set it the default one. Click **Apply and close**.

   <img alt="Change default" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/how-to-guides/change-jre/default.png" width=90%> 

## Use the newly added JRE in a test project

To run a test project with the new JRE:

1. Download `jaxb-api-2.3.1.jar` library. You can download JAXB API 2.3.1 from the Maven Repository website here: [JAXB API 2.3.1](https://mvnrepository.com/artifact/javax.xml.bind/jaxb-api/2.3.1).

2. Add the `jaxb-api-2.3.1.jar` library to your test project. To do so, you can follow the instructions in this document: [Add an external library to a project](https://docs.katalon.com/katalon-studio/docs/external-libraries.html#add-external-libraries).

   > Notes: 
   > * The JRE version used to run test projects and JRE compiler compliance level should be compatible. For instance, Java 8 test projects are compatible with the default JRE compiler level 1.8. To alter JRE compiler compliance level, go to **Preferences** > **Java** > **Compiler**.
   > * In case you want to check which Java version the test project is developed with, add the following script to a test case, then run it and see the log.
   >
   > ```groovy
   > println System.getProperty('java.version')
   > ```
## Run tests with another JRE in the command line

> Requirements:
>
> * Katalon Runtime Engine version 7.9.0 onwards.
> * The desired JRE version (from v8 to v14) installed on your machine.
> * An active Katalon Runtime Engine license. To learn more about activating licenses, you can refer to this document here: [Katalon Runtime Engine](https://docs.katalon.com/katalon-studio/docs/license.html#katalon-runtime-engine).

To execute a test suite or a test suite collection with another JRE in console mode, you need to add the `KATALON_JAVA_HOME= <JRE_location>` environment variable and use it before Katalon commands. Below is a sample command on macOS and Linux for your reference:

`export KATALON_JAVA_HOME=/Library/Java/JavaVirtualMachines/zulu-11.jdk/Contents/Home`

`./katalonc ...`

## See also

* [Execute Katalon Studio in console mode](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#execute-katalon-studio-in-console-mode)

