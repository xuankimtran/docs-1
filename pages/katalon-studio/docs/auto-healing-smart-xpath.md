---
title: "Auto-healing Smart XPath" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/auto-healing-smart-xpath.html
description:
---

From version 7.6.0, Katalon Studio launches Self-healing to replace Auto-healing Smart XPath for Web test execution. See [Self-healing](https://docs.katalon.com/katalon-studio/docs/self-healing.html).

This documentation is for the Katalon Studio version before 7.6.0.

> Download the latest version of Katalon Studio: [Katalon Studio](https://www.katalon.com/download/).

<details><summary>Auto-healing Smart XPath Plugin for Katalon Studio version before 7.6.0</summary>

## Install Auto-healing Smart XPath plugin

1. Go to Katalon Store and download the plugin: [Auto-healing Smart XPath](https://store.katalon.com/product/5/Auto-healing-Smart-XPath).
2. After successfully installing the plugin, open Katalon Studio. Click on the dropdown icon of the *Profile* button and choose **Reload Plugins**. To learn more about plugin installation, see [Reload plugins](https://docs.katalon.com/katalon-store/docs/user/access-store-in-KS.html#reload-plugins).
3. In the main toolbar, click on the **Auto-healing Smart XPath** button. If you see the **Smart XPath Disable**, the **Auto-healing Smart XPath** is currently enabled.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/auto-healing-smart-xpath/xpath_03.png" alt="enable smart xpath" width="70%">

## Configure XPath

Go to **Project Settings** > **Test Design** > **Web Locators**. Choose the **XPath** option.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/auto-healing-smart-xpath/xpath_01.png" alt="choose XPath" width=100%>

The list contains XPath generator providers which generate the corresponding XPath values for Katalon Studio test objects. You can drag and drop to change Xpath priority.

Learn more about XPath locators at this documentation: [Web Selection Method: Configure XPath](https://docs.katalon.com/katalon-studio/docs/web-selection-methods.html#configure-xpath).

## Create test objects by Recording/Spying

Once test objects in test cases are created by the Recording or Spying feature in Katalon Studio, a set of XPath values are generated in the prioritized order of the XPath generator provider list. The first value in the list is the default XPath value of the test objects.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/auto-healing-smart-xpath/xpath-update-1.png" alt="object view" width="100%"> 

## Execute test cases with Auto Healing, supported by Smart XPath

During execution, if a default XPath value fails to detect a test object, other XPath options in the list are automatically applied until successfully find the test object. The execution continues as if no failed detection has happened. This helps significantly save time updating test cases, especially when the test cases are executed in batch overnight.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/auto-healing-smart-xpath/xpath-update-2.png" alt="log viewer" width=100%>

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/auto-healing-smart-xpath/xpath-update-3.png" atl="event log" width=100%>

## Update to the new stable XPath values

After execution, you can update the proposed XPath values to the test objects. Go to **Smart Xpath > Xpath Auto-healing logs**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/auto-healing-smart-xpath/xpath-update-4.png" alt="xpath auto-healing logs" width=100%>

Check the **Approve** box, then click OK to update the value. If you wish to update all values, click **Approve all**. 

After approval, close the object and refresh the Object Repository to see the updated XPath values.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/auto-healing-smart-xpath/xpath-update-5.png" alt="updated xpath values" width=100%>

</details>
