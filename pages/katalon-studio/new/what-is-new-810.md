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

As ever, we are so excited to announce Katalon Studio version 8.1.0 is now available for download from the [Katalon website](https://www.katalon.com/download/).

Version 8.1.0 focused on improving the Retry Immediately mechanism and allowing users to stop execution based on the maximum number of test failures permitted in a single run. While the former assists users in overcoming test flakiness, the latter considerably reduces the time spent waiting for the entire execution to complete, resulting in lower testing environment costs. In addition, better experience in mobile testing and Azure DevOps integration was worth the wait in this major release.

Along with the exciting news, there were a few tidbits and changes about macOS Big Sur's UI and other 3rd-party integration that you should check out. See our [Release Notes](https://docs.katalon.com/katalon-studio/new/version-8x.html) for details on the modifications made to previous versions. Read on for the intriguing new features and improvements that we offered as below.

## Tackling test flakiness with Effective Retry Immediately mechanism 

A flaky test is a test that occasionally fails but finally passes if you attempt it enough times. It lowers test confidence and, as a result, trust is eroded. It not only irritates stakeholders, developers, and testers but also causes everyone to question the process. As a consequence, flakiness becomes an outgoing problem that needs to be tackled. Addressing this issue requires testers and developers to identify which and why tests are flaky and then remedy them accordingly.

As of being known, retrying a failed test is the first step to combat test flakiness since it will assist you in figuring out which test is problematic. Hence, in version 8.1.0, Katalon Studio applied new logic for *Retry Failed Executions Immediately Strateg*y and supports consolidating retried test case’s execution log and results into one report, which helps users easily detect flaky test cases at a glance. Wonder how it works? See [Retry Failed Execution Immediately](https://docs.katalon.com/katalon-studio/docs/test-suite.html#retry-failed-executions-immediately).

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-suite/Gif.gif" width=90%>

## Terminating Execution Conditionally

Many users believe in a fail-fast system while running tests - the shorter the feedback loop they get, the faster they move forward. Suppose a team uses cloud devices, computers, or cloud services, which costs dollars every minute. This practice helps detect test environment issues faster then saves test-related services, infrastructure, and also time and money.

Specifically, when a set of tests is mature, it takes hours to finish execution. But once a significant number of tests fail, they may fail for the exact cause. Possibly, the failures are related to test configuration, setup, infrastructure, or network. In this case, spending hours to finish the execution is not a wise choice as the root cause is already sufficient to take action.

From version 8.1.0 onwards, Katalon Studio introduced the utility to terminate execution conditionally by defining the failures threshold via the command line. This feature kisses hours of wasted waiting goodbye. See [Terminate Execution Conditionally](https://docs.katalon.com/katalon-studio/docs/terminate-execution-conditionally.html) for more details.

**Configure in Command Builder**

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/condition-to-stop/Cmd%20builder%20UC%201.png" width=90%>

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/condition-to-stop/command%20UC%201.png" width=90%>

**Execute in Console Mode**

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/condition-to-stop/execution%20log%20UC%201.png" width=90%>

## Improving Mobile testing

### Better Kobiton Integration

When it comes to mobile test automation, the integration between Kobition and Katalon Studio serves as an essential chain to execute Katalon Studio's automated tests on Kobiton's devices. From version 8.1.0 onwards, Katalon users can customize the remote server protocol and device name in Kobiton to better their testing experience. See [Mobile testing with Kobiton devices](https://docs.katalon.com/katalon-studio/docs/integrate_with_kobiton.html).

### New built-in keyword for conditional waiting

A must-have feature of a codeless automation testing tool called Conditional waiting (a modern approach comparing with Record-and-playback tools) has proved quite reliable. In this approach, scripts do not blindly wait *x* number of seconds before continuing to the next step; instead, they wait until a condition is true and proceed as soon as possible. This drastically cuts down on the execution time of the automation suite while also preventing flaky tests. Accordingly, in version 8.1.0, Katalon Studio introduced the keyword waitForElementNotPresent for Mobile testing, allowing users to set conditional waiting when executing the test script. See [[Mobile] Wait For Element Not Present](https://docs.katalon.com/katalon-studio/docs/mobile-wait-for-element-not-present.html).

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-wait-for-element-not-present/mobile-wait-for-element-not-present.png" width=90%>

## Tidbits

### Newly supported browser versions

Chrome 92 and Microsoft Edge (Chromium) 92.

### Azure DevOps enhancement - Submit Release Information together with Test Run

A team possibly has multiple pipelines for different jobs. A report of an automated test must reflect the job and its quality. Particularly, in Azure Test Plans, users can view the quality of a build or a release. Along with the build information that we already supported, from version 8.1.0 onwards, users can submit the release information (which Release and Release Stage) with the test run to ADO. See [Configure the Integration with Azure DevOps Test Plans](https://docs.katalon.com/katalon-studio/docs/azure-devops-test-plans.html#configure-the-integration).

### New APIs for Plugin platform

In version 8.1.0, Katalon Studio provided [a list of new APIs](https://github.com/katalon-studio/katalon-studio-platform/blob/master/docs/turorials/apilist.md) to offer resources for [building integration plugins](https://github.com/katalon-studio/katalon-studio-platform/blob/master/docs/turorials/create-your-first-plugin.md). These APIs are allocated to plugins that have access to the JRE location, Running mode (IDE or Katalon Runtime Engine), Test Suite/ Test Suite Collection JUnit report location via the plugin platform.