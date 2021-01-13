---
title: "How to set a new default JRE for test projects?"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/how-to-guides/set-new-default-JRE.html
description:
---

The default embedded [Java runtime environment (JRE) v8](https://www.oracle.com/java/technologies/javase/jre8-readme.html) is used to run a Katalon Studio instance as well as compile and run test projects. To make it easy and flexible for you to work with different JRE versions and vendors, you can now set your desired JRE package as the default one to compile and run test projects. 

Those of you executing tests in console mode can also override the default configuration by using the environment variable.

> Important
>
> * This change applies to the JRE used for working with your test project, not the JRE used for running Katalon Studio.
> * Version compatibility between test projects and Java compiler should be taken into consideration. For instance, Java 8 test projects are compatible with the default embedded JRE v8 in Katalon Studio.

This guide takes you through the steps to change the default Java Compiler in **Katalon Preferences** (for example, set JRE 11 as the new default one) and configure which test projects to apply the change. For users executing tests in console mode, you can find the usage example of overriding the default configuration via the command line.

### Set a new default JRE for a Katalon Studio instance

**Requirements**

* Katalon Studio version 7.9 onwards.
* Your machine already installed your desired JRE version (from v8 to v14).

First, you need to set your desired JRE (for example, JRE 11) as the default JRE in Katalon Preferences. Do as follows:

1. Open **Preferences** > **Java** > **Installed JREs**. (Quick tip: Type "jre" in the search bar.)
2. Click on button **Add...**.

   <img alt="Adding JRE" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/how-to-guides/change-jre/add-jre.png" width=90%>

3. In the displayed **Add JRE** dialog, select **Standard VM**.

   <img alt="select standard-VM" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/how-to-guides/change-jre/standard-vm.png" width=90%>

4. Browse to the JRE or JDK 11's **Home** folder and give it a meaningful name. And click **Finish**.

   <img alt="Browse to the JRE location" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/how-to-guides/change-jre/browse-jre.png" width=90%>

5. In **Installed JREs**, set it as the default one and save the changes.

   <img alt="Change default" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/how-to-guides/change-jre/default.png" width=90%> 

### Use the newly added JRE in a test project 

Then, to run and compile a test project with the new JRE, you are required to add the JAXB API 2.3.1 `.jar` library to that project. 

Useful links:

* Download JAXB API 2.3.1 [here](https://mvnrepository.com/artifact/javax.xml.bind/jaxb-api/2.3.1).
* Refer to this guide to [add an external library to a project](https://docs.katalon.com/katalon-studio/docs/external-libraries.html#add-external-libraries).

Please make sure there is version compatibility between the test project and JRE. In case you want to check which Java version the test project is developed with, append the following script to a test case, then run it and see the log.
 
```groovy
println System.getProperty('java.version')
```

### Run tests with another JRE in the command line

**Requirements**

* Katalon Runtime Engine version 7.9 onwards.
* Your machine already installed your desired JRE version (from v8 to v14).
* An active [Katalon Runtime Engine](https://docs.katalon.com/katalon-studio/docs/license.html#katalon-runtime-engine) license.

To execute a test suite or test suite collection with another JRE in console mode, you need to add the environment variable: `KATALON_JAVA_HOME= &lt;JRE_location&gt;` and use it before Katalon commands. Below is a sample command on macOS and Linux for your reference:

`export KATALON_JAVA_HOME=/Library/Java/JavaVirtualMachines/zulu-11.jdk/Contents/Home`

`./katalonc ...`

Useful links:

* [Execute Katalon Studio in console mode](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#execute-katalon-studio-in-console-mode)

