---
title: "Handle WebDrivers with EventFiringWebDriver"
sidebar: katalon_studio_docs_sidebar
permalink: /katalon-studio/docs/handle-webdrivers-with-event-firing-webdriver.html
redirect_from: 
    - "/katalon-studio/docs/webdriver-event-listeners.html"
---

> Starting in **Katalon Studio version 7.0.0**, you can use the Selenium-based class `EventFiringWebDriver` to configure event-driven capabilities related to your WebDrivers for test execution. 

This can be used for example when logging steps or triggering certain events before an operation. You can learn more about this class from the Selenium documentation here: [EventFiringWebDriver](https://www.selenium.dev/selenium/docs/api/java/org/openqa/selenium/support/events/EventFiringWebDriver.html).

In this article, we show you how to handle WebDrivers with the support of `EventFiringWebDriver`.
## Use WebDriver Event Listeners

You can use `WebDriverEventListener` to handle events started by the WebDriver, which happens for example, before or after navigation, before or after a click. If `EventFiringWebDriver` is a class that wraps around the WebDriver to throw events, `WebDriverEventListeners` is an interface to catch WebDriver events. You can learn more about this interface from the Selenium documentation here: [WebDriverEventListener](https://seleniumhq.github.io/selenium/docs/api/java/org/openqa/selenium/support/events/WebDriverEventListener.html)

Below is an example of how to add a custom `WebDriverEventListener`:

1. Create a new keyword to handle WebDriver events.
- Go to **File > New > Keywords**. Name it as **MyCustomWebEventListener**. Click **OK**.
- Copy and paste below sample code into the created keyword.

```groovy

import org.openqa.selenium.WebDriver
import org.openqa.selenium.support.events.AbstractWebDriverEventListener

public class MyCustomWebEventListener extends AbstractWebDriverEventListener {
	@Override
	public void beforeNavigateTo(String url, WebDriver driver) {
		 println "Before navigating to " + url;
	}
}
```

2. Register `MyCustomWebEventListener` with WebDriver.

```groovy
import org.openqa.selenium.WebDriver as WebDriver
import org.openqa.selenium.support.events.EventFiringWebDriver as EventFiringWebDriver

import com.kms.katalon.core.webui.driver.DriverFactory as DriverFactory
import com.kms.katalon.core.webui.keyword.WebUiBuiltInKeywords as WebUI

import customlistener.MyCustomWebEventListener as MyCustomWebEventListener

WebUI.openBrowser('')

WebDriver webdriver = DriverFactory.getWebDriver()

EventFiringWebDriver eventFiring = ((webdriver) as EventFiringWebDriver)

eventFiring.register(new MyCustomWebEventListener())

DriverFactory.changeWebDriver(eventFiring)

WebUI.navigateToUrl('www.google.com')

WebUI.closeBrowser()
```

3. Observe the result in the Console log.

```groovy
2021-09-13 09:16:21.722 INFO  c.k.k.core.webui.driver.DriverFactory    - sessionId = ebf7a901164241457b656ffece5da9b0
2021-09-13 09:16:21.747 INFO  c.k.k.core.webui.driver.DriverFactory    - browser = Chrome 93.0.4577.63
2021-09-13 09:16:21.753 INFO  c.k.k.core.webui.driver.DriverFactory    - platform = Mac OS X
2021-09-13 09:16:21.754 INFO  c.k.k.core.webui.driver.DriverFactory    - seleniumVersion = 3.141.59
2021-09-13 09:16:21.773 INFO  c.k.k.core.webui.driver.DriverFactory    - proxyInformation = ProxyInformation { proxyOption=NO_PROXY, proxyServerType=HTTP, username=, password=********, proxyServerAddress=, proxyServerPort=0, executionList="", isApplyToDesiredCapabilities=true }
2021-09-13 09:16:22.642 DEBUG testcase.WebDriver Event Listeners       - 2: webdriver = getWebDriver()
2021-09-13 09:16:22.652 DEBUG testcase.WebDriver Event Listeners       - 3: eventFiring = webdriver
2021-09-13 09:16:22.673 DEBUG testcase.WebDriver Event Listeners       - 4: eventFiring.register(new customlistener.MyCustomWebEventListener())
2021-09-13 09:16:22.693 DEBUG testcase.WebDriver Event Listeners       - 5: changeWebDriver(eventFiring)
2021-09-13 09:16:22.699 INFO  c.k.k.core.webui.driver.DriverFactory    - sessionId = ebf7a901164241457b656ffece5da9b0
2021-09-13 09:16:22.711 INFO  c.k.k.core.webui.driver.DriverFactory    - browser = Chrome 93.0.4577.63
2021-09-13 09:16:22.711 INFO  c.k.k.core.webui.driver.DriverFactory    - platform = Mac OS X
2021-09-13 09:16:22.712 INFO  c.k.k.core.webui.driver.DriverFactory    - seleniumVersion = 3.141.59
2021-09-13 09:16:22.713 INFO  c.k.k.core.webui.driver.DriverFactory    - proxyInformation = ProxyInformation { proxyOption=NO_PROXY, proxyServerType=HTTP, username=, password=********, proxyServerAddress=, proxyServerPort=0, executionList="", isApplyToDesiredCapabilities=true }
2021-09-13 09:16:22.722 DEBUG testcase.WebDriver Event Listeners       - 6: navigateToUrl("www.google.com")
Before navigating to http://www.google.com
2021-09-13 09:16:23.220 DEBUG testcase.WebDriver Event Listeners       - 7: closeBrowser()
2021-09-13 09:16:23.243 INFO  c.k.katalon.core.main.TestCaseExecutor   - END Test Cases/WebDriver Event Listeners
```

## Use RemoteWebDriver

Because `EventFiringWebDriver` does not implement the interface `RemoteWebDriver`, to obtain a RemoteWebDriver instance safely, do as follows:

```groovy
....
// Cast Katalon's WebDriver into EventFiringWebDriver
EventFiringWebDriver eventFiring = (EventFiringWebDriver) DriverFactory.getWebDriver()
// Get the driver wrapped inside
WebDriver wrappedWebDriver = eventFiring.getWrappedDriver()
// Cast the wrapped driver into RemoteWebDriver
RemoteWebDriver katalonWebDriver = (RemoteWebDriver) wrappedWebDriver
// Katalon now uses RemoteWebDriver instead of your local driver
```
We recommend encapsulating the above logic into a function to avoid code duplication.

> Note:
> 
> This is to avoid an exception in the case that your code is casting the WebDriver from DriverFactory, such as with:
>
> ```groovy
> ....
> RemoteWebDriver katalonWebDriver = (RemoteWebDriver) DriverFactory.getWebDriver()
>
> ```
> In this scenario, from Katalon Studio 7.0.0, an exception would appear as below:
>
> ```groovy
> Cannot cast object 'com.kms.katalon.core.webui.driver.SmartWaitWebDriver@7cab1508' with class 'com.kms.katalon.core.webui.driver.SmartWaitWebDriver' to class 'org.openqa.selenium.remote.RemoteWebDriver'
> ```
>
> (From [`Russ Thomas's bug report`](https://forum.katalon.com/t/bug-katalon-v7-cannot-cast-smartwaitwebdriver-to-remotewebdriver/33236))

## See also

- [Update or Downgrade WebDrivers](https://docs.katalon.com/katalon-studio/docs/update-or-downgrade-webdrivers.html)
- [Terminate Webdrivers](https://docs.katalon.com/katalon-studio/docs/terminate-webdrivers.html)