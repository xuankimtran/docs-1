---
title: "BitBucket Integration"
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

### Connect to Git with SSH Keys

Follow [this document](https://support.atlassian.com/bitbucket-cloud/docs/set-up-an-ssh-key/) to set up an SSH Key and add that public key to your BitBucket Account settings to connect with Git.

The basic steps are:

1. Generating a public/private rsa key pair with this command:\
`ssh-keygen -m PEM -t rsa -b 2048 -C "your_email@example.com"`
    > Note: Katalon Studio only supports `OpenSSL`, NOT `OpenSSH` formats.
2. Enter file in which to save the key.
3. Enter the SSH key passphrase and confirm it.
4. Add your SSH key to the ssh-agent.
5. Add a new SSH key to your Git account.

### Clone a Katalon Studio project from a Git repository in BitBucket

1. In BitBucket, get the repository URL with **SSH Protocol** for the project clone.

    - Go to the repository you want to clone > click **Clone** in the right corner.

        <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/bitbucket-integration/repo-created.png" width=65%>

    - Select **SSH** > copy the repository URL.
        
        <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/bitbucket-integration/ssh-url.png" width=60%>

2. In Katalon Studio, select the **Git** icon from the main toolbar > **Clone Project**.
    
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/bitbucket-integration/git-icon.png" width=30%>

3. In the displayed **Source Git Repository** dialog, enter the repository URL with **SSH Protocol** in step 1 > **Next**.  

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/bitbucket-integration/source-git-repo.png" width=65%>

4.  In **Branch Selection**, select which branch(es) to be checked out as local branch(es) >  **Next**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/bitbucket-integration/branch-selection.png" width=65%>

5. In **Local Destination**, specify the local location for cloning and the initial branch > **Finish**.

    Katalon Studio automatically opens your cloned project.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/bitbucket-integration/save.png" width=65%>

    Where:

    - **Directory**: the local storage location you want to store your Git repository.
    - **Initial branch**: all selected branches from step 4 are displayed here. Select the branch to be used initially from this list.

6. To verify settings, go to **Katalon Studio/Preferences/Team/Git/Configurations > Repository Settings**. 

    Ensure that the repository is selected correctly with the URL specified.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/bitbucket-integration/verify-configuration.png" width=65%>
