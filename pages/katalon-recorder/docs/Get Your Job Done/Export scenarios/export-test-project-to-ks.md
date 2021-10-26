---
title: "Export Test Projects"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-recorder/docs/export-test-project-to-ks.html
description: 
---

From version 5.6.0 onwards, Katalon Recorder (KR) users can export multiple tests into a single file. This file is compatible with many other frameworks, such as Katalon Studio, Java Maven or Python.

This feature is especially useful to users outgrowing the capabilities of KR. As your work requirements and projects complexity increase, you can move your test artifacts and projects to other frameworks. This allows you to benefit from further advanced testing without losing your work.

The table below shows the full list of exporting features that KR offers, compared with Selenium IDE:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/5.6.0-release/KR%20vs.%20Selenium%20exporting%20features.png" width=100% alt="kr kr vs selenium in exporting">

## Export to Katalon Studio

To export a test project to KS, follow these steps:

1. Open Katalon Recorder.
2. On the left sidebar, go to **Export** > **Export to Katalon Studio**.

    The **Export to Katalon Studio** dialog appears as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/5.6.0-release/export-test-project-to-ks.png"  width=100% alt="kr export test project to ks">
    
3. Select the data you want to export.
4. Click **Export**.

## Export to other frameworks

> Requirements:
>
> * ChromeDriver installed.
> * Java IDE installed (preferably IntelliJ).

Follow these steps:

1. Open Katalon Recorder.
2. On the left sidebar, go to **Export** > **Export to other frameworks**.

3. Select a framework (e.g., **Java (WebDriver + TestNG)**).

4. Select the tests you want to export.
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/5.6.0-release/export-to-java.png" width=100% alt="kr export test project to ks">

   Katalon Recorder will also notify you here if there are incompatible commands.
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/5.6.0-release/incompatible-commands.png" width=100% alt="kr export test project to ks">
    
4. Click **Export**.
