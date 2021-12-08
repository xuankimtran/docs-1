---
title: "Manage Test Cases"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/test-case-management.html
redirect_from:
---

Katalon TestOps presents test cases in a folder-based format that structures the information you receive on your tests.

This document navigates you to where test cases are stored and how they are presented in Katalon TestOps to help you manage test cases effectively.

## View test cases from script repositories

There are two ways to upload your test cases to Katalon TestOps:

* Upload tests via a Git repository (GitHub and Bitbucket). See: [Upload Test Scripts from a Git Repository](https://docs.katalon.com/katalon-analytics/docs/git-test-project.html).
* Upload tests via a non-Git repository (as .zip file). See: [Upload Test Scripts to a Script Repository](https://docs.katalon.com/katalon-analytics/docs/code-repo.html).

Depending on the type of your script repository (Git or non-Git), you can read the relevant section below to find your tests cases and their execution data.

### View test cases uploaded via a Git repository

After uploading your test scripts from a Git repository, go to **Test Management** > **Test Cases**.

The **Test Cases** page appears.

Here you can see all test case folders (corresponding to your Git repositories) display below the *Uploaded Data* folder.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-dec-release-test-case-mgt/test-case-from-git-repo.png" width=100% alt="test case folder based">

If you have not run tests yet, the execution data (**Last executed**, **Average Duration**, **Flakiness (%)**) is empty.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-dec-release-test-case-mgt/test-case-execution-data-info.png" width=100% alt="execution data info">

If you have run tests, this section contains information on your test executions.

> Notes:
>
> If you are an existing user who has created script repositories in Katalon TestOps before, you need to refresh your script repositories to make test cases appear in folders on the **Test Cases** page. Follow these steps:
>
> 1. Go to **Configurations** > **Script Repositories**.
>
> 2. Select a script repository to go to the script repository page.
>   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-dec-release-test-case-mgt/script-repo-page.png" width=100% alt="script repo page">
>
> 3. Click **Refresh Test Suite Collection** in the top right corner.
>
> 4. Go to **Test Management** > **Test Cases**.
>
> You can now see test cases from the script repository you have refreshed.

### View tests uploaded via a non-Git repository

If you upload tests as .zip file (non-KS projects), your test cases will not be displayed on the **Test Cases** page yet.

You must execute tests on Katalon TestOps to generate the execution reports first.

After running tests, the test cases and their execution data will appear in a folder within the *Uploaded Data* folder.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-dec-release-test-case-mgt/test-case-folder-info.png" width=100% alt="uploaded data folder inside">

## View tests executed in other platforms

If you run tests in other platforms than Katalon TestOps, you can upload their execution data and reports to Katalon TestOps and view them on the **Test Cases** page.

Katalon TestOps supports uploading test results from the following frameworks:

* Upload JUnit and Katalon Studio's (KS) test data. See: [Upload JUnit and Katalon Studio Test Results to Katalon TestOps](https://docs.katalon.com/katalon-analytics/docs/testops-uploader.html).
This case applies if you don't run tests in Katalon TestOps.

* Upload Mocha test results. See: [Upload Test to Katalon TestOps via Mocha](https://docs.katalon.com/katalon-analytics/docs/kt-upload-test-mocha.html).

* Upload Jest test results. See: [Upload Test to Katalon TestOps via Jest](https://docs.katalon.com/katalon-analytics/docs/kt-upload-test-jest.html).

* Upload Jasmine test results. See: [Upload Test to Katalon TestOps via Jasmine](https://docs.katalon.com/katalon-analytics/docs/kt-upload-test-jasmine.html).

* Upload Pytest test results. See: [Upload Test to Katalon TestOps via Pytest](https://docs.katalon.com/katalon-analytics/docs/kt-upload-test-pytest.html).

After uploading the execution data, go to **Test Management** > **Test Cases** and click on the *Uploaded Data* folder.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-dec-release-test-case-mgt/test-case-folder-format.png" width=100% alt="uploaded data folder outside">

You can see test cases and their execution data in folders inside the *Uploaded Data* folder.
