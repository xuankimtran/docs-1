---
title: "Set different browser locales in Chrome with Desired Capabilities"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/how-to-test-different-browser-locales-in-chrome-with-desired-capabilities.html
redirect_from:
description:
---
<INTRODUCTION>

> You can now [reuse Desired Capabilities across projects](https://docs.katalon.com/katalon-studio/docs/import-export-desired-capabilities.html). 

For Chrome’s current design, the UI language sets default by the first/main Chrome window that opens. In order words, if you wish to alter browser locales using `chrome --lang=de`//start Chrome with German, Chrome Driver still picks the default language from the Chrome browser.
Nevertheless, you can now test different browser locales by configuring [Desired Capabilities](https://docs.katalon.com/katalon-studio/docs/introduction-to-desired-capabilities.html). 

## Use Configured Desired Capability with Test Case Variables

In this section, we show you 2 possible approaches to alter browser locales while testing: 

- To test one specific language with a test case.
- To test different languages with a test suite.

### 1. Create a test case to test one language

In the following example, we configure a test case to run with a specific browser locale, like French.

Do as follow:

1. Create a New Test Case. Go to **File > New > Test Case.**

2. Create Test Case Variables. 
To run tests with different browser locales, [Test Case Variables](https://docs.katalon.com/katalon-studio/docs/test-case-variables.html#manage-test-case-variables) comes in handy because it allows parameterizing that test case with varying language inputs.

- Switch to Variables tab of your Test Case.
- Click **Add**. A new row appears in the variable list.
- Input variables.
  
 For example, you want to run a test case in French, input:

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

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/how-to-guides/tests-different-browser-locales-with-DC/Test-case-variables-2.png" width=90% alt="test case with variables">


3. Use Configured Desired Capabilities.
After defining Test Case Variables, we override default language settings in Chrome by using [Configured Desired Capabilities](https://docs.katalon.com/katalon-studio/docs/introduction-to-desired-capabilities.html#passing-desired-capabilities-at-runtime).

- Switch to Script tab of your Test Case.
- Use the code as below. With this code, the language in the testing browser changes into the language defined in Step 2, which is, in this case, French.
```groovy

import com.kms.katalon.core.configuration.RunConfiguration

Map prefs = [('intl.accept_languages') : locale]
// Map preferences key to manipulate page's language.

RunConfiguration.setWebDriverPreferencesProperty("prefs", pref)
```

- Continue writing the script for your testing purpose.
  
<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/how-to-guides/tests-different-browser-locales-with-DC/configured-desired-capabilities.png" width=90% alt="Configured Desired Capabilities">

>
> - [Sample test cases run with local Chrome](https://github.com/katalon-studio-samples/multi-locales-sample/blob/main/Test%20Cases/Run%20with%20local%20Chrome.tc)
> 
### 2. Create a Test Suite to test different languages

> **Requerements:**
> 
> Make sure to configure all your test cases with Desired Capabilities as per Part 1. 
>
>

In the following example, we demonstrate how to create a [Test Suite with Test cases variables](https://docs.katalon.com/katalon-studio/docs/run-test-case-external-data.html#create-a-new-test-suite-with-test-case-variables) to test different browser locales. Here, we use French, English, and Spanish.

1. Create a test suite. Go to **File > New > Test Suite.**
2. Click **Add** in command toolbar, then choose pre-configured test cases.

<img src="https://github.com/katalon-studio/docs-images/raw/d22b289b2b07c6ae15b9a52e11a3cc245e725974/katalon-studio/how-to-guides/tests-different-browser-locales-with-DC/new-test-suite.png" width=70% alt="New Test Suite">

3. Create a data file. Go to **File > New > Test Data.** Choose **Data Type** as **Internal Data.**
This data file contains different [language code](https://developers.google.com/admin-sdk/directory/v1/languages) you want to test on browsers.

In this example, the language codes are `fr`,`en`,`es`.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/how-to-guides/tests-different-browser-locales-with-DC/create-new-data-file-2.png" width=70% alt="New Data file 2">

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/how-to-guides/tests-different-browser-locales-with-DC/New%20Data%20File.png" width=70% alt="New Data file">

4. Manage Data Binding
- Switch back to the test suite editor, click **Show Data Binding** to expand the **Data Binding** section. Make sure you click on the correct pre-configured test case beforehand. 
This step is to bind New Data File from Step 3 with the Test Suite you want to test. See also [Manage Data Binding](https://docs.katalon.com/katalon-studio/docs/run-test-case-external-data.html#manage-data-binding).

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/how-to-guides/tests-different-browser-locales-with-DC/show-data-variables.png" width=70% alt="Show Data Binding section">

- The final results should show as below:
  
<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/how-to-guides/tests-different-browser-locales-with-DC/Test%20Suite%20Data%20Binding.png" width=70% alt="Test Suite data">


> 
> - [Sample test suite with data binding support](https://github.com/katalon-studio-samples/multi-locales-sample/tree/main/Test%20Suites)
> 
## Use Custom Profiles in Desired Capabilities

Suppose you are using Remote Server and want to test different browser locales. You can combine it with [Custom Desired Capabilities](https://docs.katalon.com/katalon-studio/docs/introduction-to-desired-capabilities.html#remote-server) with the desired language settings to alter pre-set language in Chrome.

The following example shows how to create a custom profile with Spanish as the testing language.
Make sure that you are running Selenium Grid Hub & Node while executing the test. 
Do as follow:

1. Create a new Custom profile in Desired Capabilities function. Go to **Project > Settings > Desired Capabilities > Custom.**

2. Click **Add** on the command toolbar to add a language custom execution.
Change the name into the language you want to test for better recognition, then click on the **More** icon under the **Value** column.
  
<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/how-to-guides/tests-different-browser-locales-with-DC/name-the-spanish.png" width=70% alt="Set value for custom Desired Capabilities">


3. In the **Custom Execution Configuration Builder** dialog, specify the **Driver Name** as **Remote**, then click on the **More** icon under the **Preferences** column.
 
 <img src="https://github.com/katalon-studio/docs-images/raw/5ce4d691c2e1223380169717503cd3189ae5b1ed/katalon-studio/how-to-guides/tests-different-browser-locales-with-DC/Custom-Execution%20-Configuration%20-Builder-2.jpg" width=70% alt="Set value for custom Desired Capabilities">

- In the **Driver Builder** dialog, fill in appeared criteria as below:
  1. Remote Server URL: `http://localhost:port/wd/hub` - the URL to the Remote server.
  2. Remote Server Type: Choose **Selenium**.
  3. Click **Add** on the command toolbar as the following command.
  - **goog:chromeOptions**: Support passing the ChromeOptions object into the ChromeDriver constructor
  - **Dictionary**: the [data type](https://docs.katalon.com/katalon-studio/docs/value-types.html) permits you to input a collection of keys and values.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/how-to-guides/tests-different-browser-locales-with-DC/chromeoptions.png" width=70% alt="Set value for custom Desired Capabilities">

  4. Click **More** icon under the **Preferences** column.
  5. In the opened **Dictionary Property Builder**, input
  
<img src="https://github.com/katalon-studio/docs-images/raw/7a0462f8e1b3f6a3c973b1c70a9b7ff6de1b4b9b/katalon-studio/how-to-guides/tests-different-browser-locales-with-DC/prefs.png" width=70% alt="Set value for custom Desired Capabilities">

  6. Click **More** icon under the **Preferences** column.
  7. In the opened **Dictionary Property Builder**, input
  - **intl.accept_languages**: Support passing preference key to manipulate a page's language.
  - **String**: the [data type](https://docs.katalon.com/katalon-studio/docs/value-types.html) permits you to enter a value directly into the Value cell.
  - **es**: Spanish's language code 

<img src="https://github.com/katalon-studio/docs-images/raw/7a0462f8e1b3f6a3c973b1c70a9b7ff6de1b4b9b/katalon-studio/how-to-guides/tests-different-browser-locales-with-DC/intl.accept_languages.png" width=70% alt="Set value for custom Desired Capabilities">

  8. Results after a series of the above commands

<img src="https://github.com/katalon-studio/docs-images/raw/3e6484c7dff66c86389ba45dbbe88de452031e0e/katalon-studio/how-to-guides/tests-different-browser-locales-with-DC/final-results-2-reup.png" width=70% alt="Results after setting up custom language Remote Control dialog"> 

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/how-to-guides/tests-different-browser-locales-with-DC/final-results-3.png" width=70% alt="Final Results"> 

> Make sure the browser is updated by clicking Tools > Update WebDrivers > Choose browser.

>
> - [Sample test cases with cutom execution](https://github.com/katalon-studio-samples/multi-locales-sample/blob/main/Test%20Cases/Run%20with%20custom%20execution.tc)
>  