---
title: "Global variables"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-recorder/docs/global-variables.html
description:
---

In test automation, sometimes multiple test cases might require a same set of values. Instead of manually duplicating the same set of values across multiple test cases, you can create global variables to reuse same values across test cases. This would save time and reduce maintenance efforts.

Global variables are a set of pre-defined values that are accessible across all test cases. From version 5.6.0 onwards, Katalon Recorder introduces this feature to help you automate tests with ease.

Implementing global variables in Katalon Recorder would then allow the migration process from Katalon Recorder to Katalon Studio to become easier for you.

## Create an Execution Profile

In Katalon Studio (KS), global variables are defined within an artifact called **Execution Profiles**. From version 5.6.0 onwards, you can create an Execution Profile in Katalon Recorder for global variables settings and migration to KS.

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

5. Go to the test cases you want to implement global variables.

6. Insert the syntax `${GlobalVariables.name}` in which *name* represents the specified global variable (e.g., `${GlobalVariables.username}`).  

Now you run the tests without the need to input the same set of values (e.g., username and password) across all tests.

If you want to change the global variables in your test cases, you must create a new Execution Profile and set it as default Execution Profile, then repeat the steps above to add the new set of values to your test cases.