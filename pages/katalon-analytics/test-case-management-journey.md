---
title: "Test Case Management"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/test-case-management.html
redirect_from:
---

Katalon TestOps represents test cases in a folder-based format to provide you with a clean look and well-structured information of your tests.

This document navigates you to where test cases are stored and how they are presented in Katalon TestOps to help you manage test cases effectively.

There are three options to upload your tests:

* Upload tests via Git Repositories (GitHub and Bitbucket). See: [Upload Test Scripts from a Git Repository](https://docs.katalon.com/katalon-analytics/docs/git-test-project.html).
* Upload tests via non-Git Repositories (as .zip file). See: [Upload Test Scripts to a Script Repository](https://docs.katalon.com/katalon-analytics/docs/code-repo.html).
* Upload JUnit and Katalon Studio's (KS) test data. See: [Upload JUnit and Katalon Studio Test Results to Katalon TestOps](https://docs.katalon.com/katalon-analytics/docs/testops-uploader.html).

Based on the option you select, read the relevant section below to find your tests cases and their execution data.

## View tests uploaded via Git Repositories

After uploading your test scripts from a Git Repository, go to **Test Management** > **Test Cases**.

The **Test Cases** page appears as below.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-dec-release-test-case-mgt/test-case-folder-info.png" width=100% alt="test case folder based">

You can see all Test Cases folders here.

After running tests on Katalon TestOps, a new folder is generated within the Test Case folder to store the execution data. You then can see the data in the folder named automatically and respectively after your test data.

## View tests uploaded via non-Git Repositories

If you upload tests as .zip file (non-KS projects), your test cases will not be displayed on the **Test Cases** page yet.

You must execute tests on Katalon TestOps to generate the test reports first. After running tests, the Test Cases together with their execution data will appear in the folder named *Uploaded Data*.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-dec-release-test-case-mgt/test-case-folder-format.png" width=100% alt="test case folder based UI">

## View JUnit and Katalon Studio's test data

This case applies if you don't run tests in Katalon TestOps.

In this case, the Test Cases together with their execution data will appear in the folder named *Uploaded Data* after you run tests in other different platforms.
