---
title: "Using Git Submodules to share Test Artifacts"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/git-integration.html
description:
---

While working on a Katalon Studio project, you may want to use test artifacts from external resources. You can manually share test artifacts with the Test Artifacts Sharing feature provided by Katalon Studio. See: [Test Artifacts Sharing](https://docs.katalon.com/katalon-studio/docs/import-export-test-artifact.html). 

To maintain and update the shared resources easily, you can integrate them as Git submodules. Git submodules enable you to incorporate and track the version history of external resources. To learn more about Git submodules, you can refer to the official Git documentation: [Git Tools - Submodules](https://git-scm.com/book/en/v2/Git-Tools-Submodules).

This tutorial shows you how to use the Git submodule feature to incorporate test artifacts from an external source.

> You can download the sample project here on our Github repository: [Healthcare Tests](https://github.com/katalon-studio-samples/healthcare-tests).

In our example, we want to incorporate a keyword package hosted on Github into our project as a Git submodule. We demonstrate the simple tasks when working with a Git submodule, including *add*, *update*, and *remove* the submodule on our test project.

> **Requirements**:
>
> * An active Katalon Studio Enterprise license.
> * A Katalon Studio project configured as a Git repository. To configure Git integration in a project, refer to this guide: [Git Integration](https://docs.katalon.com/katalon-studio/docs/git-integration.html#configure-git-integration).
> * A custom keyword repository hosted on Github.

## Add the Git submodule to the project

The structure of our test project repository is as follows:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/git-integration-submodules/KS-Test-Explorer.png" alt="Test project repository in Test Explorer" width=70%>

The content of the custom keyword package on Github is as follows:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/git-integration-submodules/KS-remote-repo-overview.png" alt="Custom keyword package repository" width=70%>

Katalon Studio stores test keywords in the **Keywords** folder. Therefore, we want to add the custom keyword package to the `Keywords` folder as a Git submodule.

Follow these steps:

1. Open **Terminal**, then go to the `Keywords` folder in test project directory. For example, we go to the `healthcare-tests/Keywords` folder:

    ```bash
    $ cd healthcare-tests/Keywords
    $ pwd
    /Users/katalon/git/healthcare-tests/Keywords
    ```

2. To add the keyword library hosted Github, we use the ```git submodule add <URL>``` command.

    ```bash
    # Add the keyword repository from remote as a submodule
    $ git submodule add https://github.com/<username>/mykeywords.git

    ```

3. Check the status of the project repository with the ```git status``` command.

    After adding the keyword library as a submodule, the status output displays two changes: `.gitmodules` file and `mykeywords` folder.

    ```bash
    # Get the status after adding the submodule
    $ git status
    On branch master
    Your branch is up to date with 'origin/master'.
    Changes to be committed:
     (use "git restore --staged <file>..." to unstage)
         new file:   ../.gitmodules
         new file:   mykeywords
    ```

    The `.gitmodules` file contains information about added submodules, including directory paths and URLs for cloning and fetching.

4. Add and commit the changes.

    Once the submodule is added to the main repository, you can track the changes of the submodule like a normal repository. Here we track the submodule by adding and committing the changes.

    ```bash
    $ git add .
    $ git commit -m "Add the mykeywords package as submodule"
    ```

5. Verify that the custom keyword package is added to the test project. Open the project in Katalon Studio, from the main toolbar, select **Project > Refresh**.

    Katalon Studio should display the added package with keyword files in the **Keywords** section.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/git-integration-submodules/KS-Keywords-added-package.png" alt="Added keyword package in Test Explorer" width=70%>

## Update the Submodule

The keyword package hosted on Github may change following an update from other collaborators. 

In our example, a new custom keyword file is added to the remote repository:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/git-integration-submodules/KS-remote-repo-newly-added-file.png" alt="New keyword file added on Github repository" width=70%>

To update the local keyword package with the latest files from the remote repository, we use the `git submodule update --remote` command.

Follow these steps:

1. Open **Terminal**, then go to the `Keywords` folder in test project directory.

    ```bash
    $ cd healthcare-tests/Keywords
    $ pwd
    /Users/katalon/git/healthcare-tests/Keywords
    ```

2. Update the submodule with the `git submodule update --remote` command.

    The `git submodule update --remote` command updates the keyword package by pulling all the files from the remote repository into the package folder.

    ```bash
    $ git submodule update --remote
    ```

    If you check the `mykeywords` package folder, you can see that the new keyword file is added.

    ```bash
    $ ls mykeywords/
    HighlightElement.groovy
    VerifyDrodownValues_AlphabeticalOrder.groovy
    VerifyExpectedAndActualOptionsInDropdown.groovy
    refreshBrowser.groovy # Added keyword file
    ```

4. Add and commit the changes.

    ```bash
    $ git add .
    $ git commit -m "Add the new keyword after submodule update"
    ```

5. Verify that the new keyword file is added. Open the project in Katalon Studio, from the main toolbar, select **Project > Refresh**.

    Katalon Studio should display the updated keyword file.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/git-integration-submodules/KS-Keywords-updated-keyword.png" alt="New keyword file added in Test Explorer" width=70%>

## Delete the submodule

Git provides no simple interface to delete a submodule. To fully remove a submodule, we must remove the submodule folder and all references.

In our case, we want to fully remove the custom keyword package from the test project repository.

Follow these steps:

1. Open **Terminal**, then go to the `Keywords` folder containing the submodule in test project directory.

    ```bash
    $ cd healthcare-tests/Keywords
    ```

2. Remove the references to the submodule.

    Here we remove all the references to the keyword package `mykeywords`.

    ```bash
    # Remove the reference in the .git/config file
    $ git submodule deinit -f mykeywords 
    # Remove the reference in the .git/modules folder
    $ rm -rf ../.git/modules/Keywords/mykeywords/
    # Remove the tracked folder from Git index and the folder itself
    $ git rm -f mykeywords
    ```

3. Commit the changes.

    ```bash
    $ git commit -m "Remove the keyword submodule"
    ```

4. Verify that the custom keyword package is removed. Open the project in Katalon Studio, from the main toolbar, select **Project > Refresh**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/git-integration-submodules/KS-Keywords-removed-package.png" alt="Keyword package removed" width=70%>

