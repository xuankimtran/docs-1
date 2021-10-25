---
title: "Global variables"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-recorder/docs/global-variables.html
description:
---

In test automation, sometimes multiple test cases might require the same values. Instead of manually duplicating the same set of values across multiple test cases, you can create global variables to reuse same values across test cases. This saves time and reduces maintenance efforts as projects increase in complexity. From version 5.6.0 onwards, Katalon Recorder introduces **Global Variable Profile** feature to help you automate tests with ease.

This feature reduces syntax complication so that you can simply use global variables with just one click. 

Global variables are cross-compatible with Katalon Studio when migrating your projects.

## Global Variable Profile

Creating a Global Variable Profile allows you to save which global variables apply to which workflow. These Profiles can be migrated to Katalon Studio (KS) along with your projects.

Follow these steps:

1. Open Katalon Recorder.
2. On the left sidebar, go to **Global Variable Profile** and click on the **+** button next to it to create a new Global Variable Profile.
    
3. Right click on the newly-created Global Variable Profile and select **Set as default profile**.

Repeat the steps to create multiple Global Variable Profiles.

> Notes:
>
> * You must set one Global Variable Profile as default.
> * You cannot delete a default Global Variable Profile. To delete it, you have to set another Global Variable Profile as default.

## Add Global Variables

Follow these steps:

1. Go to **Global Variable Profile** and right-click on the profile.
2. Select **Use this in a test case**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/5.6.0-release/use-gv-in-test-case.png" width=100% alt="kr ui use gv in test case">

    The **Add global variables to test case** box pops up.
    
3. Follow the two steps in the popup box.

    * Step 1: Select the test case you want to add global variables to.

        <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/5.6.0-release/add-gv-step1.png" width=100% alt="kr ui use gv in test case">
        
    * Step 2: Check your test data and select its value.

        <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/5.6.0-release/add-gv-step2.png" width=100% alt="kr ui use gv in test case">

        > Notes:
        >
        > With Katalon Recorder 5.6.0, you can easily use a selected command without the need to know the syntax for implementing global variables in a test case.

You can now run the tests without inputting the same sets of values for every test.

## Replace Global Variables

You can replace a value with an existing Global Variable by following these steps:

1. Open Katalon Recorder and click on a test case.
2. Right click on a Test Case's value.

    You have two options: **Replace with an existing Global Variable** or **Create a new Global Variable**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/5.6.0-release/replace-existing-gv.png" width=100% alt="kr ui global variables">

3. Select **Replace with an existing Global Variable**.

    The **Replace with existing Global Variables** box pops up.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/5.6.0-release/replace-existing-gv-popup.png" width=100% alt="kr ui replace existing global variables">

4. Select the Global Variables from the dropdown list.

5. Click **Replace**.
