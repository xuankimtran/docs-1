---
title: "Web Locators Settings (version 5.7.1-7.6.0)" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/web-locators-settings-since-v571.html
redirect_from:
    - "/x/MwDR/"
    - "/katalon-studio/docs/web-locators-settings-since-v571/"
    - "/katalon-studio/docs/web-locators-settings-since-57.html"
    - "/display/KD/Web+Locators+Settings"
    - "/katalon-studio/docs/web-locators-settings.html"
---

This documentation is for Katalon Studio version 5.7.1 to 7.6.0. If you are using Katalon Studio version 7.6.0 onwards, refer to this documentation: [Selection Methods for Web Tests](https://docs.katalon.com/katalon-studio/docs/web-selection-methods.html).

> Download the latest version of Katalon Studio: [Katalon Studio](https://www.katalon.com/download).

<details><summary>Web Locators Settings for Katalon Studio version 5.7.1-7.6.0</summary>

You can set the default Web Locator in **Project Setting > Test Design > Web Locators**.

While recording or spying the app under test (AUT), the **Web Locator** settings helps eliminate the repetitive tasks of selecting/deselecting locators for each captured object. The locators in this setting apply to all captured objects in [Record](/display/KD/Record+Web+Utility) and [Spy](/display/KD/Spy+Web+Utility) Web.

> Requirements:
>
> * An active Katalon Studio Enterprise License.

## Web Locators Settings

### Relative XPath

> Notes:
>
> * By default, any _New Projects_ created use the **XPath** option.
> * The XPath option does not apply to Internet Explorer. Internet Explorer always uses the Attributes option.
> * The web locator _Selection Method_ also carries over to Record Web Utility, Spy Web Utility, and Test Object View.

For better object recognition, Katalon Studio supports relative XPath. If an element cannot be consistently located using its direct attributes, Katalon Studio identifies that element by using its more robust neighbors. This method is visually intuitive as it reflects the way users often identify a visible element on the user interface.

With **Web Locator**, you can:

* Locate Web elements by clustering visualization.
* Preserve the relationship between an element and its indicator in an item.
* Generate reliable locators to reduce test script maintenance costs.

You can prioritize XPaths by dragging and dropping any XPath on the list. Katalon Studio uses the first XPath as default to locate the elements. If the first one fails, the rest XPaths of the list are leveraged to locate the element.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/web-locators-settings-since-v571/image2018-8-13-163A433A2.png" alt="web locator" width="100%">

Captured objects have properties listed as below:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/web-locators-settings-since-v571/image2018-8-14-17_30_17.png" alt="capture object" width="100%">

### Element Attributes

Katalon Studio supports the regular XPath with locator strategies. You can also add custom locators to the list. Pre-selected locators are recommended by the Katalon team.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/web-locators-settings-since-v571/image2018-8-13-163A433A31.png" alt="attributes" width="100%">

**Example:**

1. By default, the **tag** property is selected. If you do not want this behavior, you can deselect the **tag** property from the list.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/web-locators-settings-since-v571/image2018-1-26-143A213A20.png" alt="tag" width="100%">

   When you spy or record test steps, any object having this **tag** property is not used by default.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/web-locators-settings-since-v571/image2018-1-26-143A153A27.png" alt="captured object" width="70%">

2. Working with Angular pages, you might want to use **ng-model** and **ng-pattern** properties by default. Add these properties to the list.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/web-locators-settings-since-v571/Screen-Shot-2018-01-26-at-13.58.22.png" alt="properties" width="100%">
  
   These selected properties are checked by default when you Spy or Record your test steps:
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/web-locators-settings-since-v571/image2018-1-26-143A133A3.png" alt="object spy" width="70%">
</details>