---
title: "Dynamic Test Suite" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/dynamic-test-suite.html
redirect_from:
    - "/katalon-studio/docs/dynamic-querying-test-suite/"
    - "/katalon-studio/docs/dynamic+querying+test+suite/"
    - "/katalon-studio/docs/dynamic%20querying%20test%20suite/"
description: 
---

**Dynamic Test Suite** is a built-in feature in Katalon Studio that provides query search function to some plugins and returns any matched test cases or test suites of the query statement.

This function only works when you have already installed the plugin that defines the querying syntax in Dynamic Test Suite. Visit [Katalon Store](https://store.katalon.com/?query=dynamic) and install one of the two plugins.

After the plugin has been installed, go to Katalon Studio and click **Reload Plugins**. [Learn more on how to reload plugins](https://docs.katalon.com/katalon-store/docs/user/access-store-in-KS.html#reload-plugins). In case there is no installed plugin, the Query Provider is set to “No query provider available.” by default.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/dynamic-querying-test-suite/dynamic-ts.png" width="1041" height="289">

**Query Provider**: the query syntax standard of a plugin that is currently applied. For example, when you successfully install the *Basic Search For Dynamic Test Suite* plugin, the query syntax standard becomes "Built-in".

**Query**: this search box allows you to input the query syntax manually. For example:
`id=(Test Cases/Simple Examples/Katalon Shop/Custom-keyword samples/Order and check out a single product)`.

**Query Builder** provides a convenient way to create and run query in Katalon Studio.

- **Id**: to search by the exact IDs of a test artifact.
- **Name**: to search by the name of a test artifact.
- **Tag**: to search by the tag linked to test artifacts.
- **Comment**: to search by the comments attached to test artifacts.
- **Description**: to search by the description associated with test artifacts.

*Note*: Search criteria are applied to all test artifacts including test case, test suite, folder, and etc.

**Preview**: to view the results after having the searching query.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/dynamic-querying-test-suite/result.png" width="1039" height="346">
