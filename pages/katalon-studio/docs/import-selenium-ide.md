---
title: "Import Selenium IDE version 3 projects"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/import-selenium-ide.html
---

In addition to importing Selenium/TestNG/JUnit projects into Katalon Studio, from version 7.5.10 onwards, you can also import a Selenium IDE project for execution with Katalon Studio.

Selenium IDE is an integrated development environment for Selenium tests. It is implemented as a Chrome add-on and Firefox extension, which allows users to record, edit, and debug tests. Katalon Studio supports Selenium IDE project version 3.x onwards. 

This tutorial shows you how to import a Selenium IDE project to a project in Katalon Studio and how Katalon Studio maps the imported test artifacts. Also, a sample Selenium IDE project is provided for you to try out our newly supported feature.

> Requirements:
> * Katalon Studio version 7.5.10 onwards

> You can download our Github sample project for importing a Selenium IDE project to Katalon Studio: [Import Selenium IDE sample](https://github.com/katalon-studio-samples/import-selenium-ide-sample).
## Import a Selenium IDE project

In Katalon Studio:

1. Create or open a project
2. From the menu bar, select **File > Import Selenium IDE Project** and browse your Selenium IDE file (a single file with a `.side` extension) to open. 

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/import-selenium-ide/selenium-ide.png" width=763 alt="Import Selenium IDE">

## Map Selenium IDE with Katalon Studio test artifacts

A Selenium IDE project contains Tests, Suites, and Executing. Katalon Studio only imports Tests and Suites.

### Selenium IDE Suites - Katalon Studio Test Suites

Under the **Test Suites** folder in **Tests Explorer**, Katalon Studio creates an **Imported from Selenium IDE Scripts** folder to store the imported suites. Once the import process is done, Katalon Studio open the test suites automatically.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/import-selenium-ide/test-suites.png">

> Notes:
> * If your Katalon project already has an **Imported from Selenium IDE Scripts** folder under the **Test Suites** folder, the new folder should be **Imported from Selenium IDE Scripts (1)**.
> * If there is no suite in the imported Selenium IDE project, Katalon Studio does not create an **Imported from Selenium IDE Scripts** folder under the **Test Suites** folder.

### Selenium IDE Tests - Katalon Studio Test Cases

Under the **Test Cases** folder in **Tests Explorer**, Katalon Studio creates an **Imported from Selenium IDE Scripts/&lt;suite name&gt;** folder to store the imported tests.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/import-selenium-ide/test-cases.png">

An imported test case contains a set of Selenium commands recorded by Selenium IDE.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/import-selenium-ide/test.png">

> Notes:
> * Supported element locators include `identifier`, `id`, `name`, `dom`, `xpath`, `link`, `css`, and `ui`. To learn more about Selenlium locators, you can refer to the Selenium Java document here: [Selenium Java document](https://www.selenium.dev/selenium/docs/api/java/org/openqa/selenium/support/locators/package-summary.html).

## See also

* [Selenium/TestNG/JUnit Migration to Katalon Studio](https://docs.katalon.com/katalon-studio/docs/selenium-testng-junit-migration.html)
