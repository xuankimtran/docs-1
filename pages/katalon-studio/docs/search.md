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

Searching manually for test artifacts can be time-consuming. The Query Builder in Katalon Studio helps reduce time spent on searching for the desired test artifacts, based on given criteria.

The search function is used for test artifacts such as test cases, test suites, and folders.

There are three ways to use the Search function in Katalon Studio: input your search criteria directly in the Search bar, use the **Advanced Search** button or use the **Query Builder** function.

This article shows you how to view basic information of an object and how to use the search function in Katalon Studio.

## IDs and Properties

IDs and tags can be helpful when it comes to managing large projects. You can use IDs and tags to find test artifacts in the Search function.
### How to get a test artifact ID?

To get the ID of a test artifact, do as follows:

Navigate to **Tests Explorer** and find the test artifact that you want to get the ID of. Right-click on that test artifact and select **Copy ID**. The ID is now copied to your clipboard. Then, you can paste that ID into the ID text box.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/search/copy-ID.png" alt="copy ID" width="60%">

### View test artifact properties

You can find the ID, name, description, and tag of a test artifact in the **Properties** view.

Navigate to **Tests Explorer**. Right-click on that test artifact and select **Properties**. The **Properties** dialog appears.

> Notes:
>
> You cannot view the properties of a folder.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/search/tc-properties.png" alt="test case properties" alt="60%">

## The search bar

Another way to search for test artifacts is to type in the search bar located at the top of the **Test Explorer** section. You can type in a specific keyword, or follow this syntax: `id=(Your_Test_Case_ID)`. For example:

`id=(Test Cases/Common Test Cases)`

All test cases associated with the `Test Cases/Common Test Cases` ID are filtered and returned.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/search/search-bar.png" alt="search bar" width="60%">

## Advanced search

The **Advanced search** function allows you to find the desired test artifacts based on certain criteria.
From Katalon Studio version 8.2.5, the **Advanced search** button is located on the top right of the **Tests Explorer** area, next to the search bar.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/search/KS-SEARCH-Advanced-search-button.png" alt="Advanced search button" width="60%">

You can also access to this function in **Actions > Advanced search**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/search/KS-SEARCH-Access-advanced-search-function.png" alt="Access to the Advanced search function" width="30%">

To use the **Advanced search** function, click on the **Advanced search** button. The **Search** dialog appears. Input your search criteria, then click **Search**.

Katalon will query out all the matching test artifacts in the **Search** tab as shown in the following picture:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/search/KS-SEARCH-Search-results.png" alt="The search result" width="100%">

## The Query Builder

The **Query Builder** function allows you find the desired test cases based on certain criteria.
You can find the Query Builder function while working with test suites, for example, in a Dynamic Test Suite. See also: [Dynamic Test Suite](https://docs.katalon.com/katalon-studio/docs/dynamic-test-suite-ks.html).

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/search/query-builder.png" alt="query in dynamic test suite" width="100%">

To use the **Query Builder** function, click on the **Query Builder** button. The **Query Builder** dialog appears. Input your search criteria, then click **Search**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/search/query-builder-dialog.png" alt="query dialog" width="70%">

The Query Builder menu includes:

- **ID**: to search the exact IDs of the test artifact
- **Name**: to search by the name of the test artifact
- **Description**: to search by the description associated with the test artifact
- **Comment**: to search by the comments attached to the test artifacts
- **Tag**: to search by the tag linked to the test artifacts

> Notes:
>
> * Every field in this Query Builder mode can be applied to search for all types of test artifacts such as test cases, test suites, folders, etc.
> * You can only search for one keyword at a time when searching by tag, description, or comment.

## Basic Search For Dynamic Test Suite plugin

You can also use the **Basic Search For Dynamic Test Suite** plugin to search in a dynamic test suite. This plugin is available on the Katalon Store: [Basic Search For Dynamic Test Suite Plugin](https://store.katalon.com/product/2/Basic-Search-For-Dynamic-Test-Suite).

To learn more about how to use this plugin, see [Basic Search For Dynamic Test Suite](https://docs.katalon.com/katalon-studio/docs/basic-search-for-dynamic-querying-test-suite.html).

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/search/search-plugins.png" alt="search plugin" width="100%">
