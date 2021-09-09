---
title: "Change WebDrivers"
sidebar: katalon_studio_docs_sidebar
permalink: /katalon-studio/docs/change-webdrivers.html
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

> Starting from **Katalon Studio version 7.0.0**, you can update WebDrivers directly from the application. This feature supports Chrome, Firefox and Internet Explorer. 
>

## Update a Webdriver
You can update a Webdriver directly from Katalon Studio.
From the main toolbar, select **Tools > Update WebDrivers**. Select a browser in the dropdown list.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/handle-webdrivers/Update-Webdrivers.png" alt="update-webdriver-automatically" width=70%>

Alternatively, you can use this command argument  `--config -webui.autoUpdateDrivers=true` in console mode to allow automatic WebDriver updates. These kinds of console mode commands are useful for advanced users, who typically require less hand holding.
Learn more about [Console Mode Execution](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html).
## Replace a Webdriver

To upgrade or downgrade your Selenium library or WebDriver binaries, you can replace WebDrivers manually. You can choose to do so at the application or project level.

Do as follows:

1. Find the WebDriver version you want to run your test with. You can find them here:

>
> Versions of browser drivers:
> - [Chrome Drivers](https://chromedriver.chromium.org/downloads)
> - [Gecko Drivers](https://firefox-source-docs.mozilla.org/testing/geckodriver/Support.html)
> - [Internet Explorer](http://selenium-release.storage.googleapis.com/index.html)
> - [Microsoft Edge](https://developer.microsoft.com/en-us/microsoft-edge/tools/webdriver/)
>

2. Find the location of the WebDrivers you want to replace. Replace the `driver.exe` file with the one you have downloaded.
  
- For location of the Selenium Library, go to: 

* Windows: `<Katalon Studio folder>\configuration\resources\lib\selenium-server-standalone-3.x.jar`
* macOS: `/Applications/Katalon Studio.app/Contents/Eclipse/configuration/resources/lib/selenium-server-standalone-3.x.jar`

- At the application level, WebDriver binaries are stored here:

<details><summary> For Window users</summary>

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

</details>


<details><summary> For macOS users</summary>


**Chrome**

- `/Applications/Katalon Studio.app/Contents/Eclipse/configuration/resources/drivers/chromedriver_mac`

**Firefox**

- `/Applications/Katalon Studio.app/Contents/Eclipse/configuration/resources/drivers/firefox_mac`

**Edge (Chromium)**

- `/Applications/Katalon Studio.app/Contents/Eclipse/configuration\resources\drivers\edgechromium_mac`

</details>
<p>&nbsp;</p>

- At the project level, go to **\Project Folder\Include** on your computer and follow the below paths:

> **Note**
> 
> After replacing WebDrivers at project level, restart Katalon Studio to run new WebDrivers.
> 

<details><summary> For Window users</summary>

**Chrome**
- `Include/drivers/chromedriver_win32/chromedriver.exe`
- `Include/drivers/chromedriver_win64/chromedriver.exe`

**Firefox** 

- `Include/drivers/geckodriver_win32/geckodriver.exe`
- `Include/drivers/geckodriver_win64/geckodriver.exe`

**Internet Explorer**

- `Include/drivers/iedriver_win32/IEDriverServer.exe`
- `Include/drivers/iedriver_win64/IEDriverServer.exe`

**Edge (Chromium)**
- `Include/drivers/edgedriver_win32/MicrosoftWebDriver.exe`
- `Include/drivers/edgedriver_win64/MicrosoftWebDriver.exe`
- `Include/drivers/edgechromiumdriver_win64/msedgedriver.exe`
- `Include/drivers/edgechromiumdriver_win32/msedgedriver.exe`

</details>

<details><summary> For macOS users</summary>

**Chrome**
- `Include/drivers/chromedriver_mac64/chromedriver`

**Firefox**
- `Include/drivers/geckodriver_mac64/geckodriver`

**Edge (Chromium)**

- `Include/drivers/edgechromiumdriver_mac/msedgedriver`

</details>

<details><summary> For Linux users</summary>

**Chrome**
- `Include/drivers/chromedriver_linux32/chromedriver`
- `Include/drivers/chromedriver_linux64/chromedriver`

**Firefox**

- `Include/drivers/geckodriver_linux32/geckodriver`
- `Include/drivers/geckodriver_linux64/geckodriver`

</details>

<p>&nbsp;</p>

3. After finding the correct location, replace the `driver.exe` file with the one you have downloaded.
   
>**Re-run the tests**
>
> After updating or downgrading WebDrivers, to make sure the current version of the browser driver is running smoothly, it is advisable to try **re-running the test** to resolve and check any pop-up issues.
## Use DriverFactory library

Katalon Studio also offers DriverFactory library to manipulate WebDriver instances by using Katalon keywords. Learn more about [DriverFactory](https://docs.katalon.com/katalon-studio/docs/using_selenium_webdriver_katalon_studio.html#driverfactory).

## See also

- [Terminate Webdrivers](https://docs.katalon.com/katalon-studio/docs/terminate-webdrivers.html)
- [Handle WebDrivers with EventFiringWebDrivers](https://docs.katalon.com/katalon-studio/docs/handle-webdrivers-with-event-firing-webdriver.html)

