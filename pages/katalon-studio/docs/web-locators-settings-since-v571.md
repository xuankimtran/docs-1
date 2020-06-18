---
title: "Web Locators Settings" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/web-locators-settings-since-v571.html
redirect_from:
    - "/x/MwDR/"
    - "/katalon-studio/docs/web-locators-settings-since-v571/"
    - "/katalon-studio/docs/web-locators-settings-since-57.html"
    - "/display/KD/Web+Locators+Settings"
    - "/katalon-studio/docs/web-locators-settings.html"
---
From version 7.6, Katalon Studio launches [Self-healing Tests](https://docs.katalon.com/katalon-studio/docs/self-healing.html) that includes settings for default web locators during spying, recording and execution.

<details><summary>In versions <strong>before 7.6</strong>, see Web Locators Settings</summary>

Katalon Studio allows setting default Web Locator in **Project Setting > Test Design > Web Locators**.

This setting helps eliminate the repetitive tasks of selecting/deselecting locators for each captured objects while recording or spying the AUT. The locators in this setting will be applied to all captured objects in [Record](/display/KD/Record+Web+Utility) and [Spy](/display/KD/Spy+Web+Utility) Web.

> Requirement: You need to have an active Katalon Studio Enterprise License.

## Web Locators Settings

### Relative XPath

> * By default any _New Projects_ created will use the **XPath** option
> * XPath option does not apply to Internet Explorer. Internet Explorer will always use Attributes option.
> * The web locator _Selection Method_ also carries over to Record Web Utility, Spy Web Utility, and Test Object View.

Katalon Studio supports _Relative XPath_ for better object recognition. If an element cannot be consistently located using its direct attributes, Katalon Studio will identify by using its more robust neighbors. That is a simple but powerful idea behind the _New_ locator method introduced in Katalon Studio. This method is visually intuitive as it reflects the way users often identify a visible element on the user interface.

**Key features**

* Locates Web elements by clustering visualization.
* Preserves the relationship between an element and its indicator in an item. 
* Generates reliable locators to reduce test script maintenance cost.

_Drag and drop_ any XPath on the list to change its priority. Katalon Studio will use the first XPath as _default_ to locate the elements, and the rest of the list will be leveraged to locate the element if the first one failed.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/web-locators-settings-since-v571/image2018-8-13-163A433A2.png)

Captured objects will have properties listed as below:

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/web-locators-settings-since-v571/image2018-8-14-17_30_17.png)

### Element Attributes

Katalon Studio also supports the regular XPath with locator strategies available in Selenium. Custom locators can be added to the list as well. Pre-selected locators are those recommended by the Katalon team.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/web-locators-settings-since-v571/image2018-8-13-163A433A31.png)

**Example:**

1. By default, **tag** property will be selected. In some cases you don't want this behavior so that you can change this by:

   Add a new property called **tag** and deselect it:
   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/web-locators-settings-since-v571/image2018-1-26-143A213A20.png)

   When you spy or record test steps, any object having this **tag** property will **not** be used by default.
   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/web-locators-settings-since-v571/image2018-1-26-143A153A27.png)

2. Working with Angular pages, there are two properties called **ng-model** and **ng-pattern** you would like to use it by default. Added these two properties to the list of current Web Locators.
   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/web-locators-settings-since-v571/Screen-Shot-2018-01-26-at-13.58.22.png)
  
   These selected properties will be checked by default when you Spy or Record your test steps:
   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/web-locators-settings-since-v571/image2018-1-26-143A133A3.png)
</details>