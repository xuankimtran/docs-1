---
title: "BitBcuket Integration"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/bitbucket-integration.html
---

**BitBucket** is a web-based source control repository hosting service by Atlassian. Katalon Studio provides/supports the integration with BitBucket that simplifies performing various commands directly from Katalon Studio UI such as: add Katalon Studio project files to the repositories; commit and pull changes, and push them to the repositories, and so on.

**Requirements**

- Your computer already configured [Git Integration](https://docs.katalon.com/katalon-studio/docs/git-integration.html#configure-git-integration).
- Connect to your [BitBucket](https://bitbucket.org/) account.
- You already [Created a Git repository](https://support.atlassian.com/bitbucket-cloud/docs/create-a-git-repository/) in BitBucket.

## Work with BitBucket Repositories

This section gives instructions on how to work with BitBucket repositories using Git.

### Connecting to Git with SSH Key

Follow [this document](https://support.atlassian.com/bitbucket-cloud/docs/set-up-an-ssh-key/) to set up an SSH Key in BitBucket.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/bitbucket-integration/add-key.png" width=70%>

### Clone a Katalon Studio project from a Git repository in BitBucket

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/bitbucket-integration/repo-created.png" width=60%>

1. In BitBucket, get the repository URL with **SSH Protocol** for the project clone.
        
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/bitbucket-integration/get-ssh-url-to-clone.png" width=65%>

2. In Katalon Studio, select the **Git** icon from the main toolbar > **Clone Project**.
    
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/bitbucket-integration/git-icon.png" width=30%>

3. In the displayed **Source Git Repository** dialog, enter the repository URL with **SSH Protocol** in step 1 > **Next**.  

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/bitbucket-integration/source-git-repo.png" width=70%>

4.  In **Branch Selection**, select which branch(es) to be checked out as local branch(es) >  **Next**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/bitbucket-integration/branch-selection.png" width=70%>

5. In **Local Destination**, specify the local location for cloning and the initial branch > **Finish**.

    Katalon Studio automatically opens your cloned project.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/bitbucket-integration/save.png" width=70%>

    Where:

    - **Directory**: the local storage location you want to store your Git repository.
    - **Initial branch**: all selected branches from step 4 are displayed here. Select the branch to be used initially from this list.

6. To verify settings, go to **Katalon Studio/Preferences/Team/Git/Configurations > Repository Settings**. 

    Ensure that the repository is selected correctly with the URL specified.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/bitbucket-integration/verify-configuration.png" width=70%>
