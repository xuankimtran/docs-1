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

    <img src="link to be confirmed"  width=100% alt="kr ui global variable profile">
    
3. Right click on the newly-created Global Variable Profile and select **Set as default profile**.

Repeat the steps to create multiple Global Variable Profiles.

> Notes:
>
> * You must set one Global Variable Profile as default.
> * You cannot delete a default Global Variable Profile. To delete it, you have to set another Global Variable Profile as default.

### Use global variables

Follow these steps:

1. Go to **Global Variable Profile** and right-click on the profile.
2. Select **Use this in a test case**.

    The **Add global variables to test case** box pops up.

    <img src="link to be confirmed"  width=100% alt="kr ui add global variables to test case popup">
3. Follow the two steps in the popup box.

    * Step 1: Select the test case you want to add global variables to.
    * Step 2: Check your test data and select its value.

        > Notes:
        >
        > With Katalon Recorder 5.6.0, you can easily use a selected command without the need to know the syntax for implementing global variables in a test case.

You can now run the tests without inputting the same sets of values for every test.

If you want to change the global variables in your test cases, set your preferred Global Variable Profile as default, right-click on the profile and select **Use this in a test case**, then repeat the steps above to add the new set of values to your test cases.
