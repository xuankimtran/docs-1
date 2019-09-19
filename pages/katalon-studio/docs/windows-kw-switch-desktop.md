---
title: "[Windows] Switch To Desktop"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/windows-kw-switch-desktop.html
---
> Starting from **Katalon Studio version 7.0.0**, Katalon Studio Enterprise users can run a test on a Windows desktop application.

## switchToDesktop

* **Description**: Switch from the current running driver to a desktop session of the Windows Driver. This keyword initializes another Windows Driver with the `app: Root` (the whole desktop) desired capability and the same WinAppDriver URL and Proxy settings of the application driver. All of Windows built-in keywords now are manipulated by the desktop Windows Driver.
* **Keyword name**: switchToDesktop
* **Keyword syntax**: Windows.switchToDesktop()
* **Example**:

``` groovy
"Start the note pad application"
Windows.startApplication('C:\\Windows\\System32\\notepad.exe')

"Switch to control the Desktop"
Windows.switchToDesktop()
```
