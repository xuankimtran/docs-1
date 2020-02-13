---
title: "Reduce Execution Time in Mobile Testing"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/mobile-reduce-execution-time.html
---

To speed up a test suite's execution time, we recommend you start the application once in the first test case and reset it in each remaining test case with the following snippet:

```groovy
import com.kms.katalon.core.mobile.keyword.internal.MobileDriverFactory
import io.appium.java_client.AppiumDriver
AppiumDriver driver = MobileDriverFactory.getDriver();
driver.resetApp()
```
