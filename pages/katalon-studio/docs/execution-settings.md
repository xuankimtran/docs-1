---
title: "Execution Settings" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/execution-settings.html 
redirect_from:
    - "/display/KD/Execution+Settings/"
    - "/display/KD/Execution%20Settings/"
    - "/x/cgFO/"
    - "/katalon-studio/docs/execution-settings/"
description: 
---
Execution settings help users to set preferred behaviors for Katalon Studio during test execution. You can configure general execution preferences by accessing from the main menu: **Project > Settings > Execution**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-settings/execution-settings.png" width="" height="">

### Default Execution Settings

* **Default execution**: The default environment that Katalon Studio uses for executing test scripts.

* **Default Smart Wait**: to tell the web driver to wait for the web page to become static before any operations perform. [Learn more](https://docs.katalon.com/katalon-studio/docs/webui-smartwait.html).

* **Default wait for element timeout**: The default timeout period (in seconds) that Katalon Studio waits for the application under test to be loaded when executing automation test.

* **Log executed test steps**: to decide whether the logs include executed test steps or not. [Learn more](https://docs.katalon.com/katalon-studio/docs/working-with-execution-log.html#log-executed-test-steps).

* **Post-Execution Options**: These options decide the actions that Katalon Studio performs after finishing test execution.

  * Open report: Specify whether the report generated after your test suite's execution finishes is to be opened immediately.
  * Terminate drivers: Specify when any driver remains after execution is terminated.

### WebUI Settings

These settings decide the general behavior of Katalon Studio when executing WebUI testing.

* **Delay between actions**: The time for Katalon Studio to wait between test steps when executing test cases.
* **Default wait when IE hangs**: Specify the default period of waiting that Katalon Studio should use in case IE hangs.
* **Default page load timeout**:

  * *Wait until the page is loaded*: Katalon Studio waits for the web page to load completely.
  * *Wait for (in seconds)*: The default timeout period (in seconds) that Katalon Studio waits for the web page to load.
