---
title: "Search Test Cases"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/search.html
redirect_from:
    - "/katalon-studio/docs/advanced-search/"
    - "/katalon-studio/docs/advanced+search/"
    - "/katalon-studio/docs/advanced%20search/"
    - "/katalon-studio/docs/advanced-search.html"
    - "/katalon-studio/docs/advanced+search.html"
    - "/katalon-studio/docs/advanced%20search.html"
    - "/katalon-studio/docs/dynamic-querying-test-suite.html"
description: 
---
> Query Builder applies ONLY to the **built-in** advanced search function.

Searching manually for test artifacts can be time-consuming. The Query Builder in Katalon Studio helps reduce time finding the desired test artifacts based on given criteria.

The search function is used for test artifacts such as test cases, test suites, and folders.

There are two ways to use the Search function in Katalon Studio: input your search criteria directly on the **Search bar** or use the **Query Builder** button.

This article guides you through how to view basic information of an object and how to use the search function in Katalon Studio.

## IDs and Properties

IDs and tags can be helpful when it comes to managing large projects. You can use IDs and tags to find test artifacts in the Search function.
### How to get a test artifact ID?

To get the ID of a test artifact, do as follows:

Navigate to **Tests Explorer** and find the test artifact that you want to get the ID. Right-click on that test artifact and select **Copy ID**. The ID is now copied to your clipboard. Then, you can paste that ID into the ID text box.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/search/copy-ID.png" alt="copy ID" width="60%">

### View a test artifact properties

You can also find **ID**, **Name**, **Description**, and **Tag** of a test artifact by viewing the **Properties**. However, you cannot view the properties of a folder.

To view the properties of a test artifact, do as follows:

Navigate to **Tests Explorer** and find the test artifact that you want to view the properties. Right click on that test artifact and select **Properties**. The **Properties** dialog appears.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/search/tc-properties.png" alt="test case properties" alt="60%">

## The search bar

Another way to search for test test artifacts is to type on the search bar directly. This search bar is located at the top of the **Test Explorer** section. For example:

`id=(Test Cases/Common Test Cases)`

All test cases associated with the `Test Cases/Common Test Cases` ID are filtered and returned.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/search/search-bar.png" alt="search bar" width="60%">

> Notes:
>
> To search for test artifacts labeled with multiple tags, follow this syntax: `Tags = (NameOfTag1, NameOfTag2)`.

## The Query Builder

The **Query Builder** button is located on the top right of the **Tests Explorer** area, next to the search bar. It can be used to find the desired test case based on certain criteria.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/search/query-builder-button.png" alt="query button" width="60%">

You might also find this Query Builder function while working with test suites, for example, in a Dynamic Test Suite. See also: [Dynamic Test Suite](https://docs.katalon.com/katalon-studio/docs/create-test-suite.html#dynamic-test-suite-dynamic-test-cases-list).

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/search/query-builder.png" alt="query in dynamic test suite" width="100%">

To use the **Query Builder** function, click on the **Query Builder** button. The **Query Builder** dialog appears. Input your search criteria, then click **Search**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/search/query-builder-dialog.png" alt="query dialog" width="70%">

The Query Builder menu include:

- **ID**: to search the exact IDs of the test artifact
- **Name**: to search by the name of the test artifact
- **Description**: to search by the description associated with the test artifact
- **Comment**: to search by the comments attached to the test artifacts
- **Tag**: to search by the tag linked to the test artifacts

> Notes:
>
> * Every field in this Query Builder mode can be applied to search for all types of test artifacts such as test cases, test suites, folders, etc.
> * You can only search for only one tag name at a time. The same process applies to getting descriptions and comment keywords.

## Basic Search For Dynamic Test Suite Plugin

You can also use the Basic Search For Dynamic Test Suite plugin to search in a Dynamic Test Suite. This plugin is available on Katalon Store: [Basic Search For Dynamic Test Suite Plugin](https://store.katalon.com/product/2/Basic-Search-For-Dynamic-Test-Suite).

To learn more about how to use this plugin, see [Basic Search For Dynamic Test Suite](https://docs.katalon.com/katalon-studio/docs/basic-search-for-dynamic-querying-test-suite.html).

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/search/search-plugins.png" alt="search plugin" width="100%">
