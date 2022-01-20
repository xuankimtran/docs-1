---
title: "Manage Test Suites"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/test-suite-management.html
redirect_from:
---

You can create, update and manage test suites in Katalon TestOps.

By doing so, you save time creating the test suite in Katalon Studio and uploading it to a Git script repository on TestOps.

## Create a Test Suite

> Requirements:
>
> * You have created a Git script repository in Katalon TestOps. See: [Upload Test Scripts from a Git Repository](https://docs.katalon.com/katalon-analytics/docs/git-test-project.html#create-git-script-repositories).
>
> * You have at least one Katalon project.

Follow these steps:

1. Sign in to [Katalon TestOps](https://testops.katalon.io/login) and go to your project.

2. Go to **Test Management** > **Test Suites**.

3. Click on the **+ Test Suite** button.

    The **Create new Test Suite** dialog appears as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/create-test-suites/create-new-test-suite-dialog.png" width=100% alt="create new ts dialog">

4. Fill in the required information.

    * **Test Suite Name**: create a name for your test suite.
    * **Script Repository**: select the script repo.
    * **Test Cases**: select the test case, then click **Add** to add it to your new test suite.

        > Notes:
        >
        > * You can only add test cases from the same script repo you have selected.
        > * If you want to switch to a different script repo, click **Remove** to remove the added test cases manually first. Once all test cases have been removed, the **Script Repository** section is enabled again. You then can select a different script repo.
        >   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/create-test-suites/create-new-test-suite-remove-button.png" width=100% alt="remove test case">

5. Click **Create**.

You have created a test suite in Katalon TestOps.

The newly-created test suite is stored in the **TestOps** folder under the relevant script repo.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/create-test-suites/created-ts-on-ts-page.png" width=100% alt="testops folder">

> Notice:
>
> * The **TestOps** folder is a default system folder generated to store the test suite you have created in TestOps.
>
> * Katalon TestOps has a refresh feature where you can sync the latest version from your Git repos to TestOps by clicking **Refresh**. To ensure the default system **TestOps** folder unaffected by this feature, Katalon TestOps ignores any other folder named **TestOps** in your Git repos. Therefore, do not use the same name when you create test suites in other platforms (Katalon Studio and script repositories). By doing so, you can avoid losing data if you use the refresh feature.

## Execute a Test Suite

See: [Schedule Test Runs](https://docs.katalon.com/katalon-analytics/docs/create-plan.html).

## View a Test Suite

Similar to test cases, Katalon TestOps presents test suites in a folder-based view. See also: [Manage Test Cases](https://docs.katalon.com/katalon-analytics/docs/test-case-management.html#view-test-cases-from-script-repositories).

### View test suites created in TestOps

To view a test suite created in TestOps, go to **Test Management** > **Test Suites**, select the script repository folder in the folder list on the left sidebar, then go to **Test Suites** > **TestOps**.

### View test suites uploaded from a Git repository

> Notes:
>
> Katalon TestOps supports integration with Azure Repos, Bitbucket, GitHub and GitLab.

To view a test suite uploaded from a Git repository, go to **Test Management** > **Test Suites**, select the relevant script repository, then click on the **Test Suites** folder.

* If you have not run tests yet, the execution data (Last executed) is empty.
* If you have run tests, this section contains information on your test executions.

> Notes:
>
> If you can't find your script repositories, you can refresh your script repositories to make test suites appear in folders on the **Test Suites** page. Follow these steps:
>
> 1. Go to **Configurations** > **Script Repositories**.
> 2. Select a script repository to go to the script repository page.
>   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-dec-release-test-case-mgt/script-repo-page.png" width=100% alt="script repo page">
> 3. Click **Refresh Test Suite Collection** in the top right corner.
> 4. Go to **Test Management** > **Test Suites**, then select the relevant script repository.
> 5. Click on the **Test Suites** folder.
>
>       You can now see test suites from the script repository you have refreshed.

### View test suites uploaded to a script repository

> Notice:
>
> This feature will soon be deprecated. We encourage you to use the other supported sources.

If you upload tests as .zip file, your test suites will not be displayed on the **Test Suites** page yet.

You must execute tests on Katalon TestOps to generate the execution reports first.

After running tests, the test suites and their execution data will appear inside the **Test Suites** folder within the **Uploaded Data** folder.

### View test suites from uploaded execution data

If you upload your execution data using the frameworks we support, or upload manually to Katalon TestOps (see: [Upload JUnit and Katalon Studio Test Results to Katalon TestOps](https://docs.katalon.com/katalon-analytics/docs/testops-uploader.html)), you can also view test data on the **Test Suites** page.

Katalon TestOps supports uploading test results from the following frameworks:

* Jasmine. See: [Upload Test to Katalon TestOps via Jasmine](https://docs.katalon.com/katalon-analytics/docs/kt-upload-test-jasmine.html).

* Jest. See: [Upload Test to Katalon TestOps via Jest](https://docs.katalon.com/katalon-analytics/docs/kt-upload-test-jest.html).

* Mocha. See: [Upload Test to Katalon TestOps via Mocha](https://docs.katalon.com/katalon-analytics/docs/kt-upload-test-mocha.html).

* Pytest. See: [Upload Test to Katalon TestOps via Pytest](https://docs.katalon.com/katalon-analytics/docs/kt-upload-test-pytest.html).

After uploading the execution data, go to **Test Management** > **Test Suites** and click on the **Uploaded Data** folder.

You can see test suites and their execution data inside the **Test Suites** folder in the **Uploaded Data** folder.

## Update a Test Suite

You can rename a test suite and add/remove test cases in the test suite you have created in Katalon TestOps.

> Notice:
>
> Katalon TestOps has a *re-import* feature where you can import the test reports repeatedly. This feature only recognizes the original name of the test suite you have created. If you rename the test suite and then re-import the reports, there is a high chance that TestOps does not recognize the new test suite name and consequently, it imports the wrong data. Therefore, rename your test suite with caution.

Follow these steps:

1. Go to **Test Management** > **Test Suites**.

2. Find your desired script repository in the folder list on the left sidebar.

3. Go to **Test Suites** > **TestOps**.

4. Click on the name of the test suite you created in TestOps (e.g., **Test Suite TW Demo**).

    The page appears as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/create-test-suites/ts-tw-demo-page-edit-button.png" width=100% alt="ts page edit button">

5. Click **Edit** in the top right corner.

    The page appears as below.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/create-test-suites/update-ts-tw-demo.png" width=100% alt="script repo page">

6. Update the test suite.

    * You can edit the name in the **Test Suite Name** section.
    * You can search the test case in the **Test Cases** section, then click **Add** to add a test case.
    * You can remove a test case in the test case list by clicking **Remove**.

