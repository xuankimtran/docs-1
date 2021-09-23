---
title: "Git Integration Authentication with SSH Keys"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/git-integration-authentication.html
redirect_from:
    - "/katalon-studio/docs/bitbucket-integration.html"
description:
---

> Starting from **version 7.0.0**, Katalon Studio supports connecting to Git with SSH Keys.

In Katalon Studio, you can generate and add SSH keys to SSH agents without coding. With SSH keys, you can clone your Katalon Studio Project from cloud-hosted services of Git and integrate them with Katalon Studio. Cloud-hosted services of Git including:

* GitHub
* GitLab
* BitBucket
* Microsoft Azure DevOps

In this tutorial, you will learn how to generate SSH keys and clone a repository from cloud-hosted services of Git with an SSH protocal.

> Requirements:
>
> - An active Katalon Studio Enterprise license.
> - Connect to your cloud-hosted services of Git account.
> - You already create a repository in your cloud-hosted services of Git. You can download or clone our CI sample project from our Github repository: [CI sample](https://github.com/katalon-studio-samples/ci-samples).

## Generate SSH keys

1. To configure options for SSH, in **Katalon Studio > Preferences**, go to **General > Network Connection > SSH2**.

2. Manage your SSH keys:

    In the **General** tab, you can manage your SSH home directory and which private key you are using.

    For example, the SSH usually locates at `:/Users/your_user_name/.ssh` or `C:\Users\your_user_name\.ssh`). The `.ssh` folder contains your SSH private and public key, for example: `id_rsa` or `id_rsa.pub`.
    
    In the **Private keys** section, you can delete the old keys and only keep the ID key you use.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/git-integration/RSA%20id.png" alt="SSH URL" width=70%>

3. Generate new SSH keys:

    In the **Configuration options for SSH2** section, select the **Key Management** tab.

    You can check if you already have an existing SSH key by clicking **Load Existing Key**. This action opens your `.ssh` folder.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/git-integration/load-existing-key.png" alt="load existing key" width=50%>

    To generate a new SSH key, select **Generate DSA Key** or **Generate RSA Key** and copy the generated key to your clipboard.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/git-integration/generate-ssh-key.png" alt="rsa key" width=90%>

    You can also generate an RSA key with this command:

    `ssh-keygen -m PEM -t rsa -b 2048 -C "your_email@example.com"`

    > Notes:
    >
    > * Katalon Studio only supports `OpenSSL`, not `OpenSSH` formats.

4. Add your SSH key to the SSH agent:

    Enter the **Passphrase** or leave it empty, then click **Save Private Keys**. Enter the file name and click **Save**. A new private and a new public key are generated.

    > * See Github document on [Working with SSH key passphrases](https://help.github.com/en/articles/working-with-ssh-key-passphrases).
    
## Add a new SSH key to your account

### In GitHub

- Go to your **Git Account > Settings > SSH and GPG keys** and click **New SSH key**. The **SSH keys / Add new** page appears.
- Enter the **Title** and paste your **Key**, then click **Add SSH key**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/git-integration/Add%20new%20SSH%20key.png" alt="add new SSH key" width=70%>

### In Bitbucket

- Go to **Your profile and settings > Personal settings > SSH keys** and click **Add key**. The **Add SSH key** dialog appears.
- Enter the **Label** and paste your **Key**, then click **Add key**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/git-integration/bitbucket-org-account-settings-ssh-keys.png" alt="Bitbucket" width=100%>

### In Azure DevOps

- Go to **User Settings > SSH Publics key** and click **New Key**. The **Add New SSH Key** dialog appears.
- Enter the **Name** and paste your **Public Key Data**, then click **Add**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/git-integration/dev-azure-Katalon-usersSettings-keys.png" alt="ADO" width=100%>

### In GitLab

- Go to **User Settings > SSH key**.
- Enter the **Title**, set the expiration date and paste your **Key**. Then, click **Add key**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/git-integration/gitlab-profile-keys.png" alt=GitLab width=100%>

## Clone your Project

First, you need to enable Git Integration. See [Configure Git Integration](https://docs.katalon.com/katalon-studio/docs/git-integration.html#configure-git-integration).

After enabling Git Integration, you can clone an existing **Git repository** into a newly-created directory on the local machine.

1. In the main toolbar, click on the _Git_ icon and select **Clone Project**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/git-integration/image2017-2-22-143A13A12.png" alt="Clone Project" width=30%>

    The **Clone Git Repository** dialog is displayed. Enter a repository URL with SSH Protocol and click **Next**.

    > **How to get SSH Protocol?**
    > 
    > Go to your account on GitHub, GitLab, Bitbucket, or Azure DevOps, then go to the repository you want to clone to Katalon Studio.
    > Click **Clone** and select **SSH**, then copy the **SSH Protocol**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/git-integration/ssh.png" alt="source git repository" width=70%>
        
    
2. Enter the passphrase for your SSH key, then click **OK**. The **Branch Selection** screen appears.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/git-integration/filled-passphrase.png" alt="Enter the passphrase" width=70%>

3. Choose which branches to be checked out as local branches. Click **Next** to continue. The **Local Destination** appears.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/git-integration/branch.png" alt="choose local branches" width=70%>

4. Specify the local location for cloning as well as the initial branch.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/git-integration/local.png" alt="specify the local location for cloning" width=70%>

    - **Directory**: the local storage location you want to store your Git repository.
    - **Initial branch**: all selected branches from the previous step are displayed here. Select the branch to be used initially from this list.

5. Click **Finish** when you are done. Katalon Studio automatically opens your cloned project.

6. To verify settings, go to **Katalon Studio> Preferences > Team > Git > Configurations >  Repository Settings**. Ensure that the repository is selected correctly with the URL specified.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/git-integration/verify.png" alt="verify settings" width=70%>

After you successfully cloned your repositories, you can commit, pull, and push changes to the repositories from Katalon Studio. To learn more about how to integrate with Git, see [Git Integration](https://docs.katalon.com/katalon-studio/docs/git-integration.html#configure-git-integration).
