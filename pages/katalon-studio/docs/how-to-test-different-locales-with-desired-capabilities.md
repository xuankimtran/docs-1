---
title: "How to test different browser locales with Desired Capabilities?"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/how-to-test-different-browser-locales-with-Desired-Capabilities.html
redirect_from:
description:
---
<INTRODUCTION>

>**Requirements**
>
> - Katalon Studio version 8.0.0 onwards
> - Katalon Runtime Engine version 8.0.0 onwards


This article shows steps by steps as of how to execute different browser locale tests with [Desired Capabilities](https://docs.katalon.com/katalon-studio/docs/introduction-to-desired-capabilities.html).

> From 8.0.0 onwards, you can [reusing Desired Capabilities across project](https://docs.katalon.com/katalon-studio/docs/import-export-desired-capabilities.html). 

The following example is to Open and Close Browser showing in English, Spanish, French.
## Use Configured Desired Capability with Test Case Variables.

Do as follow:

1. Create a New Test Case. Go to **File > New > Test Case.**

2. Create Test Case Variables. 
With the purpose of running tests with different browser locales, [Test Case Variables](https://docs.katalon.com/katalon-studio/docs/test-case-variables.html#manage-test-case-variables) comes in handy because it allows to parameterize that test case with different language inputs.

- Switch to Variables tab of your Test Case.
- Click Add. A new row is added to the variable list.
- Input variables.
  
 For example, you want to run test case in French, input:

 <table width="959">
<tbody>
<tr>
<td><strong>Name</strong></td>
<td><strong>Type</strong></td>
<td><strong>Default Value</strong></td>
</tr>
<tr>
<td>locale</td>
<td>String</td>
<td>"fr"</td>
</tr>
</tbody>
</table>
 
 - "Default Value" should be the [language code](https://developers.google.com/admin-sdk/directory/v1/languages) you want to test.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/how-to-guides/tests-different-browser-locales-with-DC/Test%20Case%20Variable.png" width=90% alt="test case with variables">


3. Use Configured Desired Capabilities.
After defining Test Case Variables, the idea is to override predefined language in `ChromeOptions`
by using [Configured Desired Capabilities](https://docs.katalon.com/katalon-studio/docs/introduction-to-desired-capabilities.html#passing-desired-capabilities-at-runtime).

- Switch to Script tab of your Test Case.
- Use the sample code below.
```groovy

import com.kms.katalon.core.configuration.RunConfiguration

Map prefs = [('intl.accept_languages') : locale]
\\ Map preferences key to manipulate a page's language.

RunConfiguration.setWebDriverPreferencesProperty("prefs", pref)
```
- Continue writing the script, then run the test in browser.
  
<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/how-to-guides/tests-different-browser-locales-with-DC/Configured%20Desired%20Capabilities.png" width=90% alt="Configired Desired Capabililities">

4. Create a test suite

Create a new [Test Suite with Test Case Variable](https://docs.katalon.com/katalon-studio/docs/run-test-case-external-data.html#create-a-new-test-suite-with-test-case-variables) with data input should be different [language code](https://developers.google.com/admin-sdk/directory/v1/languages) you want to test on browsers.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/how-to-guides/tests-different-browser-locales-with-DC/New%20Data%20File.png" width=90% alt="Configired Desired Capabililities">


<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/how-to-guides/tests-different-browser-locales-with-DC/Test%20Suite%20Data%20Binding.png" width=100% alt="Configired Desired Capabililities">


## Use Custom Profiles in Desired Capabilities

Before starting, make sure that you have:
- [Downloaded](https://www.selenium.dev/downloads/) Selenium Grid Hub. This app is presiquite to activate Remote Execution for WebUI.
- [Configured Selenium Grid Hub.](https://www.lambdatest.com/blog/selenium-remotewebdriver/)

The idea is to use [Custom Desired Capabilities](https://docs.katalon.com/katalon-studio/docs/introduction-to-desired-capabilities.html#remote-server) to define a certain language option for execution.

Do as follow:
1. Create a new Custom in Desired Capabilities function. 
- Go to **Project > Settings > Desired Capabilities > Custom.**

<img src="url" width=100% alt="Custom Desired Capabililities">

- Click **Add** on the command toolbar to add a language custom execution.
- Change the name into the language you want to test for better recognition, then click on the **More** icon under the **Value** column.
  
<img src="url" width=100% alt="Set value for custom Desired Capabilities">

- In the **Custom Execution Configuration Builder** dialog, specify the **Driver Name** as **Remote**, then click on the **More** icon under the **Preferences** column.
 
 <img src="url" width=100% alt="Set Remote Control for custom Desired Capabilities"> 

- In the **Driver Builder** dialog, fill in appeared criterias as below:
  - Remote Server URL: `http://localhost:4444/wd/hub`
  
**where** localhost is your machine IP address.
- MacOS IP addresss: **System Preferences > Network > click on the TCP/IP tab**
- Windows IP address: **Control panel > Network and Internet > Network and Sharing Center > Change adapter settings > Double-click Ethernet > Details > Scroll down until you find the IPv4 Address**

  - Remote Server Type: Choose **Selenium**
  - Click **Add** on the command toolbar as following command
  
<table width="781">
<tbody>
<tr>
<td><strong>Name</strong></td>
<td><strong>Type&nbsp;</strong></td>
<td><strong>Value</strong></td>
</tr>
<tr>
<td>browserName</td>
<td>String</td>
<td>chrome</td>
</tr>
<tr>
<td>goog:chromeOptions</td>
<td>Dictionary</td>
<td>Click <strong>More</strong> icon to navigate to <strong>*Dictionary Property Builder.*</strong></td>
</tr>
</tbody>
</table>  

 <img src="url" width=100% alt="Set language custom in Remote Control dialog"> 

    - In the opened **Dictionary Property Builder**, input
<table width="781">
<tbody>
<tr>
<td><strong>Name</strong></td>
<td><strong>Type&nbsp;</strong></td>
<td><strong>Value</strong></td>
</tr>
<tr>
<td>prefs</td>
<td>Dictionary</td>
<td>Click More to navigate to *Dictionary Property Builder.*</td>
</tr>
</tbody>
</table>

- In the opened **Dictionary Property Builder**, input



> Make sure the browser is updated by clicking Tools > Update WebDrivers > Choose browser.

> - Use Configured Desired Capability with Test Case Variables. Sample Project
> - Use Custom Profiles in Desired Capabilities. Sample Project