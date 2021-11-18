---
title: "Set a new default JRE for test projects"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/how-to-guides/set-new-default-JRE.html
description:
---

Katalon Studio uses the default embedded Java Runtime Environment (JRE) v8 to compile and run test projects. You can learn more about JRE v8 in the Oracle document here: [JRE v8](https://www.oracle.com/java/technologies/javase/jre8-readme.html).

From Katalon version 7.9.0 onwards, you can set your desired JRE package as the default one to compile and run test projects. You can also override the default configuration in console mode by using the environment variable.

> Important
>
> * This change applies to the JRE used for working with your test project, not the JRE used for running Katalon Studio.
> * Version compatibility between test projects and Java Compiler should be taken into consideration. For instance, Java 8 test projects are compatible with the default embedded JRE v8 in Katalon Studio.

This guide takes you through the steps to:
- Set a new default JRE for a Katalon Studio instance.
- Apply the new JRE to a test project.
- Run tests with another JRE in the command line.

## Set a new default JRE for a Katalon Studio instance

**Requirements**

* Katalon Studio version 7.9.0 onwards.
* Your machine already installed your desired JRE version (from v8 to v14).

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

To run and compile a test project with the new JRE:
1. Download `jaxb-api-2.3.1.jar` library. You can download JAXB API 2.3.1 from the Maven Repository website here: [JAXB API 2.3.1](https://mvnrepository.com/artifact/javax.xml.bind/jaxb-api/2.3.1).

you need add the `jaxb-api-2.3.1.jar` library to that project Refer to this guide to [add an external library to a project](https://docs.katalon.com/katalon-studio/docs/external-libraries.html#add-external-libraries).

Please make sure there is version compatibility between the test project and JRE. In case you want to check which Java version the test project is developed with, append the following script to a test case, then run it and see the log.
 
```groovy
println System.getProperty('java.version')
```

## Run tests with another JRE in the command line

**Requirements**

* Katalon Runtime Engine version 7.9 onwards.
* Your machine already installed your desired JRE version (from v8 to v14).
* An active [Katalon Runtime Engine](https://docs.katalon.com/katalon-studio/docs/license.html#katalon-runtime-engine) license.

To execute a test suite or test suite collection with another JRE in console mode, you need to add the environment variable: `KATALON_JAVA_HOME= <JRE_location>` and use it before Katalon commands. Below is a sample command on macOS and Linux for your reference:

`export KATALON_JAVA_HOME=/Library/Java/JavaVirtualMachines/zulu-11.jdk/Contents/Home`

`./katalonc ...`

Useful links:

* [Execute Katalon Studio in console mode](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#execute-katalon-studio-in-console-mode)

