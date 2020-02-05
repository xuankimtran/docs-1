---
title: "Handle WebDrivers"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/handle-webdrivers.html
redirect_from:
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

> Starting from **Katalon Studio version 7.0**, you can terminate WebDriver processes or update WebDrivers including Chrome, FireFox and Internet Explorer Drivers.

## Terminate WebDriver processes

From the main toolbar, select **Tools > Web > Terminate running WebDrivers**> a pop-up message will inform whether your operation succeeds or not.

## Update a WebDriver

From the main toolbar, select **Tools > Update WebDrivers >** select a browser in the drop-down list.

> In the console mode, you can use this command argument, `--config -webui.autoUpdateDrivers=true`, to allow WebDriver binaries to be updated automatically. Learn more about [Console Mode Execution](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html).

## Replace Selenium library

Location:

* Windows: `<Katalon Studio folder>\configuration\resources\lib\selenium-server-standalone-3.x.jar`
* macOS: `/Applications/Katalon Studio.app/Contents/Eclipse/configuration/resources/lib/selenium-server-standalone-3.x.jar`

## Replace WebDriver binaries (application-level)

### Windows

**Chrome**

You can use 32-bit Windows Chromedriver for both 32-bit and 64-bit Windows.

Location:
- `<Katalon Studio folder>\configuration\resources\drivers\chromedriver_win32`
- `<Katalon Studio folder>\configuration\resources\drivers\chromedriver_win64`

**Firefox**

Location:
- `<Katalon Studio folder>\configuration\resources\drivers\firefox_win32`
- `<Katalon Studio folder>\configuration\resources\drivers\firefox_win64`

**Internet Explorer**

Location:
- `<Katalon Studio folder>\configuration\resources\drivers\iedriver_win32`
- `<Katalon Studio folder>\configuration\resources\drivers\iedriver_win64`

**Edge**

Location:
- `<Katalon Studio folder>\configuration\resources\drivers\edgedriver`

### macOS

**Chrome**

Location:
- `/Applications/Katalon Studio.app/Contents/Eclipse/configuration/resources/drivers/chromedriver_mac`

**Firefox**

Location:
- `/Applications/Katalon Studio.app/Contents/Eclipse/configuration/resources/drivers/firefox_mac`

## Replace WebDriver binaries (project-level)

WebDriver binaries can be replaced at project-level by copying new files into the `Include` directory inside the project.

Location:

- `Include/drivers/chromedriver_win32/chromedriver.exe`
- `Include/drivers/chromedriver_win64/chromedriver.exe`
- `Include/drivers/chromedriver_mac64/chromedriver`
- `Include/drivers/chromedriver_linux32/chromedriver`
- `Include/drivers/chromedriver_linux64/chromedriver`
- `Include/drivers/geckodriver_win32/geckodriver.exe`
- `Include/drivers/geckodriver_win64/geckodriver.exe`
- `Include/drivers/geckodriver_mac64/geckodriver`
- `Include/drivers/geckodriver_linux32/geckodriver`
- `Include/drivers/geckodriver_linux64/geckodriver`
- `Include/drivers/iedriver_win32/IEDriverServer.exe`
- `Include/drivers/iedriver_win64/IEDriverServer.exe`
- `Include/drivers/edgedriver_win32/MicrosoftWebDriver.exe`
- `Include/drivers/edgedriver_win64/MicrosoftWebDriver.exe`

## Use the WebDriver Object

To use the current session created by Katalon Studio, you can refer to example code below:  

```groovy
WebDriver driver = DriverFactory.getWebDriver()

```

The returned '**driver**' parameter will use the current browser's session launched by Katalon Studio. You need to import necessary libraries also (can be done by pressing **Ctrl + Shift + O**).

## WebDriver Event Listeners

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

Because [`EventFiringWebDriver`](https://seleniumhq.github.io/selenium/docs/api/java/org/openqa/selenium/support/events/EventFiringWebDriver.html) does not implement the interface ['RemoteWebDriver'](https://github.com/SeleniumHQ/selenium/blob/master/java/client/src/org/openqa/selenium/remote/RemoteWebDriver.java). If your code is currently casting the WebDriver obtained from DriverFactory like this:

```groovy
....
RemoteWebDriver katalonWebDriver = (RemoteWebDriver) DriverFactory.getWebDriver()
// Using RemoteWebDriver from now on

```
Then starting from Katalon 7.0.0, the following exception will be thrown:

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
