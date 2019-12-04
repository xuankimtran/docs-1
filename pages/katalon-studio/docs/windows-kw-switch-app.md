---
title: "[Windows] Switch To Application"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/windows-kw-switch-app.html
---
> Starting from **version 7.0.0**, Windows desktop application testing is available on Katalon Studio.

## switchToApplication

* **Description**: Switch from the current running driver to the application Windows Driver.
* **Keyword name**: switchToApplication
* **Keyword syntax**: Windows.switchToApplication()
* **Example**:

``` groovy
"Start the note pad application"
Windows.startApplication('C:\\Windows\\System32\\notepad.exe')

"Switch to control the desktop"
Windows.switchToDesktop()

// Do some stuffs with the desktop

"Switch back to control the note pad application"
Windows.switchToApplication()
```
