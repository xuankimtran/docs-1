---
title: "Dynamic Test Suite"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-recorder/docs/dynamic-test-suite.html
description:
---

> Requirements:
> Katalon Recorder version 5.6.0 onwards. 

With Dynamic Test Suites, you can add multiple test cases at run time via a search query. It allows users to execute test cases with certain tags dynamically.

In this article, we show you how to categorize test cases with tags and execute them in a dynamic test suite.

## Categorize Test Cases with Tags

   > Notes:
   >
   > A tag can be reused across test cases, but you can not have a duplicated tag in a test case.
   
### Categorize test cases with Tags Management

The **Tags Management** function allows you to manage all tags in one place. You can add/remove or edit tags in one or many selected test cases. 

Follow these steps:

1. In the **Actions** panel, click **Tags Management**. The **Tags Management** dialog opens.
   
2. In the opened dialog, the first interface shows you a list of existing tags and the number of test cases where the tags are present. If you have no tags, this page should be blank.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/dynamic-test-suite/KR-DYNAMIC-List-of-existing-tags.png" width="70%" alt="List of existing tags">

   - To add new tags, click **Add new tag**. The opened interface allows you to add new tags to one or many selected test cases. You can also add tags to all test cases in a test suite.

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/dynamic-test-suite/KR-DYNAMIC-Add-new-tag.png" width="70%" alt="Add new tags from tags management">
         
      - Input the new tag name, then click **Save** to add tags to selected test cases.

         <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/dynamic-test-suite/KR-DYNAMIC-Add-tags-from-tags-management.png" width="70%" alt="Add new tags from tags management">

      - After adding tags, the tag icon is highlighted in the sidebar for this test case.

         <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/dynamic-test-suite/KR-DYNAMIC-Highlighted-tag-icon-after-adding-tags.png" width="70%" alt="Tags icon highlighted after adding tags">

   - To remove tags, click *Remove* (Trash icon) of the tag you wish to remove. Katalon Recorder deletes it from all test cases. 

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/dynamic-test-suite/KR-DYNAMIC-Remove-the-tag.png" width="70%" alt="Remove tags in all test cases">

   - To edit tags, click *Edit* (Pencil icon) of the tag you wish to edit. After editing the tags, click **Save**. The edited tag is replaced in all test cases. 

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/dynamic-test-suite/KR-DYNAMIC-Edit-tags.png" width="70%" alt="Edit tags in all test cases">

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/dynamic-test-suite/KS-DYNAMIC-Click-save-to-edit.png" width="70%" alt="Save edited tags">

      > Notes:
      > 
      > If you uncheck the test case while editing the tag, the edited tag will be removed completely from the test case. 
      > In the above example, when changing the tag name from `Dashboard` to `Calculator`, if you uncheck the **Test case 01** test case, there will be no tags named `Dashboard` or `Calculator` in this test case.

### Categorize test cases from test case view

You can also add tags directly to a test case. To do so, open the desired test case. Click **Add new tag** in the test case header, then manually input the tag name or select an existing tag in the dropdown list.

   <img src="https://github.com/katalon-studio/docs-images/raw/b8e6cfa9512728f2d1c7b99e7336bafe19089a20/katalon-recorder/docs/dynamic-test-suite/KR-DYNAMIC-Add-new-tags-from-test-case%202.png" width="70%" alt="Add tags from test case view">

### Categorize test cases from the Workspace sidebar
   
To quickly add new tags from the **Workspace** sidebar, click **Tags** <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/dynamic-test-suite/KR-DYNAMIC-Tag-icon.png" width="1.8%" alt="Tag icon">. A pop-up **Tag this test case** dialog allows you to manually input the tag name or select an existing tag in the dropdown list.
   
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/dynamic-test-suite/KR-DYNAMIC-Add-tags-from-the-workspace-sidebar.png" width="70%" alt="Add tags from the Workspace sidebar">

## Execute Dynamic Test Suite containing Categorized Test Cases

After categorizing your test cases with tags, you can now execute them in a dynamic test suite. 

### Create a new Dynamic Test Suite

To quickly create a new Dynamic Test Suite, click on a tag from the **Workspace** sidebar or the test case view.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/dynamic-test-suite/KR-DYNAMIC-Click-a-tag-from-the-workspace-sidebar.png" width="70%" alt="Click a tag from the workspace sidebar">

An **Execute test case** dialog opens, showing all test cases of the selected tag.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/dynamic-test-suite/KR-DYNAMIC-an-execute-test-case-dialog.png" width="70%" alt="An execute test case dialog opens">

Alternatively, you can also click *Add* (+) in the **Dynamic Test Suite** section from the **Workspace** sidebar to create a new Dynamic Test Suite.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/dynamic-test-suite/KR-dynamic-Create-Dynamic-Test-Suite-manually.png" width="70%" alt="Create a new dynamic test suite manually">

### Add categorized test cases into a Dynamic Test Suite

To add categorized test cases into a Dynamic Test Suite, select or type the tags of the desired test cases in the **Input tags** box. Each tag is separated by a comma. Then click **Apply** to query out the matching test cases.

For example: To add the test cases with the `aTag_1` and `atag_2` tags into the dynamic test suite, you can click on the `aTag_1` and `atag_2` tags or input `aTag_1,atag_2` into the **Input tags** box, then click **Apply**. Katalon Recorder will query out the matching test cases.

<img src="https://user-images.githubusercontent.com/16775806/138648208-d277f8e4-145f-47af-8a84-7076abb92ac1.gif" width="70%" alt="Results after searching query">

### Run the Dynamic Test Suite

After selecting test cases, click **Execute** in the **Execute test case** dialog to create and execute the dynamic test suite with the specified query.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/dynamic-test-suite/KR-DYNAMIC-execute-a-dynamic-test-suite.png" width="70%" alt="Execute the dynamic test suite">

If you are running the test suite from the dynamic test suite view, click **Play** instead.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/dynamic-test-suite/KR-DYNAMIC-click-play.png" width="70%" alt="Click play in the test suite view">

After executing the test suite, you can check the status of your test in the **Log** tab. 

> Notes:
> 
> For real-time monitoring and better reporting capabilities, consider integrating your project with Katalon TestOps. To learn more about TestOps integration, you can refer to this document: [View execution reports in TestOps](https://docs.katalon.com/katalon-recorder/docs/monitor-scenario-executions.html#login-to-testops).
