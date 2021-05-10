---
title: "BitBucket Integration"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/bitbucket-integration.html
---

[BitBucket](https://bitbucket.org/product/guides) is a Git-based code hosting and collaboration tool. Katalon Studio supports BitBucket the same way it provides support for other similar mechanisms via [Git integration](https://docs.katalon.com/katalon-studio/docs/git-integration.html#about-git-integration).

Katalon Studio provides the integration with BitBucket to simplify performing various commands directly from Katalon Studio UI. With this integration, you can add Katalon Studio project files to the repositories, commit and pull changes, and push them to the repositories, and so on.

**Requirements**

- An active Katalon Studio Enterprise lience.
- Connect to your [BitBucket](https://bitbucket.org/) account.
- You already [Created a Git repository](https://support.atlassian.com/bitbucket-cloud/docs/create-a-git-repository/) in BitBucket.

### Connect to BitBucket with SSH Keys

Follow [this document](https://support.atlassian.com/bitbucket-cloud/docs/set-up-an-ssh-key/) to set up an SSH Key and add that public key to your BitBucket Account settings. Do as follows:

1. Generating a public or private rsa key pair with this command:\
`ssh-keygen -m PEM -t rsa -b 2048 -C "your_email@example.com"`
    > Note: Katalon Studio only supports `OpenSSL`, NOT `OpenSSH` formats.
2. Enter the file in which to save the key.
3. Enter the SSH key passphrase and confirm it.
4. Add your SSH key to the ssh-agent.
5. Add a new SSH key to your BitBucket account.

### Clone a Katalon Studio project from a BitBucket repository

1. In BitBucket, get the repository URL with **SSH Protocol** for the project clone.

    - Go to the repository you want to clone > click **Clone** in the right corner.

        <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/bitbucket-integration/repo-created.png" width=70%>

    - Select **SSH** > copy the repository URL.
        
        <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/bitbucket-integration/ssh-url.png" width=70%>

2. In Katalon Studio, select the **Git** icon from the main toolbar > **Clone Project**.
    
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/bitbucket-integration/git-icon.png" width=40%>

3. In the displayed **Source Git Repository** dialog, enter the repository URL with **SSH Protocol** in step 1 > **Next**.  

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/bitbucket-integration/source-git-repo.png" width=70%>

4.  In **Branch Selection**, select which branch(es) to be checked out as local branch(es) >  **Next**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/bitbucket-integration/branch-selection.png" width=70%>

5. In **Local Destination**, specify the local location for cloning and the initial branch > **Finish**.

    Katalon Studio automatically opens your cloned project.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/bitbucket-integration/save.png" width=70%>

    **Where:**

    - **Directory**: the local storage location you want to store your Git repository.
    - **Initial branch**: all selected branches from step 4 are displayed here. Select the branch to be used initially from this list.

6. To verify settings, go to **Katalon Studio/Preferences/Team/Git/Configurations > Repository Settings**. 

    Ensure that the repository is selected correctly with the URL specified.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/bitbucket-integration/verify-configuration.png" width=70%>

### Store Katalon Studio Projects in BitBucket

1. In Katalon Studio, select the **Git** icon from the main toolbar > **Commit**.
    
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/bitbucket-integration/commmit.png" width=40%>

2. The **Git Staging** tab is displayed for configuration.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/bitbucket-integration/git-log.png" width=70%>

    **Where:**

    | Field | Description |
    | --- | --- |
    | Unstaged Changes | Changes which have been made. |
    | Staged Changes | Selected changes from **Unstaged Changes.** These changes are committed. |

3. From the **Unstaged Changes** list, select the changes to be committed, then right-click on them and select **Add To Index**. Selected changes are added to the **Staged Changes** list.

4. Enter your comments into the **Commit Message** > click **Commit and Push...** to store your staged changes into the local branch and push them to BitBucket.