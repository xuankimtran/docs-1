---
title: "LambdaTest Integration" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/lambdatest-integration.html 
redirect_from:
    - "/display/KD/LambdaTest+Integration/"
    - "/display/KD/LambdaTest%20Integration/"
    - "/katalon-studio/docs/lambdatest-integration/"
description: 
---
The LambdaTest integration helps you run your tests on LambdaTest Selenium Grid from your Katalon Studio instance. To integrate with LambdaTest, you need to execute your test scripts on a remote web server configured in desired capabilities. To learn more about setting up the remote server in desired capabilities, you can refer to this document: [Set up remote server in desired capabilities](https://docs.katalon.com/katalon-studio/docs/desired-capabilities-remote-settings.html#set-desired-capabilities-for-remote-execution-in-katalon-studio).

This article demonstrates how to set up LambdaTest integration.

1. Log in to your LambdaTest account.

2. In the left navigation menu inside the LambdaTest web application, go to the **Profile** tab, then enter your **Username** and **Access Key**.

	These values are necessary for authentication purpose between your Katalon Studio instance and LambdaTest account. They also helps generate a secure remote connection between Katalon Studio and LambdaTest remote hub URL.

	Syntax for LambdaTest remote URL: `http://username:accessKey@hub.lambdatest.com/wd/hub`.

	![](../../images/katalon-studio/docs/lambdatest-integration/lambda-1.png)

	The above image is an example of a **LambdaTest Profile** section. In this case, the remote URL is: `http://harshitp:ABCD1234PQRS@hub.lambdatest.com/wd/hub`.

3. Now, you need to specify your desired capabilities to execute your test automation script. To do so, the **LambdaTest Capabilities Generator** will provide the desired capabilities the class to run scripts in LambdaTest Selenium Grid. 

	LambdaTest Capabilities Generator supports various programming languages for your desired capabilities class:

	*   Java
	*   C#
	*   PHP
	*   Ruby
	*   JavaScript
	*   Python

	For example, you want to test on macOS Mojave using the Google Chrome browser version 75 on a screen resolution of 1024x768. Then the Capability Generator will provide you with the desired capabilities class below for Java frameworks.

	<img src="url" width="70%" alt="Add remote server capabilities">


4. In Katalon Studio, go to **Project > Settings > Desired Capabilities > Remote**. Input the following information:

    *   **Remote server URL**: input the URL retrieved from step 2. For example: `http://abcdef121:affdfsr543xyz@hub-cloud.browserstack.com/wd/hub`

    *   **Remote server type**: Choose **Selenium/Appium**. Here, we choose **Selenium**.

    *   Add capabilities generated from step 3.

	<img src="url" width="70%" alt="Add remote server capabilities">

    > Notes:
    > * For Appium remote web server, you need to add the `platformName` capabilities. You can learn more about Appium capabilities in the Appium document here: [Appium Desired Capabilities](http://appium.io/docs/en/writing-running-appium/caps/).
    > * If you want to add Chrome driver capabilities, make sure to put those capabilities into the `goog:chromeOptions` property as a dictionary.
    > <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/browserstack-integration/KS-BROWSERSTACK-Add-capabilities-Chrome.png" width="70%" alt="Add Chrome capabilities for remote server">


5. Click **Apply and Close** when you are done.
6. To execute your tests with LambdaTest remote server, click **Remote** in the dropdown list next to **Run**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/browserstack-integration/KS-BROWSERSTACK-Execute-remote.png" width="30%" alt="Execute Browserstack remote server">


> Notes: 
> * LambdaTest recommends using Listeners to avoid timeout issues while executing Groovy scripts in LambdaTest Selenium Grid in Katalon Studio. To learn more about test listeners in Katalon Studio, you can refer to this document: [Test Listeners (Test Hooks)](https://docs.katalon.com/katalon-studio/docs/fixtures-listeners.html#test-listeners-test-hooks).

