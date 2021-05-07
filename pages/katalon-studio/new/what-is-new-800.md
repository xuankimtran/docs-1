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

Furthermore, 8.0.0 packaged abc to improve ... , resolved vulnerabilities and as usual - a ton of tidbits are also packed in this release (see [release notes](/katalon-studio/new/version-8x.html)). Let’s take a look at the most interesting features and changes that have been offered.

## Continuous Testing with Azure Test Plans Integration 

Companies using Azure DevOps to manage product requirements, store source code, CI/CD pipeline and create test plan.

leverage integration with Azure DevOps Pipeline

Help users achieve Continuous testing by playing automatic quality gates

Integrating Katalon Studio into their SDLC & DevOps

fit into your current tool ecosystem 
increase compatibility

Optimize our users' Continuous Testing - Continuous Delivery by further enhancing Katalon Studio's integration with other tools: Katalon TestOps and Azure DevOps.

we support test case association between two systems and automation test status submission from Studio to Azure DevOps. This native integration benefits those companies using Katalon Studio with Azure Pipelines and Azure Test Plans the most.

[Learn more](/katalon-studio/docs/azure-devops-test-plans.html)

## Opening large Projects much faster

Custom keywords has always been loved by our users. 

On your business's scaling, a test project is scaling as a result. 

Improve Performance of Scaling Projects

Picture this

a growing project is challenging

boost the efficiency

We believe a scaling need should have a scaling solution. In v800, it no longer takes forever to open a test projects with hundreds custom keywords.

Enable project scalability by improving the IDE's performance on large projects and optimize memory consumption during execution

Improve Performance: Load large projects faster and consume less memory during execution

## Reusing Desired Capabilities across projects

Increase the efficiency by reducing cost in terms of time, resources, multiple tool usage. For instance, reduce time spent in each stage of testops.

Currently, Katalon Studio supports defining Desired Capabilities in a project to add extra browsers and device properties for Web UI, Mobile, Windows, remote testing. If desired capabilities need to be used across projects, users have to manually re-define them again in a project in use. Hence, by allowing importing/exporting desired capabilities across projects, Katalon Studio reduces manual effort and helps users reuse the configurations faster and less error-prone.

Currently, Katalon Studio supports defining Desired Capabilities in a project to add extra browsers and device properties for Web UI, Mobile, Windows, remote testing. If desired capabilities need to be used across projects, users have to manually re-define them again in a project in use.

Allowing importing/exporting desired capabilities across projects, Katalon Studio reduces manual effort and helps users reuse the configurations faster and less error-prone.

[Learn more](/katalon-studio/docs/import-export-desired-capabilities.html)

## Maximizing your License Usage

Katalon Runtime Engine License
Add a parameter to release the previous execution session before checking license. [Learn more](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#general-options)

## Brand new Product Tours for new Web UI and Web Service users

emoving frictions during the on-boarding process

## Enhancing Katalon TestOps Integration

TestOps Integration Enhancement
New Build concept: TestOps Build
[Test Suite based parallel execution] Query for Test Suite Collection

## Tidbits

* Resolving Security Vulnerabilities in SonarQube for Static Code Analysis
* Open-source license compliance
* Replacing IE with Edge Chromium as the default embedded browser: Before 8.0.0, Internet Explorer is the default embedded browser in Katalon Studio, which causes multiple issues, for instance, failure to render variable editors of test case & request object; or failure to submit a bug to the integrated Jira project. Enabled by the Eclipse platform upgraded in v7.9, we can replace Internet Explorer with Edge Chromium as the default embedded browser to resolve the issues mentioned earlier.
* Newly supported browser versions: Support Chrome 90.; Support Microsoft Edge (Chromium) 90.

