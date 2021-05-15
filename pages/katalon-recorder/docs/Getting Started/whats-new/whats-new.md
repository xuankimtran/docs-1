---
title: "What's new"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-recorder/docs/whats-new.html
description:
toc: false
---
# What's new in 5.3.36

In this update, we've focused on removing barriers that may prevent users from adopting Katalon Recorder, reducing efforts to get familiar with the essential features, making data-driven execution obvious, and improving the editing experience.

## New Product Tours
From talking to our users, we know that people use KR for many different purposes, from filling in employee information to making sure that your website stays up and the crucial paths are exercised. 

Generally, there are two broad use cases: automating repetitive tasks and automated testing, to which more specific use cases belong. The product tours guide users through the essential and distinguishing features for each use case.

Whether you're new or already using the product, these product tours may contain surprising & helpful information. If you want to introduce KR to other people, these product tours help newcomers adopt the tool easier.

The product tours are automatically introduced to new users and are available to current users through the toolbar.

## New data-driven execution example
Regardless of the use cases, data-driven execution capability is useful. For test engineers, you can test the log-in flow of your website against a set of usernames and passwords to ensure your validation logic work in different circumstances. For less technical users, you can fill in employee or patient information by executing an automated scenario against the prepared data set.

Data-driven execution is already simple in Katalon Recorder, in this release we make the simplicity obvious. When you launch the new Product Tours, a sample test suite and data file will be loaded into the application. You can view the second sample test case to see how data-driven works in Katalon Recorder.

## A fault-tolerant editing experience
If you spend a lot of time editing tests, you may have once or twice modified a test to the point where it no longer works, and then forgot how you got there. In this release, we've introduced undo/redo mechanism to make the editing experience more fault-tolerant. You can now explore different ways of arranging test steps, their commands, targets, and values without worrying about messing up your test case.


## Improved registration & log-in process
We have streamlined the registration & log-in process by integrating it into the application. On successful registrations, users will be taken to the log-in screen immediately. After verifying the validity of the email, users can log in to start experiencing the product in its full capacity.

Users are strongly encouraged to sign up for a free Katalon account to get access to regular product updates and upcoming advanced features. However, it's important to experience the values of the product first before investing further efforts. From 5.3.36, users can try out Katalon Recorder without an account, but a reminder will appear after every test execution for unregistered users.

## Tidbits
Mac users can now use both CTRL and CMD in hotkeys. Previously it was limited to Ctrl which may not be intuitive to some users. Users can also initiate undo/redo with hotkeys (ctrl/cmd + z and ctrl/cmd + y).

We fixed an issue where passed/failed statuses below the Test Explorer get erased when users stop or pause an execution.