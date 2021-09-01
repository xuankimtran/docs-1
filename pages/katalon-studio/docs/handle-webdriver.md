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
To execute web tests successfully, make sure the version of browsers is equal to the version of browser drivers. In case the versions are different, try to upgrade or downgrade one of them to be similar. Learn more about [Common exceptions in Katalon Studio](https://docs.katalon.com/katalon-studio/docs/troubleshoot-common-execution-exceptions-web-test.html).
>
> Starting from **Katalon Studio version 7.0.0**, you can terminate WebDriver processes or update WebDrivers including Chrome, FireFox and Internet Explorer Drivers.
>
>
## Terminate WebDriver processes

From the main toolbar, select **Tools > Web > Terminate running WebDrivers** > a pop-up message appears when WebDrivers are successfully terminated.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/handle-webdrivers/Terminate-Webdrivers.png" alt="terminate-webdriver-processes" width=70%>

## Update a Webdriver
You can update a Webdriver directly from Katalon Studio applications.
From the main toolbar, select **Tools > Update WebDrivers > Select a browser in the dropdown list.**

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/handle-webdrivers/Update-Webdrivers.png" alt="update-webdriver-automatically" width=70%>

> In the console mode, you can use this command argument, `--config -webui.autoUpdateDrivers=true`, to allow WebDriver binaries to be updated automatically. Learn more about [Console Mode Execution](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html).
## Replace a Webdriver

In case you wish to upgrade or downgrade Selenium libary or Webdriver binaries to suit your test's purposes, you can do this by replacing Webdrivers. You can replace Webdriver binaries at either application-level or project-level.

Do as follows:
- Download the Webdriver version you want to run your test on.

>
> Versions of browser drivers:
> - [Chrome Drivers](https://chromedriver.chromium.org/downloads)
> - [Gecko Drivers](https://firefox-source-docs.mozilla.org/testing/geckodriver/Support.html)
> - [Internet Explorer](http://selenium-release.storage.googleapis.com/index.html)
> - [Microsoft Edge](https://developer.microsoft.com/en-us/microsoft-edge/tools/webdriver/)
>

- Navigate to Webdriver location as below.


**- Selenium library location**

* Windows: `<Katalon Studio folder>\configuration\resources\lib\selenium-server-standalone-3.x.jar`
* macOS: `/Applications/Katalon Studio.app/Contents/Eclipse/configuration/resources/lib/selenium-server-standalone-3.x.jar`

**- WebDriver binaries' (application-level) locations**

For **Window** users, you can find WebDriver binaries (application-level) at: 

**Chrome**

You can use 32-bit Windows Chromedriver for both 32-bit and 64-bit Windows.

- `<Katalon Studio folder>\configuration\resources\drivers\chromedriver_win32`
- `<Katalon Studio folder>\configuration\resources\drivers\chromedriver_win64`

**Firefox**

- `<Katalon Studio folder>\configuration\resources\drivers\firefox_win32`
- `<Katalon Studio folder>\configuration\resources\drivers\firefox_win64`

**Internet Explorer**

- `<Katalon Studio folder>\configuration\resources\drivers\iedriver_win32`
- `<Katalon Studio folder>\configuration\resources\drivers\iedriver_win64`

**Edge**

- `<Katalon Studio folder>\configuration\resources\drivers\edgedriver`

**Edge (Chromium)**

- `<Katalon Studio folder>\configuration\resources\drivers\edgechromium_win32`
- `<Katalon Studio folder>\configuration\resources\drivers\edgechromium_win64`

For **macOS** users, you can find WebDriver binaries (application-level) at: 

**Chrome**

- `/Applications/Katalon Studio.app/Contents/Eclipse/configuration/resources/drivers/chromedriver_mac`

**Firefox**

- `/Applications/Katalon Studio.app/Contents/Eclipse/configuration/resources/drivers/firefox_mac`

**Edge (Chromium)**

- `/Applications/Katalon Studio.app/Contents/Eclipse/configuration\resources\drivers\edgechromium_mac`

**- WebDriver binaries' (project-level) locations**

WebDriver binaries are replaceable at project-level by copying new files into the `Include` directory inside the project.

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
- `Include/drivers/edgechromiumdriver_win64/msedgedriver.exe`
- `Include/drivers/edgechromiumdriver_win32/msedgedriver.exe`
- `Include/drivers/edgechromiumdriver_mac/msedgedriver`

- Replace the `driver.exe` file with the downloaded `driver.exe` file. 

>**Re-run the tests**
>
> After updating or downgrading WebDrivers, to make sure the current version of the browser driver is running smoothly, it is advisable to try **re-running the test** to resolve and check any pop-up issues.
## Use DriverFactory library

Katalon Studio introduces DriverFactory to manipulate WebDriver instances by using Katalon keywords. Learn more about [DriverFactory](https://docs.katalon.com/katalon-studio/docs/using_selenium_webdriver_katalon_studio.html#driverfactory).

## Use WebDriver Event Listeners

> Starting in **Katalon Studio version 7.0.0**, the Katalon Studio's WebDriver extends the EventFiringWebDriver. Learn more about [EventFiringWebDriver](https://www.selenium.dev/selenium/docs/api/java/org/openqa/selenium/support/events/EventFiringWebDriver.html).

You can use [WebDriverEventListener](https://seleniumhq.github.io/selenium/docs/api/java/org/openqa/selenium/support/events/WebDriverEventListener.html) to handle events started by the WebDriver, which happens before or after navigation; before or after a click, etc. 

Below is an example of how to add your custom `WebDriverEventListener` method:

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
Starting from Katalon 7.0.0, the following exception shows:

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
