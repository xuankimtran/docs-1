---
title: Understanding waiting keywords
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/troubleshoot-globalvariable-special-character.html
---

When a condition is not met, Katalon Studio returns a result (either *True* or *False*) with a warning message regardless of what failure handling settings are specified.

In other words, Katalon Studio continues a test despite its failure. This behavior is similar to choosing *Optional* value for failure handling. See: [Failure Handling](https://docs.katalon.com/katalon-studio/docs/failure-handling.html).

In case the waiting keyword fails due to such error because the AUT didn't start, or because of network or session timeout, failure handling applies as your specification.

Here is an example:

The waiting keyword,`WaitForElementPresent`, only returns *True* or *False* in respect of the element's presence. If the element doesn’t present on the current view, the keyword will return *False* and show a warning message.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops-intergration.png"  width=100% alt="waiting keywords">

If you want to let the test case fail due to the element not present, please use the following script to make it an assertion:

```groovy
1 boolean present = Mobile.waitForElementPresent(findTestObject('...'), 10)`
2
3 assert present
```
