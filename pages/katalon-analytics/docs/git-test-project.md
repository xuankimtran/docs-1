---
title: "Upload Test Scripts from a Git Repository" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/git-test-project.html 
description: 
---

You can create a Git Script Repository in Katalon TestOps. Katalon TestOps can then upload Test Scripts automatically from a Git Repository. This allows you to store your Test Scripts in your Git accounts and execute them in Katalon TestOps.

Katalon TestOps allows GitHub integration and Bitbucket integration for Git Repositories.

In this guide, you will learn to enable GitHub and Bitbucket integration to create a Git Repository.

> Requirements:
>
> An existing [GitHub](https://github.com) and/or [Bitbucket](https://bitbucket.org/product) account.

## Create Git Script Repositories

Follow these steps:

1. Sign in to [Katalon TestOps]( https://testops.katalon.io/login) and go to the Project you want to create a Git Repository for.

   Go to **Configurations** > **Script Repositories**.
   
   The **Script Repositories** page appears as below.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-git-test-project/script-repo-screen-in-testops-config-new.png" width=100%>

2. Click **Create Git Script Repository**.

3. Fill in the required information.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-git-test-project/scrip-repo-page-after-creating-git-repo.png" width=100%>

   * For GitHub integration:

      * **Source Type**: choose **Github**.
      * **Repository URL**: enter your GitHub Repository. For example, https://github.com/katalon-studio-samples/ci-samples.
      * **Username**: enter your GitHub Username.
      * **Personal Access Token**: enter your Personal Access Token.
   
         > Notes:
         >
         > You can create an individual access token in GitHub. See: [Create a Personal Access Token](https://help.github.com/en/github/authenticating-to-github/creating-a-personal-access-token-for-the-command-line).
         >
         > Follow the instruction and make sure you choose **repo** in the **Select scopes** section in the **New personal access token** page.
         <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-git-test-project/new-personal-access-toke-page-git.png" width=100%>

   * For Bitbucket integration:

      * **Source Type**: choose **Bitbucket**.
      * **Repository URL**: enter your Bitbucket Repository.
      * **Username**: enter your Bitbucket Username.
      * **Personal Access Token**: enter your Personal Access Token.
   
         > Notes:
         >
         > See Bitbucket's [personal access tokens](https://confluence.atlassian.com/bitbucketserver/personal-access-tokens-939515499.html) for guidelines.

4. Click **Connect**.

   Additional sections appear as below.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-git-test-project/script-repo-page-after-clicking-connect.png" width=100%>

   * **Branch**: choose a branch.
   * **Name**: enter your Project’s name.

5. Click **Create**.

You have enabled GitHub/Bitbucket integration and created a new Git Script Repository.

Next step:
* [Schedule Test Runs](https://docs.katalon.com/katalon-analytics/docs/create-plan.html).