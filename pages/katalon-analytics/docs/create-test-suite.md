---
title: "Create Test Suites"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/create-test-suite.html
redirect_from:
---

You can create, update and manage test suites in Katalon TestOps.

By doing so, you save time creating the test suite in Katalon Studio and upload it to a Git script repository on TestOps.

## Create a Test Suite

> Requirements:
>
> * You have created a Git script repository in Katalon TestOps. See: [Upload Test Scripts from a Git Repository](https://docs.katalon.com/katalon-analytics/docs/git-test-project.html#create-git-script-repositories).
>
> * You have had a Katalon project.

Follow these steps:

1. Sign in to [Katalon TestOps](https://testops.katalon.io/login) and go to your project.

2. Go to **Test Management** > **Test Suites**.

3. Click on the **+ Test Suite** button.

    The **Create new Test Suite** dialog appears as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops-intergration.png" width=100% alt="create new ts dialog">

4. Fill in the required information.

    * **Test Suite Name**: create a name for your test suite.
    * **Script Repository**: select the script repo.
    * **Test Cases**: select the test case, then click **Add** to add it to your new test suite.

        > Notes:
        >
        > * You can only add the test case that is from the same script repo you have selected.
        > * If you want to switch to a different script repo, remove the added test cases manually first. Once all test cases have been removed, the **Script Repository** section is enabled again. You then can select a different script repo.
        >   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops-intergration.png" width=100% alt="remove test case">

5. Click **Create**.

You have created a test suite in Katalon TestOps.

The newly-created test suite is stored in the **TestOps** folder under the relevant script repo.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops-intergration.png" width=100% alt="testops folder">

> Notice:
>
> * The **TestOps** folder is a default system folder generated to store the test suite you have created on TestOps.
>
> * Katalon TestOps only recognizes this **TestOps** folder in the system. Therefore, do not use the same name when you create test suites in other platforms (Katalon Studio and script repositories).

## Execute a Test Suite

See: [Schedule Test Runs](https://docs.katalon.com/katalon-analytics/docs/create-plan.html).

## Manage a Test Suite

Similar to test cases, Katalon TestOps presents test suites in a folder-based view.
See: [Manage Test Cases](https://docs.katalon.com/katalon-analytics/docs/test-case-management.html#view-test-cases-from-script-repositories) to navigate where test cases/test suites  are stored and how they are presented in Katalon TestOps.

You can update the test suite you have created in Katalon TestOps.

### Rename a test suite and add/remove test cases

1. Go to **Test Management** > **Test Suites**.

2. Find your desired script repository in the folder list on the left sidebar.

3. Go to **Test Suites** > **TestOps** folder.

4. Click on the name of the test suite you created on TestOps (e.g., **Test Suite TW Demo**).

    The page appears as below.

5. Click **Edit** on the top right corner.

6. Edit the name in the **Test Suite Name** section.

7. Search the test case in the **Test Cases** section, then click **Add** to add a test case.

8. Click **Remove** to remove a test case in the test case list.
