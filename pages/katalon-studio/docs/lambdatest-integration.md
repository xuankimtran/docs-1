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

2. In the left navigation menu, go to the **Profile** tab, you can see your **Username** and **Access Key**.

	These values are necessary for authentication between your Katalon Studio instance and LambdaTest account. They also help generate a secure remote connection between Katalon Studio and the LambdaTest remote hub URL.

	Syntax for LambdaTest remote URL: `http://username:accessKey@hub.lambdatest.com/wd/hub`.

	The following image is an example of a LambdaTest profile section. In this case, the remote URL is: `http://harshitp:ABCD1234PQRS@hub.lambdatest.com/wd/hub`.

	<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/lambdatest-integration/KS-LAMBDATEST-Username-access-keys.png" width="100%" alt="View user profile in the Lambdatest page">

	Note this LambdaTest remote URL for later input.

3. Next, specify your desired capabilities to execute your test script. To do so, navigate to the LambdaTest capabilities generator page: [Capabilities Generator](https://www.lambdatest.com/capabilities-generator/).

	LambdaTest Capabilities Generator supports various programming languages for your desired capabilities class:

	*   Java
	*   C#
	*   PHP
	*   Ruby
	*   JavaScript
	*   Python

	For example, we want to test on macOS Big sur with Chrome version 96. We also choose Java as the capabilities generator language. LambdaTest Capabilities Generator will generate desired capabilities accordingly in Java.

	<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/lambdatest-integration/KS-LAMBDATEST-Capabilities-generator.png" width="100%" alt="Lambdatest capabilities generator">


4. In Katalon Studio, go to **Project > Settings > Desired Capabilities > Remote**. Input the following information:

    *   **Remote server URL**: input the URL retrieved from step 2. For example: `http://harshitp:ABCD1234PQRS@hub.lambdatest.com/wd/hub`

    *   **Remote server type**: Choose **Selenium**.

    *   Add capabilities generated from step 3.

	<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/lambdatest-integration/KS-LAMBDATEST-Set-DC.png" width="70%" alt="Add remote server capabilities">

    > Notes:
    > * If you want to add Chrome driver capabilities, make sure to put those capabilities into the `goog:chromeOptions` property as a dictionary. For example: 
	> <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/browserstack-integration/KS-BROWSERSTACK-Add-capabilities-Chrome.png" width="70%" alt="Add Chrome capabilities for remote server">


5. Click **Apply and Close** when you are done.
6. To execute your tests with LambdaTest remote server, click **Remote** in the dropdown list next to **Run**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/browserstack-integration/KS-BROWSERSTACK-Execute-remote.png" width="30%" alt="Execute Browserstack remote server">


> Notes: 
> * LambdaTest recommends using Listeners to avoid timeout issues while executing Groovy scripts in LambdaTest Selenium Grid in Katalon Studio. To learn more about test listeners in Katalon Studio, you can refer to this document: [Test Listeners (Test Hooks)](https://docs.katalon.com/katalon-studio/docs/fixtures-listeners.html#test-listeners-test-hooks).

