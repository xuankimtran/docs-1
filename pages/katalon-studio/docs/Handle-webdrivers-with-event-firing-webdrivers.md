---
title: "Handle WebDrivers with EventFiringWebDriver"
sidebar: katalon_studio_docs_sidebar
permalink: /katalon-studio/docs/handle-webdrivers-with-event-firing-webdriver.html
redirect_from: 
    - "/katalon-studio/docs/handle-webdrivers.html"
    - "/katalon-studio/docs/using-the-webdriver-object.html"
    - "/display/KD/Using+the+WebDriver+Object/"
    - "/display/KD/Using%20the%20WebDriver%20Object/"
    - "/x/OAXR/"
    - "/katalon-studio/docs/using-the-webdriver-object/"
    - "/display/KD/Update+or+Replace+Web+Browser+Drivers+and+Selenium/"
    - "/display/KD/Update%20or%20Replace%20Web%20Browser%20Drivers%20and%20Selenium/"
    - "/x/1xtO/"
    - "/katalon-studio/docs/update-or-replace-web-browser-drivers-and-selenium/"
    - "/katalon-studio/docs/update-or-replace-web-browser-drivers-and-selenium.html"
    - "/katalon-studio/docs/webdriver-event-listeners.html"
    - "/katalon-studio/docs/automatically-update-webdriver.html"
---

> Starting in **Katalon Studio version 7.0.0**, the Katalon Studio's WebDriver extends the `EventFiringWebDriver`. 

`EventFiringWebDriver` is a class in Selenium that wraps the WebDriver around to throw events. It is useful in many scenarios. One of which is for logging steps or triggering certain events before an operation. Learn more about [EventFiringWebDriver](https://www.selenium.dev/selenium/docs/api/java/org/openqa/selenium/support/events/EventFiringWebDriver.html).

In this article, we show you how to handle WebDrivers with the support of `EventFiringWebDriver`.
## Use WebDriver Event Listeners

You can use [WebDriverEventListener](https://seleniumhq.github.io/selenium/docs/api/java/org/openqa/selenium/support/events/WebDriverEventListener.html) to handle events started by the WebDriver, which happens for example, before or after navigation, before or after a click. If `EventFiringWebDriver` is a class that wraps the WebDriver around to throw events, `WebDriverEventListeners` is an interface to catch WebDriver events.

Below is an example of how to use your custom `WebDriverEventListener`:

1. [Create a class](https://docs.katalon.com/katalon-studio/docs/introduction-to-custom-keywords.html) named `MyCustomWebEventListener` to handle WebDriver's events.

```groovy
package customlistener

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
// Don't use changeWebDriver, there's a bug we will fix in upcoming releases and will update
// the docs to reflect the fix
DriverFactory.changeWebDriverWithoutLog(eventFiring)

WebUI.navigateToUrl('www.google.com')

WebUI.closeBrowser()
```

3. Observe the result in the Console log.

```groovy
2019-09-06 13:45:55.845 INFO  c.k.k.core.webui.driver.DriverFactory    - sessionId = 2cde39924e0651313007e6beedae94bf
2019-09-06 13:45:55.865 INFO  c.k.k.core.webui.driver.DriverFactory    - browser = Chrome 76.0.3809.132
2019-09-06 13:45:55.866 INFO  c.k.k.core.webui.driver.DriverFactory    - platform = Mac OS X
2019-09-06 13:45:55.867 INFO  c.k.k.core.webui.driver.DriverFactory    - seleniumVersion = 3.141.59
2019-09-06 13:45:55.876 INFO  c.k.k.core.webui.driver.DriverFactory    - proxyInformation = ProxyInformation{proxyOption=NO_PROXY, proxyServerType=HTTP, password=, proxyServerAddress=, proxyServerPort=0}
2019-09-06 13:45:55.888 DEBUG testcase.Event Firing Web Driver         - 2: webdriver = getWebDriver()
2019-09-06 13:45:55.895 DEBUG testcase.Event Firing Web Driver         - 3: eventFiring = webdriver
2019-09-06 13:45:55.910 DEBUG testcase.Event Firing Web Driver         - 4: eventFiring.register(new customlistener.MyCustomWebEventListener())
2019-09-06 13:45:55.927 DEBUG testcase.Event Firing Web Driver         - 5: changeWebDriverWithoutLog(eventFiring)
2019-09-06 13:45:55.947 DEBUG testcase.Event Firing Web Driver         - 6: navigateToUrl("www.google.com")
Before navigating to http://www.google.com
2019-09-06 13:45:56.965 DEBUG testcase.Event Firing Web Driver         - 7: closeBrowser()
2019-09-06 13:45:57.091 INFO  c.k.katalon.core.main.TestCaseExecutor   - END Test Cases/Ev
```

## Use RemoteWebDriver

Because `EventFiringWebDriver` does not implement the interface `RemoteWebDriver`, in case your code is currently casting the WebDriver obtained from [DriverFactory](https://docs.katalon.com/katalon-studio/docs/using_selenium_webdriver_katalon_studio.html#driverfactory) as below: 

```groovy
....
RemoteWebDriver katalonWebDriver = (RemoteWebDriver) DriverFactory.getWebDriver()
// Using RemoteWebDriver from now on

```
Starting from Katalon 7.0.0, an exception appears as below:

```groovy
Cannot cast object 'com.kms.katalon.core.webui.driver.SmartWaitWebDriver@7cab1508' with class 'com.kms.katalon.core.webui.driver.SmartWaitWebDriver' to class 'org.openqa.selenium.remote.RemoteWebDriver'
```

(From [`Russ Thomas's bug report`](https://forum.katalon.com/t/bug-katalon-v7-cannot-cast-smartwaitwebdriver-to-remotewebdriver/33236))

To obtain the RemoteWebDriver instance safely:

```groovy
....
// Cast Katalon's WebDriver into EventFiringWebDriver
EventFiringWebDriver eventFiring = (EventFiringWebDriver) DriverFactory.getWebDriver()
// Get the driver wrapped inside
WebDriver wrappedWebDriver = eventFiring.getWrappedDriver()
// Cast the wrapped driver into RemoteWebDriver
RemoteWebDriver katalonWebDriver = (RemoteWebDriver) wrappedWebDriver
// Using RemoteWebDriver from now on
```

We recommend encapsulating the above logic into a function to avoid code duplication.

## See also

- [Change WebDrivers](https://docs.katalon.com/katalon-studio/docs/change-webdrivers.html)
- [Terminate Webdrivers](https://docs.katalon.com/katalon-studio/docs/terminate-webdrivers.html)