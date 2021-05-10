---
title: "What's new in v8.0.0?" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/new/what-is-new-800.html
redirect_from:
    - "/katalon-studio/new/what-is-new.html"
    - "/katalon-studio/new/what-is-new/"
    - "/katalon-studio/new/"
    - "/display/KD/Release+Notes/"
    - "/display/KD/Release%20Notes/"
description: What's new in Katalon Studio 8.0.0?
---

**May 10, 2021**

Katalon Studio 8.0.0 is now released with Azure Test Plans's native integration and robust IDE performance for processing large projects.

> Download [here](https://www.katalon.com/download/).

In this update, we've focused on scalability and interoperability across projects and tools so you can have a cohesive experience in creating and executing automated tests. We are on a mission to help software team achieve continuous testing; hence, incorporating Katalon Studio into your SDLC & DevOps with ease and greater security is our top priority.

This version offered teams using Azure DevOps Services one more native integration - Azure Test Plans for monitoring quality. Katalon Studio indeed plays a quality gate in your CI/CD pipeline. Furthermore, 8.0.0 packaged Edge Chromium as the default embedded browser in Katalon Studio IDE to improve the IDE performance, resolved security vulnerabilities, and drove the development towards Open-Source Software Compliance. And as usual - a ton of tidbits are also packed in this version (see [release notes](https://docs.katalon.com/katalon-studio/new/version-8x.html)). Let’s take a look at the most exciting features and changes that have been offered.

## Continuous Testing with Azure Test Plans Integration

A need for Continuous Testing is inevitable to companies adopting Continuous Integration. Integrating Katalon Studio into their SDLC & DevOps, in particular, the Azure DevOps, is our mission: letting Katalon Studio play an automatic quality gate. That ultimately serves the purpose of helping you achieve continuous testing.

Picture this: In the morning, you open your **Azure Test Plans** and already seen there the results of your **Pipeline** run last night. There is one red test outcome while the rest is green, you click on it, and you see an error message. To see what happened, what caused your test case to fail, you open the test run attachment where you can find a test report in HTML (because you like HTML) and an execution log. You want to make sure your test case failed because it found a bug, not because it's not good enough. You open the linked test case in Katalon Studio just to make sure your script is qualified. After a little while of debugging, you rerun your test script, and it passes. And you're confident that tomorrow it won't happen again. 8.0.0 further increases the interoperability between Katalon Studio and Azure DevOps Services. The desired workflow is as follows:

* Clone and contribute to a project from Azure Repos through Katalon's built-in Git Integration
* Associate automated tests in Katalon with manual test cases in Azure Test Plans
* Run Katalon tests in Azure Pipelines
* On Azure Test Plans, view test results sent by Katalon Studio. You're equipped with test logs and reports for troubleshooting. [Learn more](https://docs.katalon.com/katalon-studio/docs/azure-devops-test-plans.html)

## Opening large Projects much faster

We believe a scaling need should have a scaling solution. In v8.0.0, it no longer takes forever to open test projects with hundreds of custom keywords.

When your business grows, your team's testing demand increases to ensure software quality. Whether the test automation needs to cover more new features, or you have more types of applications to test (for instance, before you only need to test Web, now your company launches a mobile app), there comes very often our users tend to store all the tests in one test project. Some projects even have up to thousands of test files. Whenever you open a test project, it takes you half an hour or more. And you get frustrated as a result and feel like you're wasting your time. The Katalon team totally understands your frustration. In this version, we are happy to let you know: For the second time to open the project, loading time is reduced by 60%.

You may know that Katalon Studio stores custom keywords in individual files. Every time you open a test project, Katalon Studio needs to parse and compile the custom keywords in one file for your usage. We made an improvement here: we cache the keywords for later working sessions. What we need from you is a little patience for the first time.

## Reusing Desired Capabilities across projects

Katalon Studio supports defining Desired Capabilities in a project to add extra browsers and device properties for Web UI, Mobile, Windows, remote testing. If desired capabilities need to be used across projects, you have to manually re-define them in a project. Yet it's not quite an easy job, and it's buggy as well. Hence, by allowing importing/exporting desired capabilities across projects, Katalon Studio reduces manual effort and helps you reuse the configurations faster and less error-prone. [Learn more](https://docs.katalon.com/katalon-studio/docs/import-export-desired-capabilities.html)

Together with [private plugins](https://docs.katalon.com/katalon-studio/docs/kse-use-plugins.html#private-plugins) and [sharing test artifacts](https://docs.katalon.com/katalon-studio/docs/import-export-test-artifact.html), sharing desired capabilities introduced in 8.0.0 completes the feature set of reusing test data in Katalon Studio. An ability to reuse common resources definitely boosts your team's performance since it eases collaboration and increases the efficiency of the whole team. Your team no longer has to repeat tedious manual settings time after time.

## Brand new Product Tours for new Web UI and Web Service users

## Tidbits

* Edge Chromium became the default embedded browser in Katalon Studio IDE: Before 8.0.0, Internet Explorer is the default embedded browser in Katalon Studio, which have caused multiple issues, for instance, failure to render variable editors of test case & request object; or failure to submit a bug to the integrated Jira project. Enabled by the Eclipse platform upgraded in v7.9, we can replace Internet Explorer with Edge Chromium to resolve those issues.
* Newly supported browser versions: Chrome 90; Support Microsoft Edge (Chromium) 90.
* Maximizing Katalon Runtime Engine License Usage by an ability to enforce releasing the license used for the previous session through a command option: `-licenseRelease`.
