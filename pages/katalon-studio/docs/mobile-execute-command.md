---
title: "[Mobile] Execute Mobile Command "
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/mobile-execute-command.html
---
> Starting from **version 7.2**, this keyword is available for Mobile testing on Katalon Studio.

## executeMobileCommand

* **Description**: Execute a native mobile command.
* **Keyword syntax**: Mobile.executeMobileCommand(command, args, flowControl)
* **Parameters**:
  * Name: command
    * Description: Mobile command name.
    * Parameter Type: String
    * Mandatory: Required
  * Name: args
    * Description: The provided arguments for which the command is required.
    * Parameter Type: Map
    * Mandatory: Required
  * Name: flowControl
    * Description: Used to control the step if the step failed.
    * Parameter Type: FailureHandling
    * Mandatory: optional
* **Returns**: the command's result with the *Object* type.
* **Throw**: **StepFailedException** if Katalon Studio could not find the specified element.
* **Example**:

  ``` groovy
  import com.google.common.collect.ImmutableMap as ImmutableMap;

  Mobile.startApplication('C:\\Users\\katalon\\Sample Apps\\APIDemos.apk', 
    true)

  String command = "mobile:changePermissions"
  Map args = ImmutableMap.of(
      "action", "grant",
      "appPackage","com.hmh.api",
      "permissions", "android.permission.READ_CONTACTS")
  Object result = Mobile.executeMobileCommand(command, args)

  print result

  Mobile.closeApplication()
  ```
