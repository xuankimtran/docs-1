---
title: "What's new in v5.4?"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-recorder/docs/whats-new.html
description:
toc: true
---

**May 17, 2021**

With this update, discovering the essential features of Katalon Recorder has never been easier. New users can now find and use the functions that matter to them more quickly, removing existing barriers to adoption. We’ve also made data-driven execution more visible, and improved the editing experience by making it more forgiving.
 
## A more fault-tolerant editing experience with undo/redo
If you spend a lot of time editing tests, you may have once or twice modified a test to the point where it no longer works. If so, you’re not alone - this experience is, unfortunately, a common source of frustration for KR users.  With this update, you can now undo and redo instantly, reducing frictions and making the editing experience  much more forgiving. You can now explore different ways of arranging test steps, their commands, targets, and values without worrying about messing up your test case.
 
The undo/redo mechanism applies for a large range of editing operations, such as adding, deleting, moving, or copy/pasting test steps, as well as modifying commands , targets and values.


![](https://raw.githubusercontent.com/katalon-studio/docs-images/master/katalon-recorder/docs/whats-new/5.4.0/undo-redo.gif)

Currently, the undo/redo mechanism is limited to whichever test case you are currently editing. All changes will be made permanent if you switch to a different test case. There is also a 100-operations limit that you should keep in mind.

## New Product Tours
Over the years, we've always loved to learn about the many ways you have come to use KR, from filling in employee information to making sure that your website stays up, and that important functions such as registration or purchasing work properly.
 
Generally speaking, we’ve found that KR is used to either automate repetitive tasks, or to perform automated testing. The product tours guide you through both workflows, highlighting the core features most suitable to your purpose. If you're new, these product tours contain helpful tips to get you started - but even a seasoned KR user might find surprising new information on features they had not considered using.

![](https://raw.githubusercontent.com/katalon-studio/docs-images/master/katalon-recorder/docs/whats-new/5.4.0/kr-product-tours.gif)

The product tours are automatically visible to new users. If you’re already a KR user, you can find and initiate them through the app’s toolbar.

## New data-driven execution example
Regardless of your main reason for using KR,  data-driven execution capabilities are useful for many purposes. For automated testing, you can test the log-in flow of your website against a set of usernames and passwords to ensure your validation logic works robustly. For automating repetitive tasks, you can for example fill in employee information by executing an automated scenario against a prepared data set.
 
Data-driven execution is already simple in Katalon Recorder, but this release puts a spotlight on that simplicity. When you launch the new Product Tours, a sample test suite and data file will be loaded into the application. You can then directly view the sample test case to see how data-driven execution works, and apply it to your own tests.

## Improved registration & log-in process
We have streamlined the registration & log-in process by integrating it into the application. On successful registrations, users will be taken to the log-in screen immediately. After verifying the validity of their email, users can log in to start experiencing the product in its full capacity.

![](https://raw.githubusercontent.com/katalon-studio/docs-images/master/katalon-recorder/docs/whats-new/5.4.0/improved-registration-signup-process.png)

Users are strongly encouraged to sign up for a free Katalon account to get access to regular product updates and upcoming advanced features. However, we recognize that it’s important to first see if this product is the right solution for you. Starting with version 5.3.36, users can now try out Katalon Recorder without an account, and an option to register will appear after every test execution.

## Quality of life upgrades
- Mac users can now use both CTRL and CMD in hotkeys. Previously they were limited to CTRL which wasn’t intuitive to some users. Additionally, users can also initiate undo/redo with hotkeys (ctrl/cmd + z and ctrl/cmd + y).
- We added **Save test case as** and **Save test suite as** options to the context menu.
 
## Bug Fixes
- We fixed an issue where passed/failed statuses below the Test Explorer got erased when users cancelled or paused an execution.