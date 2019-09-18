---
title: "WebDriver Event Listeners"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/webdriver-event-listeners.html
---
> Starting in **Katalon Studio version 7.0**, the Katalon Studio's WebDriver extends the  EventFiringWebDriver.

You can use [`WebDriverEventListener`](https://seleniumhq.github.io/selenium/docs/api/java/org/openqa/selenium/support/events/WebDriverEventListener.html) to handle events triggered by the WebDriver, which happens before or after navigation; before or after a click and etc. [`EventFiringWebDriver`](https://seleniumhq.github.io/selenium/docs/api/java/org/openqa/selenium/support/events/EventFiringWebDriver.html) is a class in Selenium that supports the WebDriver with event-driven capabilities. Those capabilities are useful for many use cases - one of which is for logging steps or triggering certain events before an operation.

Below is an example of how to add your custom `WebDriverEventListener` method:

1. Create a class named `MyCustomWebEventListener` to handle WebDriver's events.

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

2. Register MyCustomWebEventListener with WebDriver

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

3. Observe the result in the Console log

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

4. Using RemoteWebDriver 

Because [`EventFiringWebDriver`](https://seleniumhq.github.io/selenium/docs/api/java/org/openqa/selenium/support/events/EventFiringWebDriver.html) does not implement the interface ['RemoteWebDriver'](https://github.com/SeleniumHQ/selenium/blob/master/java/client/src/org/openqa/selenium/remote/RemoteWebDriver.java). If your code is currently casting WebDriver obtained from DriverFactory like this:

```groovy
....
RemoteWebDriver katalonWebDriver = (RemoteWebDriver) DriverFactory.getWebDriver()
// Using RemoteWebDriver from now on
```
Then in Katalon 7.0.0 (onward), the following exception will be thrown:

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

We recommend encaspulating the above logic into a function to avoid code duplication.
