---
title: "Test Case Management With Tags" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/test-case-management-with-tags.html

description: 
---

To manage test cases better in Katalon Studio, you can manipulate tag properties by utilizing the existing tag values. With the **Test Case Management with Tags** plugin, you can view all tags in the project and save time by appending existing tags to test cases.

This document shows you how to append and manage tags, search for test cases with multiple tags, and execute test cases with specific tags in console mode.

## Test Case Management with Tags Plugin

To append and manage tags, first install our plugin from the Katalon Store: [Test Case Management with Tags](https://store.katalon.com/product/6/Test-Case-Management-with-Tags).

Then, open Katalon Studio and select **Your Account > Reload Plugins**. For detailed instructions, see [Reload Plugins](https://docs.katalon.com/katalon-store/docs/user/access-store-in-KS.html#reload-plugins).

## Append and Manage Tags

### Add Tags to a test case

You can add tags to a test case when you first create a test case. To learn more about how to create a test case, see [Create Test Case](https://docs.katalon.com/katalon-studio/docs/create-test-case.html).

You can also add tags to a test case using the **Properties** tab. Do as follows:

1. Open your desired test case.
2. Switch to the **Properties** tab. In this tab, you can find more details on a test case, including associated tags.

3. Input your tag values, separate them by commas or semi-colons.

    To remove a tag, delete it from the tag field.

    <img class="pop" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-case-management-with-tags/tag.png" alt="properties tab" width="100%">

    <p align="center"><i>Click on the image to enlarge it</i></p>

### Append Tags

You can view all tags in your project and append tags to a test case. After installing the **Test Case Management with Tags** plugin, follow these instructions:

1. Open a test case and switch to the **Properties** tab. 

    Under the **Tag** field, you can find the **Append tags** button.

2. Click on the **Append** button. The **Append Tags** dialog appears with a list of all tags in your project.

3. Search for and select tags you wish to add to the current test case.

    > Notes:
    >
    > Tags previously added to this test case already display as selected, and cannot be deselected.

4. Click **Append** when you are done. New tags are now added to your test case.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-case-management-with-tags/append-tags.png" alt="append tags dialog" width="50%">

## Search For Test Cases With Multiple Tags

After you successfully install the Test Case Management With Tags plugin, in a Dynamic Querying Test Suite, you can search for test cases with multiple tags using the **Query Provider**.

To search for test artifacts labeled with multiple tags, do as follows:

1. Open a dynamic test suite. See also: [Dynamic Test Suite (Dynamic Test Cases List)](https://docs.katalon.com/katalon-studio/docs/create-test-suite.html#dynamic-test-suite-dynamic-test-cases-list).
2. Directly type in the **Query** box following this syntax: `tag=(NameOfTag1,NameOfTag2)`. For example: `tag=(may,december)`.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-case-management-with-tags/query.png" alt="query box" width="100%">

## Execute Test Cases With Specific Tags in Console Mode

> Requirements:
>
> * An active Katalon Runtime Engine license
> * The Test Case Management with Tags plugin installed

In console mode, you can filter and execute test cases attached with certain tags.

In your command, add this argument:

 `-testCaseTags="<tag1>,<tag2>"`

> Learn more about how to run tests in console mode with Katalon Runtime Engine at [Command Syntax (Command-line/Console Mode Execution)](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html).

When you execute a test in the terminal, you can see the process where test cases are filtered before executing. For example:

TC1_Verify Successful Login is associated with these tags: jan,apr
TC2_Verify Successful Appointment is associated with these tags: jan,feb,mar
TC3_Visual Testing Example is associated with these tags: jan,feb

In the command, you add this argument: `testCaseTags="jan,feb"`.

The execution log should look like this:

```
----------------- TEST CASE TAGS PLUGIN START FILTERING -----------------
Test Cases/Main Test Cases/TC1_Verify Successful Login is filtered out 
Test Cases/Main Test Cases/TC2_Verify Successful Appointment is a test case to be run
Test Cases/Main Test Cases/TC3_Visual Testing Example is a test case to be run
----------------- TEST CASE TAGS PLUGIN FINISH FILTERING -----------------
```
