---
title: Understand waiting keywords
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/understand-waiting-keyword.html
---

When a condition is not met, Katalon Studio returns a result (either *True* or *False*) with a warning message regardless of what failure handling settings are specified.

In other words, Katalon Studio continues running despite a test's failure. This behavior is similar to choosing *Optional* value for failure handling. See: [Failure Handling](https://docs.katalon.com/katalon-studio/docs/failure-handling.html).

In case the waiting keyword fails due to such errors as network problem, session timeout, or because the AUT didn't start, failure handling then applies your specified settings.

Here is an example:

If you use the waiting keyword, `WaitForElementPresent`, Katalon Studio only returns a *True* or *False* result in respect of the element's presence. If the element doesn’t present on the current view, Katalon Studio returns a *False* result and shows a warning message (Failure Handling = Optional).

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/understand-waiting-keywords/waiting-keyword.png"  width=100% alt="waiting keywords">

If you want to let the test case fail due to the element not present, use the following script to make it an assertion:

```groovy
1 boolean present = Mobile.waitForElementPresent(findTestObject('...'), 10)`
2
3 assert present
```
