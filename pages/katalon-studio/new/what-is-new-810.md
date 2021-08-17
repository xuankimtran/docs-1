---
title: "What's new in v8.1.0?" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/new/what-is-new-810.html
redirect_from:
    - "/katalon-studio/new/what-is-new.html"
    - "/katalon-studio/new/what-is-new/"
    - "/katalon-studio/new/"
    - "/display/KD/Release+Notes/"
    - "/display/KD/Release%20Notes/"
description: What's new in Katalon Studio 8.1.0?
---
**August 18th, 2021**

We are excited to announce Katalon Studio version 8.1.0 is now available for download from the [Katalon website](https://www.katalon.com/download/).

Version 8.1.0 is a major release packed with features and enhancements aimed to INSERT VALUE PROP/MAIN THEME HERE. We significantly improved the Retry Immediately mechanism to better detect and overcome test flakiness. To lower your testing environment costs, we've also introduced a new functionality: you can now configure a maximum number of test failures to automatically end poorly performing test executions early. 

Version 8.1.0 is a major release focused on improving the Retry Immediately mechanism and allowing users to stop execution based on the maximum number of test failures permitted in a single run. While the former assists users in detecting test flakiness, the latter considerably reduces the time spent waiting for the entire execution to complete, resulting in lower testing environment costs. We've also worked on a better experience in mobile testing, and enhanced integration with Azure DevOps.

Along with these major changes, we've also made adjustments to our UI on macOS Big Sur, as well as to Report and 3rd-party integration that you should check out. See our [Release Notes](https://docs.katalon.com/katalon-studio/new/version-8x.html) for details on the modifications made to previous versions. Read on to find out more detailed information on the new features and improvements we've prepared for you.

## Tackling test flakiness with Effective Retry Immediately mechanism 

A flaky test is a test that occasionally fails but finally passes if you attempt it enough times. It lowers test confidence and, as a result, trust is eroded. It not only irritates stakeholders, developers, and testers but also causes everyone to question the process. As a consequence, flakiness becomes an outgoing problem that needs to be tackled. Addressing this issue requires testers and developers to identify which and why tests are flaky and then remedy them accordingly.

The first step to combat test flakiness is to identify it. In version 8.1.0, we've addressed this by applying a new logic to our *Retry Failed Executions Immediately* function. The changed function now consolidates retried test case execution logs into one report, so you can identify flaky tests at a glance. Wonder how it works? See [Retry Failed Execution Immediately](https://docs.katalon.com/katalon-studio/docs/test-suite.html#retry-failed-executions-immediately).

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-suite/Gif.gif" width=90% alt="how retry immeidately works gif">

## Terminating Execution Conditionally

Many users believe in a fail-fast system while running tests. In other words, the shorter your feedback loop, the faster you move forward. Furthermore, if your team uses cloud devices, computers, or cloud services, test run times have a clear cost. Cutting test runs short when a significant number of tests fail, and detecting test environment issues early can mean a lot of saved time and money.

This is especially true with a mature set of tests, which can take hours to execute to completion. By creating a condition to automatically end tests early when a high number of tests fail, you can eliminate failures with a clear root cause, such as failures related to test configuration, setup, infrastructure, or network, without the wasted hours... and potential frustration. 

> **Note**
>
> For individuals who don't want to miss any issues discovered in a single run, this feature may not be compelling. It hinders the test execution from identifying more issues.

We are happy to announce you can kiss those hours of wasted waiting goodbye. From version 8.1.0 onwards, Katalon Studio introduced the utility to terminate execution conditionally by defining the failures threshold via the command line. See [Terminate Execution Conditionally](https://docs.katalon.com/katalon-studio/docs/terminate-execution-conditionally.html) for more details.

**Configure in Command Builder**

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/condition-to-stop/Cmd%20builder%20UC%201.png" width=90% alt="configure number of test failures">

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/condition-to-stop/command%20UC%201.png" width=90% alt="execute with the configured number of test failures">

**Execute in Console Mode**

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/condition-to-stop/execution%20log%20UC%201.png" width=90% alt="execute in console mode">

## Improving Mobile testing

### Better Kobiton Integration

When it comes to mobile testing, integration between Kobiton and Katalon Studio serves as an essential chain to execute automated tests from Katalon Studio on Kobiton devices. This was made easier in version 8.1.0: you can now customize the remote server protocol and device name in Kobiton for a clearer testing experience. See [Mobile testing with Kobiton devices](https://docs.katalon.com/katalon-studio/docs/integrate_with_kobiton.html).

### New built-in keyword for conditional waiting

Conditional waiting keywords is a modern solution that goes beyond Record-and-playback. It has proven to be a reliable, must-have feature for low-code automation testing tools. Conditional waiting ensure scripts do not blindly wait x number of seconds before continuing to the next step; instead, they wait until a condition is true and proceed as soon as possible. This drastically cuts down on the execution time of the testing suite while also preventing flaky tests. In version 8.1.0, we continue to expand our keyword vocabulary with `waitForElementNotPresent` for Mobile testing. See [[Mobile] Wait For Element Not Present](https://docs.katalon.com/katalon-studio/docs/mobile-wait-for-element-not-present.html).

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-wait-for-element-not-present/mobile-wait-for-element-not-present.png" width=90% alt="add mobile wait for element not present in manual view">

## Tidbits

### Newly supported browser versions

Chrome 92 and Microsoft Edge (Chromium) 92.

### Azure DevOps enhancement - Submit Release Information together with Test Run

We know that teams sometimes juggle multiple pipelines for different jobs. This can make obtaining reports of an automated test that still reflect the specific job and its quality a challenge. Currently, Azure Test Plans enables users to view the quality of a build or a release, while Katalon Studio already provides build information to Azure DevOps. With version 8.1.0 onwards, users can now also submit the release information with their test run, including Release Version and Release Stage. See [Configure the Integration with Azure DevOps Test Plans](https://docs.katalon.com/katalon-studio/docs/azure-devops-test-plans.html#configure-the-integration).

### New APIs for Plugin platform

In version 8.1.0, Katalon Studio provided [a list of new APIs](https://github.com/katalon-studio/katalon-studio-platform/blob/master/docs/turorials/apilist.md) to offer resources for [building integration plugins](https://github.com/katalon-studio/katalon-studio-platform/blob/master/docs/turorials/create-your-first-plugin.md). These APIs are allocated to plugins that have access to the:
- JRE location
- Running mode (IDE or Katalon Runtime Engine)
- Test Suite/ Test Suite Collection JUnit report location (via the plugin platform)