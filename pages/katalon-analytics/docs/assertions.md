---
title: "Automatically detect Assertions in each Test Case"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/assertions.html
redirect_from:
---
**Katalon TestOps** provides you details about assertions in execution reports from **Katalon Studio**. 

Assertions ensure that the application is working correctly by checking whether a condition is true, i.e., whether labels, data, API responses, etc., are rendered correctly.

This will give you a better grasp of the severity of a failure. For example, a Test Result with 1% of its Assertions have failed usually indicates a better product quality than that with 99% of the Assertions have failed.

## Prerequisites

- Integration with Katalon Studio version 7.8.2 or later.

## View the number of Assertions for each Test Result

Whenever an execution is submitted to Katalon TestOps, you can find its Assertions by going to **Test Management** > *Test Cases* > the Assertion statistics are displayed in each Test Result.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/assertions/assertions.png)

To view details of Assertions, click on the Test Result ID. Here you can find error messages and detailed logs of each Assertion.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/assertions/assertion-details.png)

## Custom a current Assertion

You can exclude a custom keyword from being identified as an Assertion in the *"Project Setting"* page of **Katalon TestOps**.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/assertions/custom-assertions.png)
