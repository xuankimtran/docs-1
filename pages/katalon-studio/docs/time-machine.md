---
title: "Time Machine" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/time-machine.html 
---

Currently, users have to manually reproduce the state of AUT in order to fix a broken Test Object, which is time-consuming. In data-driven test cases with multiple test data, reproducing manually on the exact combination of test data is complicated. To reduce reproduction efforts, we capture the state of the AUT when tests fail due to locators not finding elements (aka broken Test Object). To encourage users adopt this feature, we add links to Log Viewer and Test Suite Report that automatically opens Spy Tool at the captured page. As a solution, Time machine is introduced in Katalon Studio 7.7.5 (Currently a Beta release). 

**Requirement**: Katalon Studio version 7.7.5 onwards

## Time Machine 

Time machine captures the state of the AUT automatically when tests fail due to broken Test Objects and add links that open up Spy Tool at the captured page to Test Suite Report and Log Viewer.

When re-capturing the broken object on the time snapshot with Spy Tool, users can 

## Usage Examples

### Failed Test Case execution scenario

**Given** a test case execution fails due to broken locators.

**When** users click on the Test Case row in Log Viewer.

**Then**:

* Users should see a link: “Click here to fix broken Test Object”.
* Clicking on the link opens the Spy Tool at the captured state of the AUT.
* Trigger the Given Prerequisites of Fix broken test objects scenarios

### Failed Test Suite execution scenario

**Given** a Test Suite execution contains at least one Test Case that fails due to broken locators.

**When** users view the Test Suite report.

**Then**:

* Users should see link “Open in Spy Tool”.
* Clicking on the link opens the Spy Tool at the captured state of the AUT.
* Trigger the Given Prerequisites of Fix broken test objects scenarios


