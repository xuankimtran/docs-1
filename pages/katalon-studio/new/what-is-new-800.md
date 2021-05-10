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

Katalon Studio 8.0.0 is now released with Azure Test Plans's native integration and robust IDE performance for processing large projects. Download [here](https://www.katalon.com/download/).

In this update, we've focused on scalability across test projects so you can have a cohesive experence on creating and executing automated tests. We are on a mission to help users achieve continuous testing; hence, incoporating Katalon Studio into your SDLC & DevOps with ease and greater security is our top priority.

This version offered teams using Azure DevOps Services one more native integration - Azure Test Plans for monitoring software quality. Katalon Studio truly plays a quality gate in your CI/CD pipeline.

Furthermore, 8.0.0 packaged Edge Chromium as the default embedded browser in Katalon Studio IDE to improve the IDE performance; resoved security vulnerabilities and comply to OSS .... And as usual - a ton of tidbits are also packed in this release (see [release notes](/katalon-studio/new/version-8x.html)). Let’s take a look at the most interesting features and changes that have been offered.

## Continuous Testing with Azure Test Plans Integration

Picture this: In the morning, you open your Azure Test Plans and already seen there: the results of your Pipeline run last night. There is one red test outcome while the rest is green, you click on it and you see an error message: abc. Then you open the test run attachment where you can find a test report in HTML (because you like HTML) and an execution log to see what has happened, what caused your test case to fail. Then you open the counterpart test case in Katalon Studio. After a little while debugging, you rerun your test script and it passes. Let's wait until tomorrow run to see if your whole suite passes.

Azure DevOps Services including 

A need for Continuous Testing is inevitable to companies adopting Continuous Integration. 
Integrating Katalon Studio into their SDLC & DevOps
Help users achieve Continuous testing by playing automatic quality gates

8.0.0 furthers increase the interoperability between Katalon Studio and Azure DevOps Services.

* Git Integration using Azure Repo 
* Associate automated tests in Katalon Studio with manual test cases in Azure Test Plans
* Run your test with Azure Pipeline

Companies using Azure DevOps to manage product requirements, store source code, CI/CD pipeline and create test plans.

Optimize our users' Continuous Testing - Continuous Delivery by further enhancing Katalon Studio's integration with other tools: Katalon TestOps and Azure DevOps.

we support test case association between two systems and automation test status submission from Studio to Azure DevOps. This native integration benefits those companies using Katalon Studio with Azure Pipelines and Azure Test Plans the most. [Learn more](/katalon-studio/docs/azure-devops-test-plans.html)

## Opening large Projects much faster

We believe a scaling need should have a scaling solution. In v8.0.0, it no longer takes forever to open a test projects with hundreds custom keywords.

When your business grows, your team's testing demand increases to ensure the software quality. Whether the test automation needs to cover more new features, or you have more types of application to test (before you only need to test Web, now your company launches a mobile app), there comes very often our users tend to store all the tests in one test project. Some projects even have up to thousands of test cases.

Before 8.0.0, it took you 2 to 3 minutes to open your test project. And you get frustrated as a result and feel like you're wasting you time. The Katalon team totally understands your frustration. In this version, we are happy to let you know: For the second time to open the project, loading time is reduced by 60%.

You may know that Katalon Studio stores all data: test cases, test suites, objects, keywords, and etc in individual files. Every time you open a test project in Katalon Studio, Katalon needs to parse and compile the custom keywords in one file. We made an improvement here: we cache the keywords for later working session. What we need from you is a little patience for the first time.

## Reusing Desired Capabilities across projects

Katalon Studio supports defining Desired Capabilities in a project to add extra browsers and device properties for Web UI, Mobile, Windows, remote testing. If desired capabilities need to be used across projects, users have to manually re-define them again in a project in use. Hence, by allowing importing/exporting desired capabilities across projects, Katalon Studio reduces manual effort and helps users reuse the configurations faster and less error-prone. [Learn more](/katalon-studio/docs/import-export-desired-capabilities.html)

Katalon Studio supports defining Desired Capabilities in a project to add extra browsers and device properties for Web UI, Mobile, Windows, remote testing. If desired capabilities need to be used across projects, you have to manually re-define them again in a project. Yet it's not quite an easy job and it's buggy as well.

Together with [private plugins] and [test artifacts export/import] including profiles, custom keywords, test cases, and test objects, sharing desired capabilities introduced in 8.0.0 completes the feature set of reusing test data in Katalon Studio. Abilities to reuse common resources is definitely boost your team performance since it eases the collaboration, and increase the efficiency of the whole team. Your team no longer have to repeat tedious manual settings time after time.

## Brand new Product Tours for new Web UI and Web Service users

emoving frictions during the on-boarding process

2 gifs

## Tidbits

* Replacing IE with Edge Chromium as the default embedded browser: Before 8.0.0, Internet Explorer is the default embedded browser in Katalon Studio, which causes multiple issues, for instance, failure to render variable editors of test case & request object; or failure to submit a bug to the integrated Jira project. Enabled by the Eclipse platform upgraded in v7.9, we can replace Internet Explorer with Edge Chromium as the default embedded browser to resolve the issues mentioned earlier.
* Newly supported browser versions: Support Chrome 90.; Support Microsoft Edge (Chromium) 90
* Enhancing Katalon TestOps Integration: New Build concept: TestOps Build and [Test Suite based parallel execution] Query for Test Suite Collection
* Maximizing your Katalon Runtime Engine License Usage: Add a parameter to release the previous execution session before checking license. [Learn more](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#general-options)