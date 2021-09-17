---
title: "Dynamic Test Suite"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-recorder/docs/dynamic-test-suite.html
description:
---

> Requirements:
> Katalon Recorder version 5.6.0 onwards. 

Dynamic Test Suite is a test suite with multiple test cases added at run time via a search query. This allows users to dynamically execute test cases with certain tags, names or properties.

In this article, we demonstrate how to manage test case tags and execute them in a dynamic test suite.

## Manage Test Case Tags

The **Tags Management** functions allows you to manage all tags in one place. With this functions, you can:
- Add/remove tags in one or many selected test cases. 
- Edit tags in one or many selected test cases.

Follow these steps:

1. In the **Actions** panel, click **Tags Management**. The **Tags Management** dialog opens.
2. In the opened dialog, you can see a list of existing tags along with the number of test cases where the tags present. 
     <img src="url" width="70%" alt="List of existing tags">

     - To add new tags, click **Add new tag**. The opened interface allows you to add new tags into one or many selected test cases. You can also add tags into all test cases in a test suite.

     <img src="url" width="70%" alt="Add tags into selected test cases from tags management">

     <img src="url" width="70%" alt="Add tags into all test case in a test suite from tags management">

     - To remove tags, click **Remove (X)** in the tag you wish to remove. Katalon Recorder will delete it from all test cases. 

     <img src="url" width="70%" alt="Remove tags in all test cases">

     - To edit tags, click on the tag you wish to edit. Katalon Recorder will change it into a new tag in all test cases. 

     <img src="url" width="70%" alt="Remove tags in all test cases">

Moreover, you can also add/remove or edit tags from:
- The **Test case** view:

<img src="url" width="70%" alt="Add tags from test case view">

- The **Workspace** panel:

<img src="url" width="70%" alt="Add tags from test case view">

> Note:
> 
> In the **Workspace** panel, you can quickly add tags into all test cases in a test suite by click **Tags** <img src="url" width="30%" alt="Tag icon"> in the test suite.
## Execute Dynamic Test Suite

  1. Use one of three options in Part 1 to add tags into your test case.
  2. In the **Workshop** panel, right-click on **Test Suite > New Dynamic Test Suite**.
  3. To add test cases via search query, input the the query `tags=(tags1,tags2,tags3)` into the **Query** box. Then hit **What?** to query out the matching test cases.
   
     To learn more about the search query function, you can refer to this document: [Search test cases](https://docs.katalon.com/katalon-studio/docs/search.html).
   
     For example: To add the test cases with the `Caculator` and `Dashboard` tags into this dynamic test suite, you can input `tags=(Caculator,Dashboard)` into the **Query** box. The matching test case appears in the test suite.

     <img src="url" width="70%" alt="Results after searching query">

  4. Hit **What?** to execute the test suite.
  5. Do we have reports? Where to see the results?