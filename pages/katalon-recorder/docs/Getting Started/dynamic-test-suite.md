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

There are three possible ways to manage your test case tags:

  1. From the **Test case** view: 
    This function allows you to add/remove tags in one test case. Follow these steps:
       - Open the desired test case.
       - To add new tags, click **Add new tag** in the opened test case. A pop-up dialog alows you to input tags into the test case. Click **Save**.
       - To remove tags, click **Remove (X)** in the tag box.

            <img src="url" width="70%" alt="Add tags from test case view">

  2. From the **Workspace** panel:
    This functions allows you to add/remove tags in one test case. Follow these steps:
       - In the **Workspace** panel, navigate to the desired test case.
       - To add new tags, click **Tags** <img src="url" width="30%" alt="Tag icon"> in the desired test case. A pop-up dialog alows you to input tags into the test case. 

            <img src="url" width="70%" alt="Add tags from test case view">

            > Note:
            > 
            > You can quickly add tags into all test cases in a test suite by click **Tags** <img src="url" width="30%" alt="Tag icon"> in the test suite.

  3. From the **Tags Management**:
    This functions allows you to add/remove tags in one or many selected test cases. Follow these steps:
       - In the **Actions** panel, click **Tags Management**. The **Tags Management** dialog opens.
       - In the opened dialog, you can see a list of existing tags along with the number of test cases where the tags present. 

            <img src="url" width="70%" alt="List of existing tags">

       - To add new tags, click **Add new tag**. The opened interface allows you to add new tags into one or many selected test cases.

            <img src="url" width="70%" alt="Add tags into selected test cases from tags management">

       - You can also add tags into all test cases in a test suite.
            
            <img src="url" width="70%" alt="Add tags into all test case in a test suite from tags management">

       - To remove tags, click **Remove (X)** in the tag box. Katalon Recorder will remove the tags from all test cases. 

            <img src="url" width="70%" alt="Remove tags in all test cases">

## Execute Dynamic Test Suite 

  1. Use one of three options in Part 1 to add tags into your test case.
  2. In the **Workshop** panel, right-click on **Test Suite > New Dynamic Test Suite**.
  3. To add test cases via search query, input the the query `tags=(tags1,tags2,tags3)` into the **Query** box. Then hit **What?** to query out the matching test cases.

    To learn more about the search query function, you can refer to this document: [Search test cases](https://docs.katalon.com/katalon-studio/docs/search.html).   

    For example: To add the test cases with the `Caculator` and `Dashboard` tags into this dynamic test suite, you can input `tags=(Caculator,Dashboard)` into the **Query** box. The matched test case appears in the test suite.

       <img src="url" width="70%" alt="Results after searching query">

  4. Hit **What?** to execute the test suite.
