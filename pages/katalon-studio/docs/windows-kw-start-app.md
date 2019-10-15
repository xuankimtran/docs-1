---
title: "[Windows] Start Application"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/windows-kw-start-app.html
---
> Starting from **version 7.0.0**, Windows desktop application testing is available on Katalon Studio.

## startApplication

* **Description**: Start the Windows driver and the Windows application with the given absolute path.
* **Keyword name**: startApplication
* **Keyword syntax**: Windows.startApplication(appFile)
* **Parameter**: appFile
  * Description: The absolute path to the Windows Executable File (*.exe) of the test machine.
  * Parameter Type: String
  * Mandatory: Required
* **Example**:

``` groovy
"Start the note pad application"
Windows.startApplication('C:\\Windows\\System32\\notepad.exe')
```
