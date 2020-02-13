---
title: "Reduce Execution Time in Mobile Testing"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/mobile-reduce-execution-time.html
---

When you execute a test suite containing multiple test cases that share the same process as follows: start an application > run steps > close the application, it normally takes a significant amount of time for the test to finish.

Hence, we suggest **starting** the AUT in the first test case only and **reusing** the AUT in the remaining test cases. This trick reduces the execution time of a test suite tremendously.

To reuse the AUT in the remaining test cases, you need to restart that AUT in each test case with the following snippet:

```groovy
import com.kms.katalon.core.mobile.keyword.internal.MobileDriverFactory
import io.appium.java_client.AppiumDriver
AppiumDriver driver = MobileDriverFactory.getDriver();
driver.resetApp()
```
