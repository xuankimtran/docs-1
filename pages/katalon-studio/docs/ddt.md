---
title: "Data-driven Testing with Katalon Studio"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/ddt.html
---

Katalon Studio supports data-driven testing with several methods that allow test scripts to read inputs from internal or external data files. Particularly, in Katalon test cases, test objects or their properties can be parameterized as place holders and receive values during execution. You can design data-driven test scripts in Katalon Studio using:

* [Web Test Objects Parameterization](https://docs.katalon.com/katalon-studio/docs/manage-test-object.html)
* [Mobile Test Object Parameterization](https://docs.katalon.com/katalon-studio/docs/parameterize-mobile-test-object-properties.html)
* [Web Service Object Parameterization](https://docs.katalon.com/katalon-studio/docs/parameterize-a-web-service-object.html)

There are many ways of passing different sets of values through parameters in test scripts.

1. [Global Variables and parameterized global variables](https://docs.katalon.com/katalon-studio/docs/global-variables.html).
2. [Test Case Variables](https://docs.katalon.com/katalon-studio/docs/test-case-variables.html).
3. [Data Binding Feature](https://docs.katalon.com/katalon-studio/docs/run-test-case-external-data.html) and [enhanced variable binding](https://docs.katalon.com/katalon-studio/docs/bind-as-string.html).
4. `findTestData` method in Groovy Script. Learn about [TestData](https://docs.katalon.com/javadoc/com/kms/katalon/core/testdata/TestData.html).

The inputs passed through test scripts can be read from an external file such as Excel, CSV, Internal file, and Database. Learn how to [manage test data](https://docs.katalon.com/katalon-studio/docs/manage-test-data.html). 

For advanced DDT ability with Katalon Studio, Katalon Studio Enterprise users can [combine multiple data sources](https://docs.katalon.com/katalon-studio/docs/combine-multiple-data-sources.html) in the data binding section.

An example of DDT in Katalon Studio can be view specifically in [Shopping Cart Project](https://docs.katalon.com/katalon-studio/docs/shopping-cart-prj.html#test-suites), a sample project written by the Katalon Team.
