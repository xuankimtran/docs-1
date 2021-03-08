---
title: "Katalon TestOps Terminology"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/testops-terminology.html
redirect_from:
---

## Release

Represents a version or a milestone of a software product, which consists of one or more **Test Cases**.  

**Usage**

Manages your test cases and testing progress by milestone. With Katalon TestOps Release, you can view the overall performance and readiness of the software product to be deployed with confidence.

> Releases can be managed in **Test Planning** section.      

**Example**                                                                          

![](https://raw.githubusercontent.com/katalon-studio/docs-images/master/katalon-analytics/docs/release/release-list.png) 


## Build

Represents a version of a software product, which the development team hands over to the testing team for testing purposes. A build also consists of one or more **Test Cases**.  

**Usage**

This feature strengthens collaboration among developers and testers. Hence, you can manage product readiness efficiently and seamlessly. 

> **Build** list can be viewed and managed on **Releases** detailed page.      

**Example**                                                                          

![](https://raw.githubusercontent.com/katalon-studio/docs-images/testops-new/katalon-analytics/docs/build/build-list.png) 


## Test Run

Consists of one or more test case, depending on whether it is conducted parallelly, to be scheduled or executed.

**Usage**

Gives you the related information of running Test Cases.  A Test Run will keep track of the test result, when the test was ran, Test Run status, duration, assignee, etc. 

> Test Runs can be planned in **Test Planning** section.
>
> After being executed, you can view their results in **Reports & Analytics** section.                                                                            

**Examples**

![](https://raw.githubusercontent.com/katalon-studio/docs-images/master/katalon-analytics/docs/view-reports-overview/report-test-run.png)

![](https://raw.githubusercontent.com/katalon-studio/docs-images/master/katalon-analytics/docs/kt-scheduler/test-run-detail.png)


## Trigger

By when the Test Run should be executed. (A Trigger can be an Event (e.g. from Github or Jira), or a time interval).   

**Usage**

**Katalon TestOps** provides you an ability to determine when the Test Run is executed so that you can actively plan your testing procedure.
                 
**Example**

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-terminology/trigger.png)

## Test Environment

In what machines the Test Run should be executed. If a Test Environment is a local machine, it has to be controlled by an Agent.           

**Usage**

Used to execute test cases along with Script Repository after being configured. **Katalon TestOps** allows you to create a Test Environment with the following options:
- Your local machine
- Kubernetes environment
- CircleCI environment

> Test Environments can be managed in **Configurations** section.

**Example**

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-terminology/test-environment.png)



## Script Repository

Stores the actual test automation scripts to be executed.                           

**Usage**

Gives you a space to manage all test scripts and decide which one to be executed along with the given Test Environment. In **Katalon TestOps**, Script Repository can be a Git repository or a ZIP file. 

> Script Repository can be managed in **Configurations** section.                    

**Example**

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-terminology/script-repository.png)                                           


## Test Run Type

A collection of Test Runs having the same configurations.  

**Usage**

Gives you an ability to view the list of Test Run with similar configurations (Test Environment, Trigger, Script Repository) so that you can better manage your Test Runs.

> You can find Test Run Types in **Test Planning** section.   

**Example**

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-terminology/test-run-type.png)   


## Test Session

Being created once a Test Run is executed. Each Test Run can be executed as one or many Test Sessions depending on whether it is conducted parellely. 

**Usage**

Gives you information after executing a subset of the overall Test Run. In **Katalon TestOps**, each Test Session contains:
- One or more Test Cases
- Test Environment and test scripts in Script Repository used for the execution of each Test Case 

**Example**                                                                          

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-terminology/test-session.png) 


## Test Result

A result of a Test Case after being executed.                                                                                                                             
**Usage**

Gives you detailed results after a Test Case is executed from **Katalon Studio** (or other apps). Usually, Test Results are organized into one or more Test Suites and can link to one or more Defects to track bugs and failures.

> To view Test Result, in **Reports & Analytics**, go to Test Runs > select one Test Run to view details. Here you can view all details of the Test Case after being executed.  

**Example**

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-terminology/test-result.png)

## Defect

Represents a Jira Issue linked to a (failed) Test Run in **Katalon TestOps**.                                                                                       

**Usage**

Gives you an oveview of performance of Test Runs by Jira issue so that you can have full control and awareness of any problem for better test maintenance.

> You can find Defects in **Test Management** section.
>
> Learn how to link Test Runs to Jira Defects [here](https://docs.katalon.com/katalon-analytics/docs/ka-defects.html).

**Example**

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-terminology/defect.png)



## Assertion

A statement that a predicate (Boolean-valued function, a true–false expression) is expected to always be true at that point in the code. Assertion is the validation step that determines whether the automated Test Case succeeded or not.

**Usage**

**Katalon TestOps** provides you a specific view of Assertions in each Test Case. This used to evaluate the quality of Test Case and ensure that your application is working correctly by checking whether a condition is true, i.e., whether labels, data, API responses, etc., are rendered correctly.

> Assertion statistics of each Test Case are displayed in the list of Test Cases from **Test Management**.
>
> To view details of Assertions, in **Reports & Analytics**, go to Test Runs > select a Test Run to view details. Here you can view the list of Assertions with status, errors and logs.

**Example**

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-terminology/assertion.png)                                                                                        
## Requirement

Represents a Jira Issue linked to a Test Case in **Katalon TestOps**.                

**Usage**

Gives you an oveview of performance of Test Cases by Jira issue so that you can oversee the Test Case quality for better test performance. 

> Requirements can be managed in **Test Management** section.

**Example**

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-terminology/requirement.png) 


## Test Case

Has multiple Test Results, usually when the Test Case is a data-driven one. A Test Case can link to one or more Requirements.

**Usage**

Ensures if different features within an application are working as expected. **Katalon TestOps** provides you detailed information of Test Cases that helps your team validate if the software is free of defects and if it is working as per your expectations. You can also link Test Cases to Jira Requirements to ensure good test coverage.

> You can find Test Cases in **Test Management** section.

**Example** 

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-terminology/test-case.png)                                    


## Test Suite

A collection of Test Cases.                      

**Usage**

Organizes Test Cases for better management and maintenance.

> You can find Test Suites in **Test Management** section.

**Example**

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-terminology/test-suite.png)                                  
