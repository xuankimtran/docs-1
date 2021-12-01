---
title: "Proxy Preferences" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/proxy-preferences.html 
redirect_from:
description: 
---

From Katalon Studio version 7.5.0 onwards, the proxy is divided into two categories: Authentication and System proxies. You can apply different proxy configurations for connecting to the Katalon server and your servers during testing.

Please go to **Katalon Studio> Preferences > Katalon > Proxy** and select **Authentication** or **System** section for corresponding proxy configuration of each type.

### Authentication Proxy

The proxy configurations in this section are used for all network connections to authenticate with Katalon Servers including Katalon account authentication, Katalon Auto-updater, Katalon TestOps, and  Katalon Store integration, sample projects provider, AMI Authentication, and etc.)

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/proxy-preferences/auth-proxy.png" width="70%" alt="Authentication proxy">

### System Proxy

System proxy configurations are applied to all network connections generated when using Katalon Studio, including but not limited to recording, spying, executing tests, integrating with other tools, and downloading Web Drivers or Android SDK.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/proxy-preferences/proxy-system.png" width="70%" alt="System proxy">

### Proxy Settings

In the Proxy Settings areas of both Authentication and System proxies, you can select one of three options below.

* **No proxy**: there's no proxy.
* **Use system proxy configuration**: Katalon Studio guesses which proxy server your system is behind by checking Java, browser and operating system settings, and environment variables.
* **Manual proxy configuration**: you can manually set up your proxy
  * Address: an HTTP Proxy host
  * Port: an HTTP Proxy port
  * Excludes: A list of addresses separated by comma to exclude
  > The ability to exclude proxy is available from version 7.2.0 onwards. Katalon Studio only supports proxy exceptions in web recorder and spying with **Chrome** and **Firefox**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/proxy-preferences/proxy-options.png" width="70%" alt="proxy settings">

### System proxy for test execution's desired capabilities

Katalon Studio applies the System proxy to test execution's desired capabilities on the instance automatically. If you wish to configure different proxy's desired capabilities for a project, you need to do as follows:

1. Open your project and go to **Katalon Studio/Preferences/Katalon/Proxy/System**
2. At the bottom of the displayed view, uncheck the **Auto-apply to test execution desired capabilities** option and click **OK** to save
   
  <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/proxy-preferences/uncheck.png" width="70%" alt="uncheck proxy for desired capabilities">

3. Go to **Project/Settings/Desired Capabilities** and select a testing environment

4. Specify proxy details and click **OK** to save

   For example:

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/proxy-preferences/desired-capabilities.png" width="70%" alt="use proxy for desired capabilities">

### Override proxy details in the test script

From version 7.0.0 onwards, Katalon Studio supports an option to pass proxy details via a request object in Web Service testing. Below is an example:

```groovy
RequestObject requestObject = findTestObject("google")
ProxyInformation proxyInfo = new ProxyInformation();
proxyInfo.setProxyServerAddress("localhost")
proxyInfo.setProxyServerPort(8001)
proxyInfo.setProxyOption(ProxyOption.MANUAL_CONFIG.toString())
proxyInfo.setProxyServerType(ProxyServerType.HTTP.toString())
requestObject.setProxy(proxyInfo)
```

> The proxy information passed in the request object takes precedence over the proxy information set in **Preferences**.

### Troubleshoot proxy issues

1. If you're behind a Proxy Server, you need to configure the Authentication proxy settings before activating Katalon Studio. Click **Configure Authentication Proxy** at the bottom of the Activation dialog box.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/proxy-preferences/config-proxy-activation.png" width="70%" alt="troubleshoot proxy issue">

2. "*New and old proxy mechanisms are not allowed in one command. Please use either the new or the old one.*"

   If you encounter the above error when executing your test with Runtime Engine, please check if you are mixing options of the new mechanism with options for proxy configuration prior to 7.5.0 and correct the commands in use. [Learn more about proxy options](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#proxy-options).

**See also**:

- [Katalon Preferences](https://docs.katalon.com/katalon-studio/docs/katalon-studio-preferences.html)
- [Import Preferences](https://docs.katalon.com/katalon-studio/docs/import-preferences.html)
- [Test Case Preferences](https://docs.katalon.com/katalon-studio/docs/test-case-preferences.html)
- [Object Spy Preferences](https://docs.katalon.com/katalon-studio/docs/object-spy-preferences.html)