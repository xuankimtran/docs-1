---
title: "Running Cucumber Features File" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/running-cucumber-features-file.html 
redirect_from:
    - "/display/KD/Running+Cucumber+Features+File/"
    - "/display/KD/Running%20Cucumber%20Features%20File/"
    - "/x/PhLR/"
    - "/katalon-studio/docs/running-cucumber-features-file/"
description: 
---
From a Feature File
-------------------

Katalon Studio allows you to run the feature file instantly by itself to make sure it works properly. Open the desired **Features** file, click the **Play** button on the main toolbar.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/running-cucumber-features-file/Screen-Shot-2018-09-06-at-10.11.40-AM.png)

In Test Cases
-------------

Katalon Studio supports Cucumber keywords along with the original built-in keywords. The user doesn't have to import Cucumber libraries into Katalon Studio.

To include Cucumber _Feature_ file in Katalon Studio test case:

1. Execute a single Feature File (with or without tags)

* [runFeatureFile](https://docs.katalon.com/katalon-studio/docs/cucumber-kw-run-feature-file.html)
* [runFeatureFileWithTags](https://docs.katalon.com/katalon-studio/docs/cucumber-kw-run-feature-file-tag.html)

2. Execute multiple Feature Files (with or without tags)

* [runFeatureFolder](https://docs.katalon.com/katalon-studio/docs/cucumber-kw-run-feature-folder.html)
* [runFeatureFolderWithTags](https://docs.katalon.com/katalon-studio/docs/cucumber-kw-run-feature-folder-tag.html)

3. Execute using [Cucumber Runner](http://toolsqa.com/cucumber/junit-test-runner-class/).

* [runWithCucumberRunner](https://docs.katalon.com/katalon-studio/docs/cucumber-kw-run-cucumber-runner.html)

Cucumber Reports
----------------

There is **NO** custom report for executing Feature File. Katalon Studio uses only generated Cucumber **reports** for **Test Suite/Test Suite Collection** execution **level**, in which the test cases contain the Cucumber Features file. The generated Cucumber report of Test Suite/Test Suite Collection will be located in the same folder of Katalon Studio report's folder:

*   In Katalon Studio Tests Explorer, right-click at the desired **Report > Open Containing Folder**. Katalon Studio will redirect you to the local folder where Cucumber Reports are stored. 
*   Katalon Studio supports **three** formats for Cucumber reports: 
    *   JSON
    *   XML
    *   HTML

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/running-cucumber-features-file/Screenshot-at-Sep-04-20-01-21.png)
