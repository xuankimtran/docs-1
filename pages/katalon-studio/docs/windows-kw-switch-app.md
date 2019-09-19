---
title: "[Windows] Switch To Application"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/windows-kw-switch-app.html
---
> Starting from **Katalon Studio version 7.0.0**, Katalon Studio Enterprise users can run a test on a Windows desktop application.

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
