---
title: "Create Test Suites"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/create-test-suite.html
redirect_from:
---

You can create and manage test suites in Katalon TestOps.

## Create a Test Suite

By doing so, you save time opening Katalon Studio to create the new test suite then upload it to a script repository.

> Requirements:
>
> * You have created a Git script repository in Katalon TestOps. See: [Upload Test Scripts from a Git Repository](https://docs.katalon.com/katalon-analytics/docs/git-test-project.html#create-git-script-repositories).
>
> * You use Katalon projects.

Follow these steps:

1. Sign in to [Katalon TestOps](https://testops.katalon.io/login) and go to your project.

2. Go to **Test Management** > **Test Suite*.

3. Click on the **+ Test Suite** button.

    The **Create new Test Suite** box appears as below.

4. Fill in the required information.

    * **Test Suite Name**: create a name for your test suite.
    * **Script Repository**: select the script repo.
    * **Test Cases**: add the test cases to your new test suite.

        > Notes:
        >
        > * You can only add the test case that is from the same script repo you have selected.
        > * If you want to use test cases from a different script repo, you have to remove your added test cases manually first, then select a different script repot to switch to it.

5. Click **Create**.

You have created a test suite in Katalon TestOps.

You can find the test suite in the selected script repo > Test Suites > TestOps folder.

> Notice:
>
> * All test suites you create on Katalon TestOps are stored in the default system folder called *TestOps folder*. Katalon TestOps only recognizes this *TestOps folder* in our system. Therefore, do not use the same name in Katalon Studio and script repositories.

## Execute a Test Suite

See: [Schedule Test Runs](https://docs.katalon.com/katalon-analytics/docs/create-plan.html).

## Manage a Test Suite

Similar to test cases, Katalon TestOps presents test suites in a folder-based view. 
See: [Manage Test Cases](https://docs.katalon.com/katalon-analytics/docs/test-case-management.html#view-test-cases-from-script-repositories) to navigate where test cases/test suites  are stored and how they are presented in Katalon TestOps.

You have options to add or remove test cases, and rename the test suite you have created in Katalon TestOps.

> Notes:
>
> You cannot update test suites from Katalon Studio and script repos.

### Add test cases
### Remove test cases
### Rename a test suite
