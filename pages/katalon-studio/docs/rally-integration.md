---
title: "Rally Integration"
sidebar: katalon_studio_docs_sidebar
root: "qtest-integration"
permalink: katalon-studio/docs/rally-integration.html
description: Instruction of how to integrate Rally and Katalon Studio
---

Katalon Studio allows you to link Katalon Studio test cases and view test execution results in Rally. 

> Requirements:
> * Katalon Studio version 7.0.0 onwards.
> * An active Katalon Studio Enteprise license. To learn more about activating your Katalon Studio license, you can refer to this document: [Activate Katalon license](https://docs.katalon.com/katalon-studio/docs/activate-license.html#activate-a-license-with-internet-access).

## Install the Rally Integration plugin

To download and install the **Rally Integration** plugin, you can go to the Katalon Store here: [Rally Integration](https://store.katalon.com/product/125/Rally-Integration). 

To activate the installed plugin, navigate to Account Settings in Katalon Studio and click **Reload Plugin**.
## Configure Rally in Katalon Studio

Go to **Project Setting > Plugins > Rally**. Input the following information:

* **Rally URL**: `https://rally1.rallydev.com/`.
* **API Key**: the API key in Rally. To generate an API key in Rally, you can refer to the Broadcom documentation: [Create an API key](https://knowledge.broadcom.com/external/article/10814/rally-how-to-create-an-api-key.html).

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/rally-integration/KS-RALLY-Enable-Rally-integration.png" width="70%" alt="Enable Rally integration">

Once connected successfully, Katalon retrieves your available workspaces from Rally. Choose the Rally workspace you want to work on.
## Map test cases between Katalon Studio and Rally

Katalon Studio provides an easy way to map a Katalon test case to an existing Rally test case. Follow these steps:
### In Rally

To view the test case ID, open your project in Rally, then go to **Quality > Test Cases**. Here you can see the list of test cases and their IDs.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/rally-integration/KS-RALLY-Test-case-ID-inRally.png" width="100%" alt="Test case ID in Rally">

### In Katalon Studio 

Open the test case you wish to link to Rally. Switch to the **Integration** tab, and specify the respective Test Case ID in Rally. For example:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/rally-integration/KS-Rally-Integration-tab.png" width="70%" alt="Map KS test case with Rally">

## Upload test execution results to Rally

To upload test execution results to Rally, do as follows:

1. Create a new test suite/test suite collection.
2. Add the mapped test cases to a test suite/test suite collection.
3. Execute the test suite/test suite collection.

The test suite/test suite collection results are uploaded to Rally accordingly.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/rally-integration/KS-RALLY-Test-results-uploaded-to-Rally.png" width="100%" alt="Map KS test case with Rally">

To view results in Rally, in the Rally dashboard, open the linked Rally test cases, switch to the **Results** tab.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/rally-integration/KS-RALLY-View-results-in-Rally.png" width="100%" alt="View results in Rally">




