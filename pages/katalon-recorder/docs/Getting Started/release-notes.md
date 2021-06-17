---
title: "Release Notes"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-recorder/docs/release-notes.html
redirect_from:
  - "/display/KR/Release+Notes/"
  - "/display/KR/Release%20Notes/"
  - "/x/JwHR/"
  - "/katalon-recorder/docs/release-notes/"
description:
---

## 5.4.10
- Improved registration process.
  - Since version 5.4.10, new users will have unlimited test executions, but can create only one automation script. To create more, a **free account** is required. 
    - We have experimented with setting quota on the number of executions, but decided that it does not align with how users experience success with the product because the number of executions required to automate a scenario successfully vary greatly. However, when you want to automate more scenarios, it likely indicates that you have succeeded in automating one scenarios.

## 5.4.6
- Improved registration process.
  - Since version 5.4.6, new users will have to sign up for a **free** account after 4 successful executions. Our data has shown that users that have more than 4 successful executions are more likely to adopt the product.
- Fixed an issue where record and playback fails on Angular forms.
  - A bug prevented users from recording `sendKey` on Angular forms, which also makes playback fail.

## 5.4.5
- Improved registration process. 
  - We are constantly refining the registration process to offer users the best experience while balancing againt our business needs.
  - Since version 5.4.5, new users will be able to execute 25 tests without being forced or suggested to sign up. However, when the quota is exceeded, you will need a **free** account and log in to continue your work.

## 5.4
- Undo/redo mechanism to recover from mistakes while editing tests.
- New Product Tours for both new and current KR users.
- Improved registration process.

## 5.3.30 - latest release

**New feature**
- [Daily Usage](https://docs.katalon.com/katalon-recorder/docs/daily-usage.html).

**Bug fixes**
- Fixed an error where sign-up dialog prevents people from using KR

## 5.1.0

- Add some `waitFor` contextual menu actions (@anthonybriand).
- Support more commands for Protractor exporter (@anthonybriand).

## 5.0.0

- Now all data such as Test Cases, Test Data, Extension Scripts, etc. can be automatically backed up.

## 4.1.0

- Added relative=top and relative=up to selectFrame (@svrnm).

## 4.0.0

- Added dark-theme (by @pgroot91).

## 3.9.x

- Enhanced the Robot Framework formatter (by @reyelts).
- Fixed an issue where test suite file is malformed (by @UpUpDwnDwnLftRt).
- Allowed to use variables in command names (by @zoldike-gh).
- Added "Close All Test Suites" feature (by @UpUpDwnDwnLftRt).
- Used the extension `.html` for saved files (by @olenitsj).

## 3.8.x

- Added the Protractor formatter (TypeScript) (by @MilesLin).

## 3.7.x

- Added the New Relic Synthetics formatter (JavaScript) (by @tanben).

## 3.6.x

- Enhanced the underlying automation engine and the integration with Katalon Studio.

## 3.5.7

- Supported "loadVars" for JSON-format data files.
- Supported custom order for locator builders.
- Supported "Play From Here" to execute a test suite from an arbitrary test case.

## 3.5.0 - 3.5.6

- Supported [extension scripts (AKA user-extensions.js)](/display/KR/Extension+Scripts+%28AKA+user-extensions.js%29+for+Custom+Locator+Builders+and+Actions).

## 3.4.12

- Fixed a bug with "chooseOkOnNextConfirmation".
- Fixed a bug where KR crashes when processing values with patterns like "${variable" (missing the closing "}").

## 3.4.11

- Supported storing returned values from "runScript" commands.
- Fixed various bugs of "store" and "storeEval" commands.
- Supported parameters in selectFrame, selectWindow commands.
- Show variable types in the tab "Variables".
- Added command "#" for writing comments.
- Added command "storeCsv" for loading values from CSV data files.

## 3.4.10

- Command names are now case-insensitive.
- On Chrome, "sendKeys" and "type" (for file inputs) can now be used with all types of locators. The old versions required CSS locators.

## 3.4.7 - 3.4.9

- Supported dragAndDropToObjectByJqueryUI for testing drag-and-drop functions built with jQuery UI.
- Supported gotoIf, gotoLabel, and label for jumping to steps inside test cases.
- Supported capturing screenshots upon failures.
- Supported sendKeys for special keys (e.g. ENTER) on Chrome.
- Fixed an issue with pause command.
- Provided more details in logs for easier debugging.
- Supported storedVars.key (or storedVars\['key'\]) syntax in storeEval command.
- Supported "Play From Here" (context menu) for playing test case from an arbitrary test step.

## 3.4.0 - 3.4.6

- Supported plugins for export recorded Test Cases to other formats.
- Fixed bugs.

## 3.3.2

- Supported file uploading.

## 3.3.0

- Improved performance.
- Added XML formatter.
- Supported loading variables from CSV file.
- Added if...elseIf..else..endIf statements.
- Added while..endWhile statements.

## 3.2.0 - 3.2.2

- Supported screenshot capturing.
- Allowed sharing variables across test cases.

## 3.1.0 - 3.1.2

- Improved logging: Start Time, End Time, Browser, OS.
- Supported uploading logs to Katalon Analytics (Beta).

## 3.0.3 - 3.0.4

- Supported exporting to C# and MSTest framework.
- Fixed bugs

## 3.0.0 - 3.0.2

- Added new features: Play Suite, Play All, Speed Configuration, Pause, Resume.
- Supported debugging: Pause, Resume, Breakpoints, Variables View.
- Improved logging: Save, Clear.
- Improved Test Cases authoring: Copy, Paste.

## 2.2.0

- Added support for offline mode in Chrome.
- Added support for Glob & Regex patterns in Assert & Verify commands.
- Added confirmation before deleting all test steps.

## 2.1.0

- Added support for CSS locators.
- Added support for runScript & storeEval commands.
- Fixed a bug in store… functions.
- Fixed a bug in string interpolation.

## 2.0.0 - 2.0.9

- First releases with Selenium IDE-based features: Record, Play, Selenese, Export to other programming languages and frameworks.
- Fixed bugs.
