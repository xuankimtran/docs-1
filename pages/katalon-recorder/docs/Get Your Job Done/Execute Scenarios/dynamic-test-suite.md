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

2. The test case view: 

   <img src="url" width="70%" alt="Add tags from test case view">

3. The **Workspace** sidebar:

   <img src="url" width="70%" alt="Add tags from test case view">

   > Note:
   > 
   > In the **Workspace** sidebar, you can quickly add tags into all test cases in a test suite by click **Tags** <img src="url" width="30%" alt="Tag icon"> in the test suite.
## Execute Dynamic Test Suite

After catergorizing your test cases with tags, you can now execute them in a dynamic test suite. 
### Create a new Dynamic Test Suite

To quickly create a new Dynamic Test Suite, from the **Workspace** sidebar or the test case view, click on a tag. An **Execute test case** dialog opens, showing all test cases of the selected tag.

<img src="url" width="70%" alt="Click a a tag from the workspace sidebar">

<img src="url" width="70%" alt="A execute test case dialog opens">

Alternatively, from the **Workspace** sidebar, you can right-click on **Test Suite > New Dynamic Test Suite** to create a new Dynamic Test Suite.

<img src="url" width="70%" alt="Create a new dynamic test suite manually">

### Add tags into a Dynamic Test Suite

To add tags into a Dynamic Test Suite, select or type desired tags to include them in the **Query** box. Each tag is seperated by *Comma*(,). Then click **Apply** to query out the matching test cases.

For example: To add the test cases with the `tag_1` and `tag_2` tags into the dynamic test suite, you can click on the `tag_1` and `tag_2` tags or input `tag_1,tag_2` into the **Query** box, then click **Apply**. The matching test case appears in the test suite.

<img src="url" width="70%" alt="Results after searching query">

### Run the Dynamic Test Suite

Click **Execute** to create and execute the dynamic test suite with the specified query.

<img src="url" width="70%" alt="Execute the dynamic test suite">

After executing the test suite, you can check the status of your test in the **Log** tab. 

> Notes:
> 
> For real-time monitoring and better reporting capabilities, consider integrating your project with Katalon TestOps. To learn more about TestOps intergration, you can refer to this document: [View execution reports in TestOps](https://docs.katalon.com/katalon-recorder/docs/monitor-scenario-executions.html#login-to-testops).
