---
title: "Create your first test"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-recorder/docs/automate-scenarios.html
description:
---

Broadly speaking, there are usually two steps to create an automate scenario in Katalon Recorder:
1. Add commands to interact with websites
2. Add verify or assert commands to make sure your test case follows the correct flow.

## Add commands to interact with websites
To get started, use the Recorder to automatically create a test case:
- Click on the **Record** button.
- Switch to the currently active tab.
- Start interacting with your website.
- Switch to Katalon Recorder.
- Click the **Stop** button.

You should see your interactions are recorded as a test case.

## Add verify or assert commands
There are two ways to add verify or assert commands.

### After the recording of a test case
If you just have just recorded a test case:
- Add a new test step through the toolbar item.
- Type `verify` or `assert` in the Command field of the new test step.
- Choose from the list of available suggested commands (for example `verifyElementPresent`).
- Click on the button **Select a target element for the current command** located next to the Target field of the new test step.
- Switch to the currently active tab.
- Select an element on the page.
- Switch back to Katalon Recorder.

You should see the newly created assert or verify command for the target element.

### During the recording of a test case
If you are recording a test case:
- Right-click on the target element.
- Choose a command from the context menu item *Katalon Recorder (Selenium tests generator)*.


