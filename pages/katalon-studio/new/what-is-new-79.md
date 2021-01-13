---
title: "What's new in v7.9?" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/new/what-is-new-79.html
redirect_from:
    - "/katalon-studio/new/what-is-new.html"
    - "/katalon-studio/new/what-is-new/"
    - "/katalon-studio/new/"
    - "/display/KD/Release+Notes/"
    - "/display/KD/Release%20Notes/"
description: What's new in Katalon Studio 7.9?
---

**Jan 19, 2021**

Today we have released Katalon Studio 7.9 with major improvements for both Katalon Studio and Katalon Studio Enterprise Editions.

This version upgraded Groovy and Eclipse IDE frameworks to the latest versions, extended more utilities for debugging test scripts, and enhanced the integration with application lifecycle management (ALM) tools, and resolved many regressions and bugs. This document describes the enhancement highlights available in 7.9.

> For a detailed list of enhancements and bug fixes, see [release notes](https://docs.katalon.com/katalon-studio/new/version-70.html).

> [What’s new in v7.8?](https://docs.katalon.com/katalon-studio/new/what-is-new-78.html)

### **Multiple enhancements enabled by Eclipse Platform upgrade**

Upgrading the Eclipse platform to version 4.16 has been looked forward to by our community users. This major improvement was released as an alpha version for more than a year before our team is confident with this upgrade.

### Performance amplification 

You now can enjoy a Katalon Studio IDE performing more robustly while consuming less memory on the latest OS versions.

### IDE look and feel

Moreover, the IDE look and feel is substantially improved with:

* The more freshened interface on macOS 10.14 - 10.15, Windows 10, and Ubuntu 19.04 - 20.04.
* Extending Dark theme support in additional Windows areas, including the text of radio buttons, check-box, and group control.

### Flexibility to configure different JRE versions (from v8 to v14) for working with your test projects

The default embedded Java Runtime Environment (JRE) is used to run a Katalon Studio instance, compile, and run your test projects. To make it easy and flexible for you to work with different Java projects and different JRE vendors, you can now specify your desired JRE package in Katalon Preferences to compile and run tests.

Those of you running tests in console mode can also change the default JRE or override the configuration in Katalon Preferences by using the environment variable.

See the [how-to guide]() for more detailed instructions.

This change only impacts the JRE used for working with your test project, not the JRE used for running the application.

### **Empowered Groovy scripting capabilities**

Another primary enhancement is shipped in this release is the Groovy framework upgrade from v2.4.7 to v3.0. Along with the Eclipse upgrade, it was also tested by our pioneer users for months before its official launch.

This upgrade addresses the limitations of Groovy 2.4.7 and equips those of you using Groovy script with the [latest Groovy technologies](). 

### **More reliable and secure macOS packages** 

All Katalon Studio and Katalon Runtime Engine packages now are to be notarized for macOS Catalina (10.15.x) as a required step in our distribution process. [Learn more about why we need to notarize our software.]?

### **Extended utilities for debugging**

To read the 3rd-party libraries' source code for debugging test scripts, you can either attach source code, a default feature supported by Eclipse or decompiling the class files. [Learn more]()

In previous versions, only users with Enterprise license can view and interact with the source code compressed in the `com.kms.katalon.core*` packages. Now, this feature is accessible by all Katalon Studio users.

### **qTest Integration Enhancements**

We made several changes to improve the integration with qTest. Particularly, those of you using qTest can pass Build information and submit screenshots to qTest Manager along with other test logs and reports for analyzing test results better.

Notably, to continue using the integration in this version, you need to map the execution status to activate Automation Integration in qTest. [Learn more]()

Useful links:

* Support uploading screenshots in test results to qTest. [Learn more]()
* [CLI] Submit automation test status with build information by -qTestBuildLabel and -qTestBuildURL. [Learn more]()

### **Newly supported browser versions**

* Support Chrome 87.
* Support Microsoft Edge (Chromium) 87.

