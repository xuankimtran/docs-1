---
title: "Test Case Management With Tags" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/test-case-management-with-tags.html

description: 
---

To manage test cases better in Katalon Studio, you can manipulate tag properties by utilizing the existing tag values. With the **Test Case Management with Tags** plugin, you can view all tags in the project and save time by appending existing tags to test cases.

This document shows you how to append and manage tags, search for test cases with multiple tags, and execute test cases with specific tags in console mode.

## Test Case Management with Tags Plugin

To append and manage tags, first, install our plugin from the Katalon Store: [Test Case Management with Tags](https://store.katalon.com/product/6/Test-Case-Management-with-Tags).

Then, open Katalon Studio and select **Your Account > Reload Plugins**. For detailed instructions, see [Reload Plugins](https://docs.katalon.com/katalon-store/docs/user/access-store-in-KS.html#reload-plugins).

## Append and Manage Tags

### Add Tags to a test case

You can add tags to a test case when you first create a test case. To learn more about how to create a test case, see [Create Test Case](https://docs.katalon.com/katalon-studio/docs/create-test-case.html).

Another way to add tags to a test case is using the **Properties** tab. Do as follows:

1. Open your desired test case.
2. Switch to the **Properties** tab. In this tab, you can find detailed information of a test case, including all tags.

3. Input your tag values, separate them by commas or semi-colons.

    To remove a tag, delete it from the tag field.

    <img class="pop" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-case-management-with-tags/tag.png" alt="properties tab" width="100%">

    <p align="center"><i>Click on the image to enlarge it</i></p>

### Append Tags

You can view all tags in your project and append tags to a test case. After installing the **Test Case Management with Tags** plugin, follow these instructions:

1. Open a test case and switch to the **Properties** tab. 

    Under the **Tag** field, you can find the **Append tags** button. If this button does not appear, ensure you already installed this plugin: [Test Case Management with Tags](https://store.katalon.com/product/6/Test-Case-Management-with-Tags).

2. Click on the **Append** button. The **Append Tags** dialog appears with a list of all tags in your project.

3. You can search for any tag and select tags from the list to add to the current test case.

    Click on the check box to select. Since this feature is for appending tags to a test case, you cannot uncheck a tag that already exists in that test case.

3. Click **Append** when you are done. New tags are now added to your test case.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-case-management-with-tags/append-tags.png" alt="append tags dialog" width="50%">


## Search For Test Cases With Multiple Tags

After you successfully install Test Case Management With Tags plugin, in a Dynamic Querying Test Suite, you can search for test cases with multiple tags using the **Query Provider**.

To search for test artifacts labeled with multiple tags, do as follows:

1. Open a dynamic test suite. See also: [Dynamic Test Suite (Dynamic Test Cases List)](https://docs.katalon.com/katalon-studio/docs/create-test-suite.html#dynamic-test-suite-dynamic-test-cases-list).
2. Directly type on the **Query** box follow this syntax: `tag=(NameOfTag1,NameOfTag2)`. For example: `tag=(may,december)`.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-case-management-with-tags/query.png" alt="query box" width="100%">

## Execute Test Cases With Certain Tags in Console Mode

In console mode, you can filter and execute test cases attached with certain tags. Make sure you already have installed the **Test Case Management with Tags** plugin.

In your command, add this argument:

 `-testCaseTags="<tag1>,<tag2>"`

> Learn more about how to run a test in console mode with Katalon Runtime Engine at [Command Syntax (Command-line/Console Mode Execution)](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html).

When you execute a test in the terminal, you can see the process where test cases are filtered before executing. For example:

```
----------------- TEST CASE TAGS PLUGIN START FILTERING -----------------
Test Cases/Main Test Cases/TC1_Verify Successful Login is a test case to be run
Test Cases/Main Test Cases/TC2_Verify Successful Appointment is filtered out 
Test Cases/Main Test Cases/TC3_Visual Testing Example is a test case to be run
----------------- TEST CASE TAGS PLUGIN FINISH FILTERING -----------------
```
