---
title: "What's new in v7.9?" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/new/what-is-new-79.html
description: What's new in Katalon Studio 7.9?
---

**Jan 19, 2021**

Today we have released Katalon Studio 7.9 with major improvements for both Katalon Studio and Katalon Studio Enterprise Editions.

This version upgraded Eclipse IDE framework to the latest version, supported Class File Decompiler for debug, enhanced the integration with application lifecycle management (ALM) tools, and resolved several bugs. This document describes the enhancement highlights available in 7.9.

> Important
>
> Please be noted that you will not be able to use **Check for updates...** to upgrade to v7.9+ due to the core engine upgrade (but you can upgrade from v7.9 to later versions via **Check for updates...**). 
>
> * Download the latest version from [our website](https://www.katalon.com/download/). 
>
> * To reuse Preferences from previous versions, refer to [this guide](https://docs.katalon.com/katalon-studio/docs/katalon-studio-preferences.html#import-preferences).

* See [what’s new in v7.8](https://docs.katalon.com/katalon-studio/new/what-is-new-78.html).

## Multiple enhancements enabled by Eclipse Platform upgrade

Upgrading the Eclipse platform to version 4.16 has been looked forward to by our community users. This major improvement was released as an alpha version for more than a year before our team is confident with this upgrade.

### Performance amplification 

You now can enjoy a Katalon Studio IDE performing more robustly while consuming less memory on the latest OS versions.

### IDE look and feel

Moreover, the IDE look and feel is substantially improved with:

* The more freshened interface on macOS 10.14 - 10.15, Windows 10, and Ubuntu 19.04 - 20.04.
* Extending Dark theme support in additional Windows areas, including the text of radio buttons, check-box, and group control.

   Before: 
   
   <img alt="before" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/what-is-new/1_before.PNG" width=40%> 

   After: 
   
   <img alt="after" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/what-is-new/1_after.PNG" width=40%>

### Flexibility to use different JRE (from v8 to v14) for your test projects

The default embedded Java Runtime Environment (JRE) v8 is used to run a Katalon Studio instance, and compile, run your test projects. To make it easy and flexible for you to use your desired JRE version and vendor, you can now set another JRE as the default one for compiling and running test projects. Those of you running tests in console mode can flexibly use another JRE for test execution by using environment variable.

See the [how-to guide](https://docs.katalon.com/katalon-studio/how-to-guides/set-new-default-JRE.html) for more detailed instructions.

<img alt="Change default" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/how-to-guides/change-jre/default.png" width=70%> 

### Katalon Class File Decompiler for debug

In previous versions, you have to manually find, and attach source code of the 3rd-party libraries to prepare for debugging test scripts. In v7.9 and later, with **Katalon Class File Decompiler** enabled by default for all Katalon Studio instances, you can always access a class file's source code for debug. [Learn more](https://docs.katalon.com/katalon-studio/docs/class-decompiler.html)

<img alt="decompiler-introduction" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/class-decompiler/decompiler.png" width=70%>

## More reliable and secure macOS packages

All Katalon Studio and Katalon Runtime Engine packages now are to be notarized for macOS Catalina (10.15.x) as a required step in our distribution process. Understand [why we notarize our macOS software](https://developer.apple.com/documentation/xcode/notarizing_macos_software_before_distribution#overview).

## qTest Integration Enhancements

We made several changes to improve the integration with qTest. Particularly, you can pass Build information and submit screenshots to qTest Manager along with other test logs and reports for analyzing test results better.

Notably, to continue using the integration in this version, you need to map the execution status to activate Automation Integration in qTest. [Learn more](https://docs.katalon.com/katalon-studio/docs/qtest-integration.html#execution-status-mapping)

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/status-map-ks.png" width=70%>

Useful link:

* [CLI] Submit automation test status with build information by -qTestBuildLabel and -qTestBuildURL. [Learn more](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#integration-options)

## Newly supported browser versions

* Support Chrome 87.
* Support Microsoft Edge (Chromium) 87.
* Support latest embedded GeckoDriver

