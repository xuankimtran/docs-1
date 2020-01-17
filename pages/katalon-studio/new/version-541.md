---
title: "Version 5.4.x"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/new/version-541.html
redirect_from:
    - "/display/KD/Version+5.4.1/"
    - "/display/KD/Version%205.4.1/"
    - "/x/6QPR/"
    - "/katalon-studio/new/version-541/"
    - "/katalon-studio/new/version-540.html"
    - "/display/KD/Version+5.4.0/"
    - "/display/KD/Version%205.4.0/"
    - "/x/lQHR/"
    - "/katalon-studio/new/version-540/"
description:
---

## Version 5.4.1

### Fixes bugs

*   Fix an issue where Tests Explorer is not displayed when restoring last working session.
*   Fix some issues regarding Test Suite Collection HTML report.
*   Fix an issue where email report can't be sent to recipients.
*   Correct browser's information in Test Suite HTML report when Microsoft Edge is used for execution.
*   Fix an issue where the executed browser is closed upon executing a test case.
*   Fix migration issue of where HTTP Body with POST method is not transferred when opening project with version 5.4.
*   Fix an issue of cannot send API Request due to NullPointerExeception using specific Request URL.
*   Modify setHttPBody & getHttpBody deprecated methods to function properly in version 5.4.
*   Fix issues where Execution Profile/Global Variables does not work properly in Test Case Variables.

## Version 5.4.0

Katalon Studio version 5.4 has finally arrived! introducing all-new UI and features to fully support API testing in conjunction with the Functional automation component.

New features & improvements of Katalon Studio 5.4:

### New API Testing

Fully support **SOAP** and **REST API** automation, the enhanced API component empowers automation engineer to combine, manipulate and validate the functional scenario test cases easily and effectively by using the same IDE interface.

Katalon Studio users will have more capabilities to improve the API automation activities includes **Query Parameters** for **REST** request URL, support various **HTTP Body** message types and common information for **HTTP Header**, display more details in **Response** such as **Status**, **Elapsed** time, and package **Size**, and more.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-540/image2018-4-9-173A13A52.png)

### Sensitive Text Encryption

Privacy and Security are crucial than ever to the software industry. **Text encryption** feature is introduced via the built-in "**[setEncryptedText](/x/6AHR)**" keyword. It allows users to encrypt any sensitive text right in the test case and capable to decrypt on-the-fly at runtime. Thus, the project team can collaborate and share test artifacts among members and stakeholder without any security concerns.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-540/image2018-4-9-163A423A34.png)

### Execution Profile

> **Global Variables** interface is moved to be a **default profile,** so please check **'default' profile** for any existing **Global Variables** 

Test execution is more versatile in Katalon Studio v5.4. Automation tests can be executed dynamically by configurable **profiles**, defined by a combination of multiple attributes (environments, test data, platforms). **Execution profiles** enable Functional and API test execution integrated into the CI pipeline regardless of the test requirement complexity to meet the rapid demand of Agile software project.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-540/image2018-4-9-163A433A45.png)

### Templates for Custom Keywords

Adding the options to generate sample template when users create new custom keywords, the output can be selected as web, mobile or API custom keyword.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-540/image2018-4-9-173A153A40.png)

### Auto-update

Katalon Studio will deliver the newest version directly while letting users continue to work uninterrupted. The update process is configurable with options of **Download** Now, **Remind Me Later**, or **Ignore** **This Update**. 

### Enhancements

*   Captured images in execution reports can be viewed in "**Fit to view**" or "**Full-size**".