---
title: "Upload Test Scripts from a Git Repository" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/git-test-project.html 
description: 
---

You can create a Git script repository in Katalon TestOps. Katalon TestOps can then upload test scripts automatically from a Git repository. This allows you to store your test scripts in your Git accounts and execute them in Katalon TestOps.

Katalon TestOps allows Azure Repos, Bitbucket, GitHub and GitLab integration for Git repositories.

> Requirements:
>
> An existing [Azure Repos](https://azure.microsoft.com/en-us/services/devops/repos/)/ [Bitbucket](https://bitbucket.org/product)/ [GitHub](https://github.com)/ [GitLab](https://about.gitlab.com/install/) account.

## Create Git Script Repositories

Follow these steps:

1. Sign in to [Katalon TestOps]( https://testops.katalon.io/login) and go to the project you want to create a Git repository for.

   Go to **Configurations** > **Script Repositories**.
   
   The **Script Repositories** page appears as below.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-git-test-project/script-repo-screen-in-testops-config-new-2.png" width=100% alt="script repo page">

2. Click **Create Git Script Repository**.

3. Fill in the required information.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-git-test-project/scrip-repo-page-after-creating-git-repo-2.png" width=100% alt="create script repo page">

   * For Azure Repository integration:

      * **Source Type**: choose **Azure Repos**.
      * **Repository URL**: enter your Azure Repository.
      * **Username**: enter your Azure Repos Username.
      * **Personal Access Token**: enter your Personal Access Token.

      > Notes:
      >
      > See [Azure Repos Git Documentation](https://docs.microsoft.com/en-us/azure/devops/repos/git/?view=azure-devops) for guidelines.

   * For Bitbucket integration:

      * **Source Type**: choose **Bitbucket**.
      * **Repository URL**: enter your Bitbucket Repository.
      * **Username**: enter your Bitbucket Username.
      * **Personal Access Token**: enter your Personal Access Token.
   
         > Notes:
         >
         > See Bitbucket's [personal access tokens](https://confluence.atlassian.com/bitbucketserver/personal-access-tokens-939515499.html) for guidelines.
   
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

   * For Gitlab integration:

      * **Source Type**: choose **GitLab**.
      * **Repository URL**: enter your GitLab Repository.
      * **Username**: enter your GitLab Username.
      * **Personal Access Token**: enter your Personal Access Token.

         > Notes:
         >
         > You can create a personal access token in GitLab. See: [Create a personal access token](https://docs.gitlab.com/ee/user/profile/personal_access_tokens.html#create-a-personal-access-token).

4. Click **Connect**.

   The following sections appear:

   * **Branch**: choose a branch.
   * **Name**: enter your project’s name.

5. Click **Create**.

You have enabled Azure Repos/ Bitbucket/ GitHub/ GitLa integration and created a new Git script repository in Katalon TestOps.

Next step:
* [Schedule Test Runs](https://docs.katalon.com/katalon-analytics/docs/create-plan.html).