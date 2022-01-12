---
title: "BrowserStack Integration" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/browserstack-integration.html 
redirect_from:
    - "/display/KD/BrowserStack+Integration/"
    - "/display/KD/BrowserStack%20Integration/"
    - "/x/mRdO/"
    - "/katalon-studio/docs/browserstack-integration/"
description: 
---

The BrowserStack integration helps you execute your tests on BrowserStack Selenium Grid from your Katalon Studio instance. To integrate with BrowserStack, you need to execute your test scripts on a remote web server configured in desired capabilities. To learn more about setting up the remote server in desired capabilities, you can refer to this document: [Set up remote server in desired capabilities](https://docs.katalon.com/katalon-studio/docs/desired-capabilities-remote-settings.html#set-desired-capabilities-for-remote-execution-in-katalon-studio).

This article demonstrates how to set up BrowserStack integration.

1.  Login to BrowserStack.

2.  On the left side of the BrowserStack account page, you can see your username and the Access Key value. These values are necessary for authentication between your Katalon Studio instance and the BrowserStack account.

    Syntax for the BrowserStack remote URL: `http://username:accessKey@hub-cloud.browserstack.com/wd/hub`. 
     
    For example: `http://abcdef121:affdfsr543xyz@hub-cloud.browserstack.com/wd/hub`.
    
    Note this BrowserStack remote URL for later input.
    
3.  Navigate to the Browserstack capabilities generator page: [Capabilities Generator](https://www.browserstack.com/automate/capabilities).

4.  Select the operating system and the device/browser you wish to execute with. Here, we select iOS and iPhone 12 device. We also choose Java as the generator language. Browserstack Capabilities Generator will generate desired capabilities accordingly in Java.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/browserstack-integration/KS-BROWSERSTACK-Capabilities-generator.png" width="70%" alt="Select Browserstack capabilities">

5. In Katalon Studio, go to **Project > Settings > Desired Capabilities > Remote**. Input the following information:

    *   **Remote server URL**: input the URL retrieved from step 2. For example: `http://abcdef121:affdfsr543xyz@hub-cloud.browserstack.com/wd/hub`

    *   **Remote server type**: Choose **Selenium/Appium**. Here, we choose **Appium**. From Katalon Studio version 6.3.0 onwards, when choosing Appium server, you also need to select **Android Driver/iOS Driver**.

    *   Add capabilities generated from step 4.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/browserstack-integration/KS-BROWSERSTACK-Add-DC-remote.png" width="70%" alt="Add remote server capabilities">

    > Notes:
    > * For Appium remote web server, you need to add the `platformName` capabilities. You can learn more about Appium capabilities in the Appium document here: [Appium Desired Capabilities](http://appium.io/docs/en/writing-running-appium/caps/).
    > * If you want to add Chrome driver capabilities, make sure to put those capabilities into the `goog:chromeOptions` property as a dictionary. For example:
    > <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/browserstack-integration/KS-BROWSERSTACK-Add-capabilities-Chrome.png" width="70%" alt="Add Chrome capabilities for remote server">

6. Click **Apply and Close** when you are done.
7. To execute your tests with Browserstack Selenium Grid, click **Remote** in the dropdown list next to **Run**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/browserstack-integration/KS-BROWSERSTACK-Execute-remote.png" width="30%" alt="Execute Browserstack remote server">