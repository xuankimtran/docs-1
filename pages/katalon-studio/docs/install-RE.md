---
title: "Install Runtime Engine"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/install-RE.html
redirect_from:
    - "/x/5QDR/"
    - "/katalon-studio/docs/katalon-studio-for-linux-console-mode/"
    - "/katalon-studio/docs/katalon%20studio%20for%20linux%20console%20mode/"
    - "/katalon-studio/docs/katalon+studio+for+linux+console+mode/"
description:
---
Starting from **version 7.0.0**, you need a [Runtime Engine](https://docs.katalon.com/katalon-studio/docs/intro-RE.html) (RE) license to activate and run Katalon Studio or Katalon Studio Enterprise from the command line.

## Download RE

1. Log in to your Katalon account on the Katalon [website](https://katalon.com/download).
2. Select the compatible version of **Runtime Engine** with your operating system and download. For example, Linux version:
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/katalon-studio-for-linux-console-mode/download.png)

3. Unzip the package and move to the preferred directory to execute automation tests.

* **macOS**: If you currently use macOS Catalina, you have to enable Katalon Studio Engine application in System Preferences/ Security & Privacy/ General.

* **Linux**: Be sure to install **OpenJDK 8** on your Ubuntu (NOT Oracle JDK). You can find the installation steps [here](http://openjdk.java.net/install/). Once you finish the installation, your `OpenJDK` information is displayed when you execute `java -version` command.

    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/katalon-studio-for-linux-console-mode/Screen-Shot-2018-02-07-at-11.50.50.png)
    
  * Troubleshoot: You may encounter the `NoClassDefFoundError` error since Oracle JDK is being used. Please uninstall Oracle JDK, and then install [Open JDK8](http://openjdk.java.net/install/).

## RE Licensing

You need a valid RE license to use this add-on. RE license is a node-locked license. The number of licenses to acquire should be based on the number of processes and the maximum parallel sessions that you plan to execute.

* A license is linked to a single machine ID and for one execution session.
* A machine can be mapped to multiple licenses (if needed).
* The license can be transferred to a new machine for an online environment. For the offline environment, once converted, the license cannot be transferred to another machine until it is expired.

> Learn more about [RE License](https://docs.katalon.com/katalon-studio/docs/license.html).

## Activate RE

To activate RE, there are different activation methods based on the execution environment which can be online or offline. [Learn more](https://docs.katalon.com/katalon-studio/docs/activate-RE.html).

Once ready, navigate to the RE directory and execute the Katalon automation test in command-line mode (CLI) as normal. Learn more about [execution in console mode](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#execute-katalon-in-cmd).

## Get Started

To execute tests, follow the following steps:  

* Generate a console mode command. You can generate command directly from the command generator.
* Copy and paste the generated command in Terminal (macOS, and Linux)/ Command Prompt (Windows).

For example:

```groovy
./katalonc -noSplash  -runMode=console -projectPath="/home/demokatalon/Katalon Studio/WebTesting/WebTesting.prj" -retry=0 -testSuitePath="Test Suites/TS_RegressionTest" -browserType="Chrome (headless)"
```
