---
title: "Test Case Preferences"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/test-case-preferences.html
redirect_from:
    - "/display/KD/Test+Case+Preferences/"
    - "/display/KD/Test%20Case%20Preferences/"
    - "/x/ZIUw/"
    - "/katalon-studio/docs/test-case-preferences/"
description:
---
All the preferences under the **Test Case** group are for controlling the default behaviors that Katalon Studio should perform when test cases are designed.

You can configure the Test Case preferences via **Katalon Studio > Preferences > Katalon > Test Case**.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-case-preferences/Window.png)

## Test Case Calling

This is to specify how Katalon Studio should behave when you are calling another test case in your current one.

* **Generate variable with default value**: Called test case uses default values for its variables.
* **Generate variable with the same name as the exposed variable of the called test case**: Called test case uses default values which are the same with its variables name.
  * **Expose variables automatically after choosing the called test case**: Called test case uses default values which are the same with its variables name. The variables are also added to the current test case at the 'Variables' tab.

You might need to refer back to the [Variable Types](/display/KD/Variable+Types) section for which types of variables are supported in Katalon Studio.

## Initially open Test Case

This is to indicate in which view Katalon Studio should display a test case when it is first opened.

* **In Manual View**: The opened test case will be first in the manual view.
* **In Script View**: The opened test case will be first in the script view.

## Default Keyword Type

* **Default Keyword**: These default keywords will be available when a new step is added to your test case.

## Line-wrapping Settings

This is to enable Katalon Studio to wrap up the code lines in a script with a customized maximum line width. You can also wrap the code lines when switching from the manual mode to the script mode by pressing a keyboard combination of **Command+Shift+F** (Mac Users) or **Ctrl+Shift+F** (Windows and Linux Users).

Before the line-wrapping enabled:

![Before](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-case-preferences/wrap.png)

After the line-wrapping enabled:

![After](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-case-preferences/wrapped.png)

> All the above preferences are saved into the  `com.kms.katalon.composer.testcase.prefs` file under the "**config\\.metadata\\.plugins\\org.eclipse.core.runtime\\.settings**" location in your Katalon Studio build folder. You can manually modify the values in this file to change these preference settings.
