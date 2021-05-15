---
title: "What's new in v5.4?"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-recorder/docs/whats-new.html
description:
toc: true
---
In this update, we've focused on removing barriers that may prevent users from adopting Katalon Recorder, reducing efforts to get familiar with the essential features, making data-driven execution obvious, and improving the editing experience.

## A fault-tolerant editing experience
If you spend a lot of time editing tests, you may have once or twice modified a test to the point where it no longer works, and then forgot how you got there. In this release, we've introduced undo/redo mechanism to make the editing experience more fault-tolerant. You can now explore different ways of arranging test steps, their commands, targets, and values without worrying about messing up your test case.

The undo/redo mechanism applies for editing operations such as: adding, deleting, moving, copy/pasting test steps, and modifying commands, targets values. There is a 100-operations limit that you should keep in mind.

Currently, the scope of undo/redo mechanism is limited to one test case only. When you switch to a different test case, the changes made to the previous test case will persist. There is also a 100-operations limit that you should keep in mind.

## New Product Tours
From talking to our users, we know that people use KR for many different purposes, from filling in employee information to making sure that your website stays up and the crucial paths are exercised. 

Generally, there are two broad use cases: automating repetitive tasks and automated testing, to which more specific use cases belong. The product tours guide users through the essential and distinguishing features for each use case. Whether you're new or already using the product, these product tours may contain surprising & helpful information.

The product tours are automatically visible to new users and are accessible for current users through the app's toolbar.

## New data-driven execution example
Regardless of the use case, data-driven execution capability is useful for many purposes. For automated testing, you can test the log-in flow of your website against a set of usernames and passwords to ensure your validation logic work robustly. For automating repetitive tasks, you can fill in employee information by executing an automated scenario against a prepared data set.

Data-driven execution is already simple in Katalon Recorder, in this release we've made the simplicity obvious. When you launch the new Product Tours, a sample test suite and data file will be loaded into the application. You can view the sample test case to see how data-driven works, and apply it to your own tests.

## Improved registration & log-in process
We have streamlined the registration & log-in process by integrating it into the application. On successful registrations, users will be taken to the log-in screen immediately. After verifying the validity of the email, users can log in to start experiencing the product in its full capacity.

Users are strongly encouraged to sign up for a free Katalon account to get access to regular product updates and upcoming advanced features. However, it's important to experience the values of the product first before investing further efforts. From 5.3.36, users can try out Katalon Recorder without an account, but a reminder will appear after every test execution for unregistered users.

## Tidbits
Mac users can now use both CTRL and CMD in hotkeys. Previously it was limited to Ctrl which may not be intuitive to some users. Users can also initiate undo/redo with hotkeys (ctrl/cmd + z and ctrl/cmd + y).

We fixed an issue where passed/failed statuses below the Test Explorer get erased when users stop or pause an execution.