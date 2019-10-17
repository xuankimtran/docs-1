---
title: "[Windows] Close Application"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/windows-kw-close-app.html
---
> > Starting from **version 7.0.0**, Windows desktop application testing is available on Katalon Studio.


## closeApplication

* **Description**: Trigger a closing event of the running application on the Windows System. This action is similar to pressing ALT + F4 and does not force the application to close. If there is a pop-up confirmation, you need to take some extra steps to actually close it.
* **Keyword name**: closeApplication
* **Keyword syntax**: Windows.closeApplication()
* **Example**:

``` groovy
"Start the note pad application"
Windows.startApplication('C:\\Windows\\System32\\notepad.exe')

"Close note pad application"
Windows.closeApplication()
```
