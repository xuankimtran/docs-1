---
title: "Global variables"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-recorder/docs/global-variables.html
description:
---

In test automation, sometimes multiple test cases might require the same values. Instead of manually duplicating the same set of values across multiple test cases, you can create global variables to reuse same values across test cases. This saves time and reduces maintenance efforts as projects increase in complexity. From version 5.6.0 onwards, Katalon Recorder introduces global variables to help you automate tests with ease.

Global variables are cross-compatible with Katalon Studio when migrating your projects.

## Create an Execution Profile

Global variables are defined within an artifact called Execution Profiles. Creating an Execution Profile allows you to save which global variables apply to which workflow. These Profiles can be migrated to Katalon Studio (KS) along with your projects.

Follow these steps:

1. Open Katalon Recorder.
2. On the left sidebar, go to **Profiles** and click on the **+** button next to it to create a new Execution Profile.

    <img src="link to be confirmed"  width=100% alt="kr ui create execution profile">
    
3. Right click on the newly-created Execution Profile and select **Set as default Execution Profile**.

Repeat the steps to create multiple Execution Profiles.

> Notes: 
>
> * You must set one Execution Profile as default.
> * You cannot delete a default Execution Profile. To delete it, you have to set another Execution Profile as default.

## Set global variables

Follow these steps:

1. Open Katalon Recorder and select your test case.

2. Copy the values you want to use as global variables (e.g., username and password).

3. On the left sidebar, go to **Profiles**, then select the **Execution Profile** you have set as default.

    The **Execution Profile** screen appears.

4. Click **Add**, then paste the values in the **Name** and **Default value** sections.

5. Go to the test cases you want to implement global variables in.

6. Insert the syntax `${GlobalVariables.name}` in which *name* represents the specified global variable (e.g., `${GlobalVariables.username}`).  

You can now run the tests without inputting the same sets of values for every test.

If you want to change the global variables in your test cases, you must create a new Execution Profile and set it as default Execution Profile, then repeat the steps above to add the new set of values to your test cases.