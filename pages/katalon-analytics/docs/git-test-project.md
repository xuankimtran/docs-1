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

   * **Source Type**:  choose your Git script repository source type (**Azure Repos**/ **Bitbucket**/ **GitHub**/ **GitLab**).
   * **Repository URL**: enter the URL of your Git script repository.
   * **Username**: enter your Azure Repos/ Bitbucket/ GitHub/ GitLab username.
   * **Personal Access Token**: enter your Personal Access Token (PAT).

> Notes:
>
> To get the information on your repository URL and username, see the following documentation:
>  * [Azure Repos Git Documentation](https://docs.microsoft.com/en-us/azure/devops/repos/git/?view=azure-devops).
>  * [Bitbucket Documentation](https://confluence.atlassian.com/bitbucketserver/bitbucket-data-center-and-server-documentation-776639749.html).
>  * [GitHub Docs](https://docs.github.com/en).
>  * [GitLab Docs](https://docs.gitlab.com/ee/).
>
> To create a PAT, see the following guides:
>  * For Azure Repos, see: [Use personal access tokens](https://docs.microsoft.com/en-us/azure/devops/organizations/accounts/use-personal-access-tokens-to-authenticate?view=azure-devops&tabs=preview-page).
>  * For Bitbucket, see: [HTTP access tokens](https://confluence.atlassian.com/bitbucketserver/personal-access-tokens-939515499.html).
>  * For GitHub, see: [Create a Personal Access Token](https://help.github.com/en/github/authenticating-to-github/creating-a-personal-access-token-for-the-command-line).
>     * Follow the instruction and make sure you choose **repo** in the **Select scopes** section in the **New personal access token** page.
         <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-git-test-project/new-personal-access-toke-page-git.png" width=100%>
>  * For GitLab, see: [Create a personal access token](https://docs.gitlab.com/ee/user/profile/personal_access_tokens.html#create-a-personal-access-token).

4. Click **Connect**.

   The following sections appear:

   * **Branch**: choose a branch.
   * **Name**: enter your project name.

5. Click **Create**.

You have enabled Azure Repos/ Bitbucket/ GitHub/ GitLab integration and created a new Git script repository in Katalon TestOps.

Next step:
* [Schedule Test Runs](https://docs.katalon.com/katalon-analytics/docs/create-plan.html).