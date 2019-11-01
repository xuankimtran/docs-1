---
title: "Katalon Studio for Linux (Console Mode)" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/katalon-studio-for-linux-console-mode.html 
redirect_from:
    - "/x/5QDR/"
    - "/katalon-studio/docs/katalon-studio-for-linux-console-mode/"
description: 
---

Katalon Studio for Linux (Ubuntu tested) supports both IDE and console mode versions. This guide covers installation steps for running Katalon Studio on Linux from the command line. For more details about console mode execution, please see [this document](/display/KD/Console+Mode+Execution).

## Download

Starting from **version 7.0.0**, you need a [Runtime Engine](https://docs.katalon.com/katalon-studio/docs/intro-RE.html) license to activate and run Katalon Studio or Katalon Studio Enterprise from the command line.

Log in to your Katalon account on the Katalon [website](https://katalon.com/download) and select the **Linux** version of **Runtime Engine** to download.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/katalon-studio-for-linux-console-mode/download.png)

## Installation

Be sure to install **OpenJDK 8** on your Ubuntu (NOT Oracle JDK). You can find the installation steps [here](http://openjdk.java.net/install/). Once you finish the installation, your `OpenJDK` information is displayed when you execute `java -version` command.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/katalon-studio-for-linux-console-mode/Screen-Shot-2018-02-07-at-11.50.50.png)

## Get Started

To execute tests, follow the following steps:  

* **Generate** a console mode command. You can generate command directly from the command generator.
* Copy and paste the generated command in Terminal.

For example:

```groovy
./katalonc -noSplash  -runMode=console -projectPath="/home/demokatalon/Katalon Studio/WebTesting/WebTesting.prj" -retry=0 -testSuitePath="Test Suites/TS_RegressionTest" -browserType="Chrome (headless)"
```

* Troubleshooting `NoClassDefFoundError` error: This happens because Oracle JDK is used. Please uninstall the current Oracle JDK, and then install the [Open JDK8](http://openjdk.java.net/install/).
