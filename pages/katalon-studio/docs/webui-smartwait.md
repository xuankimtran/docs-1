---
title: "[WebUI] Smart Wait Function" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/webui-smartwait.html 
description: 
---

One of the most common problems is that Katalon users cannot interact with web page elements, which causes automation tests to fail. Some elements are neither visible nor interactable; the other would receive the operations instead of the intended ones. This issue is because the page hasn't fully loaded or some operations (adding, removing, or modifying elements) haven't finished performing yet.

As a solution, Smart Wait is introduced in Katalon Studio version 7.0. It tells the web driver to wait for the web page to become static before any operations perform.

> **Notes**:
>
> * Your Katalon Studio version must be 7.0 or later.
> * The Smart Wait function is only available on Chrome and Firefox.

## Sample Tests

[Sample tests](https://github.com/katalon-studio-samples/smart-wait-example-tests) are available for your download.

## Apply to all elements in a project

Smart Wait is enabled by default in **Project/Settings/Execution**. This default configuration will download the Smart Wait extension automatically and apply Smart Wait to all elements in that project.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/webui-smartwait/smartwait.png" width="799" height="598">

## Temporarily turn off Smart Wait

You can use the `disableSmartWait` keyword in a script to turn off Smart Wait temporarily.

If you want to apply Smart Wait to specific elements in a script, make sure that you did NOT change the enabled **Default Smart Wait**. Since Katalon Studio only installs the Smart Wait extension when it's enabled in Project Settings. Then you need to use `disableSmartWait` to disable it on project scale. Next, use `enableSmartWait` and `disableSmartWait` keywords to apply this function to your target elements.

**Example**:

```groovy
WebUI.disableSmartWait()

WebUI.openBrowser('')

WebUI.navigateToUrl('https://store.katalon.com/')

WebUI.maximizeWindow()

WebUI.click(findTestObject('signin-link'))

WebUI.enableSmartWait()

WebUI.setText(findTestObject('username'), 'demo@katalon.com')

WebUI.setEncryptedText(findTestObject('password'),'3zBGMH+v8QQXwX1AbEAx2g==')

WebUI.click(findTestObject('signin-button'))

WebUI.click(findTestObject('menu-dropdown'))

WebUI.click(findTestObject('dashboard-item'))

WebUI.click(findTestObject('plugins-item'))

WebUI.disableSmartWait()

WebUI.closeBrowser()
```
