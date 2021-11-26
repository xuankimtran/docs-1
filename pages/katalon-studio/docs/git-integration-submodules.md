---
title: "Using Git Submodules to share Test Artifacts"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/git-integration.html
description:
---

While working on a Katalon Studio project, you may want to use Test Artifacts from external resources. To maintain and update the shared resources, you can add them as Git submodules. Git submodules enable you to incorporate and track the version history of external resources easily. To learn more about Git submodules, you can refer to the official Git documentation: [Git Tools - Submodules](https://git-scm.com/book/en/v2/Git-Tools-Submodules).

This tutorial shows you how to use the Git submodule feature to integrate Test Artifacts from an external source.

> You can download the sample project here on our Github repository: [Healthcare Tests](https://github.com/katalon-studio-samples/healthcare-tests).

In our example, we incorporate an Excel-related keyword library hosted on Github into our project as a Git submodule. We then update the submodule with the latest changes, make some local changes to the library, and push the library to the remote repository.

> **Requirements**:
>
> * An active Katalon Studio Enterprise license.
> * A Katalon Studio project configured as a Git repository. To configure Git integration in a project, refer to this guide: [Git Integration](https://docs.katalon.com/katalon-studio/docs/git-integration.html#configure-git-integration).
> * A custom keyword repository hosted on Github.

## Add a Git submodule to the project

The structure of our test project repository is as follows:

```bash
healthcare-tests/
├── Checkpoints
├── Data\ Files
├── Drivers
├── GlobalVariables.glbl
├── Include
├── Keywords
├── Libs
├── Object\ Repository
├── Plugins
├── Profiles
├── README.md
├── Reports
├── Scripts
├── Test\ Cases
├── Test\ Listeners
├── Test\ Suites
├── bin
├── console.properties
├── katatlon-test.sh
├── settings
├── test.prj
├── thumbnail.png
└── thumbnail@2x.png
```

We want to add an Excel custom keyword library to the `Keywords` folder as a Git submodule.

Follow these steps:

1. Open **Terminal**, then go to the `Keywords` folder in test project directory. For example, we go to the `healthcare-tests/Keywords` folder:

    ```bash
    $ cd healthcare-tests/Keywords
    $ pwd
    /Users/katalon/git/healthcare-tests/Keywords
    ```

2. To add the keyword library hosted Github, we use the ```git submodule add <Github_URL>``` command.

    In our example, the URL to keyword library is `https://github.com/haolekatalon/excelKeywords.git`.

    ```bash
    # Add the keyword repository from remote as a submodule
    $ git submodule add https://github.com/haolekatalon/excelKeywords.git
    Cloning into '/Users/<username>/git/healthcare-tests/Keywords/excelKeywords'...
    remote: Enumerating objects: 5, done.
    remote: Counting objects: 100% (5/5), done.
    remote: Compressing objects: 100% (5/5), done.
    remote: Total 5 (delta 0), reused 5 (delta 0), pack-reused 0
    Receiving objects: 100% (5/5), done.
    ```

3. Check the status of the project repository with the ```git status``` command.

    After adding the keyword library as a submodule, the status output displays two changes: `.gitmodules` file and `excelKeywords` folder.

    ```bash
    # Get the status after adding the submodule
    $ git status
    On branch master
    Your branch is up to date with 'origin/master'.

    Changes to be committed:
    (use "git restore --staged <file>..." to unstage)
        new file:   ../.gitmodules
        new file:   excelKeywords
    ```

    The `.gitmodules` file contains information about added submodules, including directory paths and URLs.

4. 