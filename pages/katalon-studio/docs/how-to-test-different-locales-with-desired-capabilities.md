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

The following sample tests is to Open and Close Browser showing in English, Spanish, French.
## Use Configured Desired Capability with data-driven approach.

Do as follow:

1. Create a New Test Case. Go to **File > New > Test Case.**

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/how-to-guides/tests-different-browser-locales-with-DC/Sample%20Test%20Case.png" width=100% alt="sample test cases">

>
2. Create Test Case Variables. 

- Switch to Variables tab of your Test Case.
- Click Add. A new row is added to the variable list.
- Input variables.
  
 For example, you want to run test case in English, input:

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
<td>"en"</td>
</tr>
</tbody>
</table>
* Default Value should be the [language code](https://developers.google.com/admin-sdk/directory/v1/languages) you want to test.
* 
<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/how-to-guides/tests-different-browser-locales-with-DC/Test%20Case%20Variable.png" width=90% alt="test case with variables">


### . Create a test suite

## Use Custom Profiles in Desired Capabilities

Before starting, make sure that you have:
- [Downloaded](https://www.selenium.dev/downloads/) Selenium Grid Hub. This app is presiquite to run Remote Selenium WebDriver (Grid).
- [Configured Selenium Grid Hub](https://www.lambdatest.com/blog/selenium-remotewebdriver/)