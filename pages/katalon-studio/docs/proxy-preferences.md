---
title: "Proxy Preferences" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/proxy-preferences.html 
redirect_from:
    - "/display/KD/Proxy+Preferences/"
    - "/display/KD/Proxy%20Preferences/"
    - "/x/hw1O/"
    - "/katalon-studio/docs/proxy-preferences/"
description: 
---
Proxy can be configured at: **Katalon Studio> Preferences > Katalon > Proxy**. This setting affects both WebUI and WebService testings.

In the Proxy Settings, you can select one of three options below.

* **No proxy**: there's no proxy.

* **Use system proxy configuration**: Katalon Studio guesses which proxy server your system is behind by checking Java, browser and operating system settings, and environment variables.

  > Notes: Proxy auto-config (PAC) file is supported in version 7.1 and later. You need to select **Use system proxy configuration** to utilize a PAC file.
  
* **Manual proxy configuration**: you can manually set up your proxy.
  * Address: a HTTP Proxy host.
  * Port: a HTTP Proxy port.
  * Excludes: A list of addresses separated by comma to exclude. This proxy exception list is available in Katalon Studio version 7.2 and later.
<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/proxy-preferences/proxy-manual.png" width="663.5" height="">

> If you're behind a Proxy Server, you'll need to configure the proxy settings before activating Katalon Studio. Click **Config Proxy** at the bottom of the Activation dialog box.

## Pass proxy details through the script

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
