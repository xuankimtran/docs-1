---
title: "How to test different browser locales in Chrome with Desired Capabilities?"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/how-to-test-different-browser-locales-with-Desired-Capabilities.html
redirect_from:
description:
---
<INTRODUCTION>

>**Requirements**
>
> - Katalon Studio version 8.0.0 onwards


For Chrome’s current design, the UI language sets default by the first/main Chrome window that opens. In order words, if you wish to alters browser locales using `chrome --lang=de`//start Chrome with German, Chrome Driver still picks the default language from the Chrome browser.
Nevertheless, you can now test different browser locales by configuring [Desired Capabilities](https://docs.katalon.com/katalon-studio/docs/introduction-to-desired-capabilities.html). 

> From 8.0.0 onwards, you can [reusing Desired Capabilities across project](https://docs.katalon.com/katalon-studio/docs/import-export-desired-capabilities.html). 
## Use Configured Desired Capability with Test Case Variables.

In the following example, we demonstrate how to create a Test Suite containing several Test cases with different Browser locales. Here, we use French, English and Spanish.
First, we configure a test case to run with a specific browser locale, like French.

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
After defining Test Case Variables, we override default language settings in Chrome by using [Configured Desired Capabilities](https://docs.katalon.com/katalon-studio/docs/introduction-to-desired-capabilities.html#passing-desired-capabilities-at-runtime).

- Switch to Script tab of your Test Case.
- Use the code as below. With this code, the language in testing broswer changes into the language defined in Step 2 which is, in this case, French.
```groovy

import com.kms.katalon.core.configuration.RunConfiguration

Map prefs = [('intl.accept_languages') : locale]
// Map preferences key to manipulate page's language.

RunConfiguration.setWebDriverPreferencesProperty("prefs", pref)
```

- Continue writing the script for your testing purpose.
  
<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/how-to-guides/tests-different-browser-locales-with-DC/Configured%20Desired%20Capabilities.png" width=90% alt="Configured Desired Capabilities">

4. Create a test suite

After configuring all your test cases with Desired Capabilities, use configured test cases to create a test suite with different browser locales. The example here uses French, English, Spanish.

Create a new [Test Suite with Test Case Variable](https://docs.katalon.com/katalon-studio/docs/run-test-case-external-data.html#create-a-new-test-suite-with-test-case-variables) with data input should be different [language code](https://developers.google.com/admin-sdk/directory/v1/languages) you want to test on browsers.

For the purpose of this example, the language codes are `fr`,`en,`,`es`.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/how-to-guides/tests-different-browser-locales-with-DC/New%20Data%20File.png" width=70% alt="New Data file">


<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/how-to-guides/tests-different-browser-locales-with-DC/Test%20Suite%20Data%20Binding.png" width=100% alt="Test Suite data">


## Use Custom Profiles in Desired Capabilities

The purpose of this approach is to create a custom profile with the desired language settings,then combine with Remote Server to open `chromedriver.exe` using this profile.
The idea is to use [Custom Desired Capabilities](https://docs.katalon.com/katalon-studio/docs/introduction-to-desired-capabilities.html#remote-server) combined with Selenium Remote WebDriver to alter pre-set language in Chrome.

Do as follow:

1. Implement Selenium Grid Hub & Node

- [Downloaded](https://www.selenium.dev/downloads/) Selenium Grid. Selenium Grid is presiquite to activate Remote Execution in Katalon Studio.
- Follow this video tutorial shows to configure [Selenium Grid Hub & Node](https://docs.katalon.com/katalon-studio/videos/test_execution_on_remote_machines.html)

**Note:**
- Make sure to change the version number from the command accordingly.
- Selenium Grid server is up and running till the time command prompt window closes.
- Selenium Grid, by default uses port <4444> for its web interface. To start the same on other port, use this command: `java -jar selenium-server-standalone-3.3.1.jar -port 4455 -role hub`

2. Create a new Custom profile in Desired Capabilities function. 
- Go to **Project > Settings > Desired Capabilities > Custom.**

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/how-to-guides/tests-different-browser-locales-with-DC/Custom%20Desired%20Capabilities.png" width=100% alt="Custom Desired Capabililities">

- Click **Add** on the command toolbar to add a language custom execution.
- Change the name into the language you want to test for better recognition, then click on the **More** icon under the **Value** column.
  
<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/how-to-guides/tests-different-browser-locales-with-DC/Set%20Value%20for%20Custom%20Execution%20Configuration%20Builder.png" width=100% alt="Set value for custom Desired Capabilities">


- In the **Custom Execution Configuration Builder** dialog, specify the **Driver Name** as **Remote**, then click on the **More** icon under the **Preferences** column.
 
 <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/how-to-guides/tests-different-browser-locales-with-DC/Custom%20Execution%20Configuration%20Builder.jpg" width=100% alt="Set value for custom Desired Capabilities">

- In the **Driver Builder** dialog, fill in appeared criterias as below:
  1. Remote Server URL: `http://localhost:port/wd/hub`. This URL retrieves from Step 1.

  2. Remote Server Type: Choose **Selenium**
  3. Click **Add** on the command toolbar as following command

  
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

  4. In the opened **Dictionary Property Builder**, input
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

   5.In the opened **Dictionary Property Builder**, input
<table>
<tbody>
<tr>
<td><strong>Name</strong></td>
<td><strong>Type&nbsp;</strong></td>
<td><strong>Value</strong></td>
</tr>
<tr>
<td>
<div>
<div data-qa="message_content">
<div>
<div>
<div data-qa="block-kit-renderer">
<div>
<div dir="auto">
<div>intl.accept_languages</div>
</div>
</div>
</td>
<td>String</td>
<td>fr</td>
</tr>
</tbody>
</table>

> Know more about type "String","Dictionary" at [Date type](https://docs.katalon.com/katalon-studio/docs/value-types.html)

   6. The results after a series of above command is

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/how-to-guides/tests-different-browser-locales-with-DC/Final%20results%20with%20customs%20in%20DC.png" width=100% alt="Results after setting up custom language Remote Control dialog"> 

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/how-to-guides/tests-different-browser-locales-with-DC/Final%20results.png" width=100% alt="Final Results"> 

> Make sure the browser is updated by clicking Tools > Update WebDrivers > Choose browser.

> - Use Configured Desired Capability with Test Case Variables. Sample Project
> - Use Custom Profiles in Desired Capabilities. Sample Project