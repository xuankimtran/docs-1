---
title: "Version 5.1.x"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/new/version-5102.html
redirect_from:
    - "/display/KD/Version+5.1.0.2/"
    - "/display/KD/Version%205.1.0.2/"
    - "/x/BB1O/"
    - "/katalon-studio/new/version-5102/"
    - "/katalon-studio/new/version-51.html"
    - "/display/KD/Version+5.1.0/"
    - "/display/KD/Version%205.1.0/"
    - "/x/zBtO/"
    - "/katalon-studio/new/version-510/"
description:
---

## Version 5.1.0.2

*   Fix an issue where desired capabilities are not working on Chrome.
*   Fix 'NullPointerException' error from mobile execution.
*   Fix an issue where '[Execute from here...](/display/KD/Execute+test+from+specific+step)' feature is disabled.
*   Fix an issue where 'Workbench auto-save job' message is displayed when users leave Katalon Studio in an idle state for a while.
*   Support Appium 1.7. Due to this change, '[Swipe](/display/KD/%5BMobile%5D+Swipe)' keyword has been adjusted:

    |   | Current | Changed |
    | --- | --- | --- |
    | Behavior | Swipe from (startx, startY) position to **extract** (endX,endY) position. | Swipe from (startX, startY) position to **relative position** of (startX, endY) position. |
    | Example | Swipe from (100,200) position to (200,300) position | Swipe from (100,200) position to (200,300) position => (endX,endY) position in this case will be (startX + 100, endX + 100) |
    | Script | Mobile.swipe(100, 200, 200, 300) | Mobile.swipe(100, 200, 100, 100) |

## Version 5.1.0

### Drivers Update

Katalon team has implemented the following changes in Katalon Studio Version 5.1.0

*   Selenium Driver 3.71
*   Gecko Driver for Firefox 0.19.0
*   IE Driver 3.6.0

With these upgrades, users will be able to smoothly execute automation scripts with Firefox version 57 or greater. 

**Project Settings**

### Email Attachment

Sharing Katalon Studio test execution report with team members just got easier. Email setting is enhanced in Version 5.1.0 to support **PDF** test execution **reports** as email **attachment**.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-510/image2017-11-14-153A423A45.png)

### Execution

Improved **Execution Settings** for users conveniences by combining settings in Katalon Studio Preferences and Project Settings

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-510/image2017-11-14-153A373A52.png)![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-510/image2017-11-14-153A383A8.png)