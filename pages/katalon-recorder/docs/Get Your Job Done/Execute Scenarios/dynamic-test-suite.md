---
title: "Dynamic Test Suite"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-recorder/docs/dynamic-test-suite.html
description:
---

> Requirements:
> Katalon Recorder version 5.6.0 onwards. 

Dynamic Test Suite is a test suite with multiple test cases added at run time via a search query. This allows users to dynamically execute test cases with certain tags.

In this article, we show you how to catergorize test cases with tags and execute them in a dynamic test suite.

## Catergorize Test Cases with Tags

Katalon Recorder offers three possible ways to catergorize your test cases with tags. You can do it from:

1. The **Tags Management** function:  
   This function allows you to manage all tags in one place. You can add/remove or edit tags in one or many selected test cases. 

   Follow these steps:

     1. In the **Actions** panel, click **Tags Management**. The **Tags Management** dialog opens.
     2. In the opened dialog, the first inteface shows you a list of existing tags along with the number of test cases where the tags present. If you have no tags, this page should be blank.
         <img src="url" width="70%" alt="List of existing tags">

      - To add new tags, click **Add new tag**. The opened interface allows you to add new tags into one or many selected test cases. You can also add tags into all test cases in a test suite.

         <img src="url" width="70%" alt="Add tags into selected test cases from tags management">

         <img src="url" width="70%" alt="Add tags into all test case in a test suite from tags management">

         <img src="url" width="70%" alt="Tags icon highlighted after adding tags">

      - To remove tags, click *Remove* (x) in the tag you wish to remove. Katalon Recorder deletes it from all test cases. 

         <img src="url" width="70%" alt="Remove tags in all test cases">

      - To edit tags, click on the tag you wish to edit. The edited tag is replaced in all test cases. 

         <img src="url" width="70%" alt="Edit tags in all test cases">

2. The **Test case** view:

   <img src="url" width="70%" alt="Add tags from test case view">

3. The **Workspace** sidebar:

   <img src="url" width="70%" alt="Add tags from test case view">

   > Note:
   > 
   > In the **Workspace** sidebar, you can quickly add tags into all test cases in a test suite by click **Tags** <img src="url" width="30%" alt="Tag icon"> in the test suite.
## Execute Dynamic Test Suite

After catergorizing your test cases with tags, you can now execute them in a dynamic test suite.
### Execute a Dynamic Test Suite directly from tags

1. From the **Workspace** sidebar, click **Tags** <img src="url" width="30%" alt="Tag icon"> of the test case you wish to add in a Dynamic Test Suite. 
   
   <img src="url" width="70%" alt="Click the tag from the test case panel">

2. An **Execute test case** dialog appears, showing all test cases that have selected tags from step 1.
   
   <img src="url" width="70%" alt="Click the tag from the test case panel">

In case you want to add more tags, select or types desired tags to include them in the **Query** box. Each tag is seperated by `,`. For example: `tag_1,tag_2`.

3. Click **Execute** to create and execute a dynamic test suite with the specified query.

### Execute a Dynamic Test Suite from Test Suite view

1. In the **Workshop** sidebar, right-click on **Test Suite > New Dynamic Test Suite** to create a new Dynamic Test Suite.

2. To add associated test cases via search query, click or manually input tags name into the **Query** box. Then click **Apply** to query out the matching test cases.
   
   For example: To add the test cases with the `Calculator` and `Dashboard` tags into this dynamic test suite, you can input `Caculator,Dashboard` into the **Query** box. The matching test case appears in the test suite.

   <img src="url" width="70%" alt="Results after searching query">

3. Hit **Play** to execute the test suite.
4. After executing the test suite, you can check the status of you test in the **Log** tab. 