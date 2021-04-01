---
title: "BitBicuket Integration"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/bitbucket-integration.html
---

**BitBucket** is a web-based source control repository hosting service by Atlassian. Katalon Studio provides/supports the integration with BitBucket that simplify performing various commands directly from Katalon Studio UI such as: add Katalon Studio project files to the repositories; commit and pull changes, and push them to the repositories and so on.

**Requirements**

- Your computer already configured [Git Integration](https://docs.katalon.com/katalon-studio/docs/git-integration.html#configure-git-integration).

## Work with BitBucket Repositories

This section gives instructions on how to work with BitBucket repositories using Git.

### Create Katalon Studio projects in BitBucket

1. Connect to [BitBucket](https://bitbucket.org/).
2. Create a repository in Bitbucket.

    - In the **Repositories** on the left side bar > Click **Create repository**.

    - Select **Workspace** and Enter required **Project name** and **Repository name** > **Create repository**.

        <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/bitbucket-integration/create-repo-in-bitbucket.png" width=60%>

        



### Clone a Katalon Studio project from a Git repository in BitBucket



### Connecting to Git with SSH Keys

>Starting from **version 7.0.0**, Katalon Studio supports connecting to Git with SSH Keys.

1. Generating a public/private rsa key pair with this command:\
    `ssh-keygen -m PEM -t rsa -b 2048 -C "your_email@example.com"`
        > Note: Katalon Studio only supports `OpenSSL`, NOT `OpenSSH` formats.
2. Enter file in which to save the key.
3. Enter the SSH key [passphrase](https://help.github.com/en/articles/working-with-ssh-key-passphrases) and confirm it.
4. Add your SSH key to the ssh-agent.
5. Add a new SSH key to your Git account.

In the **Source Git Repository** dialog, enter a repository URL with SSH Protocol and click **Next**.  

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/git-integration/ssh.png" width="610" height="413">

Enter the passphrase for the key generated above.
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/git-integration/filled-passphrase.png" width="523" height="415">

3. At **Branch Selection** screen, you can choose which branches to be checked out as local branches. Click **Next** to continue.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/git-integration/branch.png" width="523" height="411">

4. At **Local Destination** dialog, specify the local location for cloning as well as the initial branch.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/git-integration/local.png" width="520" height="412">

    Where:

* Directory: the local storage location you want to store your Git's repository.
* Initial branch: all selected branches from the previous step are displayed here. Select the branch to be used initially from this list.

5. Click **Finish** when you are done. Katalon Studio automatically opens your cloned project.

6. To verify settings, go to **Katalon Studio> Preferences > Team > Git > Configurations >  Repository Settings**. Ensure that the repository is selected correctly with the URL specified.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/git-integration/verify.png" width="" height="">