---
title: "Create Mobile Test Object in Object Repository during Runtime" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/create-mobile-test-object-object-repo-in-runtime.html 
---
You can create a new Mobile Test Object in Object Repository during runtime using this custom keyword:

```groovy
/**
* Construct a Katalon-compatible TestObject in memory.
* @param css (String) The CSS selector used to find the target element.
* @return (TestObject) The constructed TestObject.
*/
@Keyword
static TestObject makeTO(String css) {
	TestObject to = new TestObject()
	to.addProperty("css", ConditionType.EQUALS, css)
	return to
}

```

_Credit to [Russ Thomas](https://forum.katalon.com/discussion/6171/creation-of-test-object-in-object-repository-in-runtime#Comment_13991)_