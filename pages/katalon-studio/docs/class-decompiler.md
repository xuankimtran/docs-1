---
title: "Decompile Class File for Debugging"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/class-decompiler.html
description:
---

> Introduced in v7.9

As a precondition before debugging test scripts, you need to prepare and attach source code to a class file in Katalon Studio. 

You can read and interact with source code in previous versions by using the default feature of Eclipse Platform, Source Attachment. In version 7.9 onwards, Katalon Studio decompiles class files automatically and directly. Particularly, Katalon finds, downloads, and attaches source code behind the scene; hence, you do not have to manually perform these steps.

In case Katalon Studio fails to find the source attachment owing to the Internet connection or the `jar` file not found, it decompiles a class file and displays the decompiled source.

Katalon Class Decompiler is **enabled by default** for all Katalon Studio instances. This document gives you many details on additional configurations for it.  

## Use Class Decompiler for debugging test scripts

**Requirements**:

* An active Katalon Studio Enterprise license
* Katalon Studio v7.9 onwards
* Enabled Decompiler in Katalon **Preferences**

With **Katalon Class File Decompiler**, you can always access a class file's source code to set a breakpoint for debugging test scripts. Learn about [Debug Mode](https://docs.katalon.com/katalon-studio/docs/execute-a-test-case-or-a-test-suite.html#debug-mode) in Katalon Studio.

<img alt="decompiler-introduction" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execute-a-test-case-or-a-test-suite/decompiler-introduction.png" width=85%>

## Configure Class Decompiler

For further configurations, open the Decompiler in Katalon Preferences:

* Windows: Go to **Windows** > **Preferences** > **Java** > **Decompiler**.
* macOS: Go to **Katalon Studio** > **Preferences** > **Java** > **Decompiler**.

<img alt="decompiler-introduction" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/class-decompiler/decompiler.png" width=85%>

Katalon Studio supports the following Decompilers, including CFR, FernFlower (selected by default), Jad-Core, JD, and Procyon.

<img alt="decompiler-introduction" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/class-decompiler/decompilers.png" width=85%>

**Disable Class Decompiler**

To turn off **Katalon Class Decompiler**, you need to set **Class File Viewer** to the default viewer in **Preferences** > **General** > **Editors** > **File Associations**.

1. For "\**.class*" and "\**.class without source*" in **File Types**, select "*Class File Viewer*" in **Associated Editors**.
2. Click **Default** to set it as the default viewer.
3. Click **Apply and Close**.

   <img alt="decompiler-introduction" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/class-decompiler/switch.png" width=85%>






