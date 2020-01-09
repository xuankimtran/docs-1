---
title: "Katalon Studio Preferences" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/katalon-studio-preferences.html 
redirect_from:
    - "/display/KD/Katalon+Studio+Preferences/"
    - "/display/KD/Katalon%20Studio%20Preferences/"
    - "/x/NQRO/"
    - "/katalon-studio/docs/katalon-studio-preferences/"
description: 
---

Katalon Studio Preferences define default behaviors of Katalon Studio across projects. You can access the Preferences by selecting **Katalon Studio > Preferences** from the menu.

Starting from Katalon Studio version 7.0.0, you can configure the usage tracked by Katalon Studio. Go to **Katalon Studio > Preferences> Katalon** from the menu. By default, Katalon Studio is allowed to collect error and execution logs, and other information about your use of the application. Refer to the [Privacy Policy](https://www.katalon.com/terms/katalon/privacy-policy/) for further details of our tracking.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/katalon-studio-preferences/preferences.png" width="610" height="304">

For more details, please refer to the following articles:

## Test Case Preferences

All the preferences under the **Test Case** group are for controlling the default behaviors that Katalon Studio should perform when test cases are designed.

You can configure the Test Case preferences via **Katalon Studio > Preferences > Katalon > Test Case**.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-case-preferences/Window.png)

### Test Case Calling

This is to specify how Katalon Studio should behave when you are calling another test case in your current one.

* **Generate variable with default value**: Called test case uses default values for its variables.
* **Generate variable with the same name as the exposed variable of the called test case**: Called test case uses default values which are the same with its variables name.
  * **Expose variables automatically after choosing the called test case**: Called test case uses default values which are the same with its variables name. The variables are also added to the current test case at the 'Variables' tab.

You might need to refer back to the [Variable Types](/display/KD/Variable+Types) section for which types of variables are supported in Katalon Studio.

### Initially open Test Case

This is to indicate in which view Katalon Studio should display a test case when it is first opened.

* **In Manual View**: The opened test case will be first in the manual view.
* **In Script View**: The opened test case will be first in the script view.

### Default Keyword Type

* **Default Keyword**: These default keywords will be available when a new step is added to your test case.

### Line-wrapping Settings

This is to enable Katalon Studio to wrap up the code lines in a script with a customized maximum line width. You can also wrap the code lines when switching from the manual mode to the script mode by pressing a keyboard combination of **Command+Shift+F** (Mac Users) or **Ctrl+Shift+F** (Windows and Linux Users).

Before the line-wrapping enabled:

![Before](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-case-preferences/wrap.png)

After the line-wrapping enabled:

![After](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-case-preferences/wrapped.png)

> All the above preferences are saved into the  `com.kms.katalon.composer.testcase.prefs` file under the "**config\\.metadata\\.plugins\\org.eclipse.core.runtime\\.settings**" location in your Katalon Studio build folder. You can manually modify the values in this file to change these preference settings.

## Proxy Preferences

Proxy can be configured at: **Katalon Studio> Preferences > Katalon > Proxy**. This setting affects both WebUI and WebService testings.

In the Proxy Settings, you can select one of three options below.

* **No proxy**: there's no proxy.

* **Use system proxy configuration**: Katalon Studio guesses which proxy server your system is behind by checking Java, browser and operating system settings, and environment variables.

  > Notes: Proxy auto-config (PAC) file is supported in version 7.1 and later. You need to select **Use system proxy configuration** to utilize a PAC file.
  
* **Manual proxy configuration**: you can manually set up your proxy.
  * Address: a HTTP Proxy host.
  * Port: a HTTP Proxy port.
  * Excludes: A list of addresses separated by comma to exclude. 
  > The ability to exclude proxy is available in version 7.2 and later. Katalon Studio only supports proxy exceptions in web recorder and spying with **Chrome** and **Firefox**.
  
  <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/proxy-preferences/proxy-manual.png" width="663.5" height="">

> If you're behind a Proxy Server, you'll need to configure the proxy settings before activating Katalon Studio. Click **Config Proxy** at the bottom of the Activation dialog box.

### Override proxy details in the test script

Starting from **version 7.0.0**, Katalon Studio supports an option to pass proxy details via a request object in Web Service testing. Below is an example:

```groovy
RequestObject requestObject = findTestObject("google")
ProxyInformation proxyInfo = new ProxyInformation();
proxyInfo.setProxyServerAddress("localhost")
proxyInfo.setProxyServerPort(8001)
proxyInfo.setProxyOption(ProxyOption.MANUAL_CONFIG.toString())
proxyInfo.setProxyServerType(ProxyServerType.HTTP.toString())
requestObject.setProxy(proxyInfo)
```

>**Note**: The proxy information passed in the request object takes precedence over the proxy information set in **Preferences**.

## Object Spy Preferences

You can access this preferences at **Window > Katalon Studio Preferences > Katalon > Object Spy.**

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/object-spy-preferences/image2017-11-27-113A43A34.png)

### Pin Object Spy Window while spying

Users can check/uncheck this option to pin Object Spy Window on top while spying for more convenience.

### Hotkeys

Katalon Studio supports customizable hotkeys for Object Spy function so that users can choose the preferred combination or avoid confliction with UAT hotkeys. 

> This ability to change hotkeys for Object Spy only affect Chrome browser. Other browsers will be considered for future releases.

## Using Katalon Studio in Dark theme

By default, Katalon Studio has the Light theme applied. Starting in version 6.3.0, Dark Theme is available.

To enable it, from __Window__, select __Themes__, then select __Dark__.


![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/dark-theme/1-darktheme.png)

Katalon Studio is required restarting to enable another theme to be applied.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/dark-theme/2-darktheme.png)

