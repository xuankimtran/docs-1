---
title: "[WebUI] Smart Wait Function" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/webui-smartwait.html 
description: 
---
> Starting in **Katalon Studio version 7.0**, the Smart Wait function is available.

Currently, one of the most common problems that Katalon users may have encountered is that elements cannot be interacted with since they are neither visible nor interactable. This issue is because the page hasn't completely loaded or some previous actions including adding, removing, modifying elements of that page haven't finished executing. To solve this issue, a smart waiting function is launched in Katalon Studio version 7.0.

## Apply Smart Wait for the whole project

To enable the Smart Wait function for the whole project in Katalon Studio, navigate to **Project** > **Settings** > **Execution**> Select **Enable** in Default Smart Wait.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/webui-smartwait/smartwait.png" width="799" height="598">

## Use SmartWait Keywords in preferred test cases

If you want to use Smart Wait function in certain test cases only, it's important that you disable **Default Smart Wait** in Project Settings. Navigate to **Project** > **Settings** > **Execution**> Select **Disable** in Default Smart Wait. Then use `enableSmartWait` and `enableSmartWait` keywords to enable and disable this function respectively.

### enableSmartWait

**Description**: Enable the Smart Wait function when it's disabled by default in project settings.\
**Keyword name**: enableSmartWait.

### disableSmartWait

**Description**: Disable the Smart Wait function when it's enabled by using the above keyword.\
**Keyword name**: disableSmartWait.\
**Example**:

```groovy
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

> Note: The Smart Wait function is only available on Chrome and Firefox.
