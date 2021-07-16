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

> 8.0.5 is now available!
> 
> * Download [here](https://www.katalon.com/download/).
> * See [release notes](https://docs.katalon.com/katalon-studio/new/version-8x.html)

**May 10, 2021**

Katalon Studio 8.0.0 was released with Azure Test Plans's native integration and robust IDE performance for processing large projects.

In this update, we've focused on scalability and interoperability across projects and tools so you can have a cohesive experience in creating and executing automated tests. We are on a mission to help software team achieve continuous testing; hence, incorporating Katalon Studio into your SDLC & DevOps with ease and greater security is our top priority.

This version offered teams using [Azure DevOps Services](https://azure.microsoft.com/en-in/services/devops/) one more native integration - [Azure Test Plans](https://azure.microsoft.com/en-in/services/devops/test-plans/) for monitoring quality. Katalon Studio indeed plays a quality gate in your CI/CD pipeline. 

Furthermore, 8.0.0 packaged Edge Chromium as the default embedded browser in Katalon Studio IDE to improve the IDE performance, resolved security vulnerabilities, and drove the development towards Open-Source Software Compliance. And as usual - a ton of tidbits are also packed in this version (see [release notes](https://docs.katalon.com/katalon-studio/new/version-8x.html)). Let’s take a look at the most exciting features and changes that have been offered.

## Continuous Testing with Azure Test Plans Integration

A need for Continuous Testing is inevitable to companies adopting Continuous Integration. Integrating Katalon Studio into your Azure DevOps workflow ultimately serves the purpose of helping you achieve continuous testing.

8.0.0 further increases the interoperability between Katalon Studio and Azure DevOps Services with the following desired workflow:

* Contribute to a project cloned from Azure Repos through Katalon's built-in Git Integration. [Learn more](https://docs.katalon.com/katalon-studio/docs/git-integration.html)
* Associate automated tests in Katalon with manual test cases in Azure Test Plans. [Learn more](https://docs.katalon.com/katalon-studio/docs/azure-devops-test-plans.html)
* Run Katalon tests in Azure Pipelines. [Learn more](https://docs.katalon.com/katalon-studio/docs/azure-devops-extension.html)
* On Azure Test Plans, view test results sent by Katalon Studio.

<img alt="Azure DevOps and Katalon Studio" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/whatsnew800/interoperability.png" width=100%>

Picture this: In the morning, you open your **Azure Test Plans** and already seen there the results of your **Pipeline** run last night. There is one red test outcome while the rest is green. What does it means? It means either there’s a bug found in your software build or in the failed test case itself.

What will you do?

Normally, you will start investigating to see what happened, what caused your test case to fail. With this integration, you're equipped with test logs and reports sent by Katalon Studio for troubleshooting.

## Opening large Projects much faster

We believe a scaling need should have a scaling solution. For the second time to open a project with hundreds of custom keywords, loading time is reduced by 60% in 8.0.0.

You may know that Katalon Studio stores custom keywords in individual files. Every time you open a test project, Katalon Studio needs to parse every single custom keyword, which means the more custom keywords a project stores, the longer it takes to finish opening that project. We made an improvement here: we cache the keywords parsing result. What we need from you is a little patience for the first time.

## Reusing Desired Capabilities across projects

Katalon Studio supports defining Desired Capabilities in a project to add extra browsers and device properties for Web UI, Mobile, Windows, remote testing. If desired capabilities need to be used across projects, you have to manually re-define them in a project. Yet it's not quite an easy job, and it's buggy as well. Hence, by allowing importing/exporting desired capabilities across projects, Katalon Studio reduces manual effort and helps you reuse the configurations faster and less error-prone. [Learn more](https://docs.katalon.com/katalon-studio/docs/import-export-desired-capabilities.html)

<img alt="Reusing Desired Capabilities" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/whatsnew800/import-export-desired-cap.gif" width=100%>

Together with [private plugins](https://docs.katalon.com/katalon-studio/docs/kse-use-plugins.html#private-plugins) and [sharing test artifacts](https://docs.katalon.com/katalon-studio/docs/import-export-test-artifact.html), sharing desired capabilities introduced in 8.0.0 completes the feature set of reusing test data in Katalon Studio. An ability to reuse common resources definitely boosts your team's performance since it eases collaboration and increases the efficiency of the whole team. Your team no longer has to repeat tedious manual settings time after time.

## Brand new Product Tours for new Web UI and Web Service users

Picking up a new skill is hard, and test automation is not an exception. Often our new users feel overwhelmed with what's offered in the tool. We feel you. That's why from v8.0.0 onwards, users using Katalon Studio for the first time can enjoy two product walkthroughs with Web and Web Service testing.

<img alt="Katalon Studio Walkthroughs" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/whatsnew800/walkthroughs.png" width=100%>

## Tidbits

* Edge Chromium became the default embedded browser in Katalon Studio IDE: Before 8.0.0, Internet Explorer is the default embedded browser in Katalon Studio, which have caused multiple issues, for instance, failure to render variable editors of test case & request object; or failure to submit a bug to the integrated Jira project. Enabled by the Eclipse platform upgraded in v7.9, we can replace Internet Explorer with Edge Chromium to resolve those issues.
* Newly supported browser versions: Chrome 90, Microsoft Edge (Chromium) 90, Firefox 88.
* Maximizing Katalon Runtime Engine License Usage by an ability to enforce releasing the license used for the previous session through a command option: `-licenseRelease`.
