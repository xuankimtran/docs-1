---
title: "Upload Test Scripts from Git Repositories" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/git-test-project.html 
description: 
---

You can create a Git Repository in Katalon TestOps. By doing so, you can store your Projects in Git and execute them in Katalon TestOps. You do not have to upload your Projects manually to Test Projects.

## Create Git Script Repository

Follow these steps:

1. Sign in [Katalon TestOps](https://testops.katalon.io/login?redirect=%252F%253F) and go to the Project you want to create a Git Repository for.

   Go to **Configurations** > **Script Repositories**.
   
   The **Script Repositories** page appears as below.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-git-test-project/script-repo-screen-in-testops-config.png" width=100%>

2. Click **Create Git Script Repository**.

3. Fill in the required information.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-git-test-project/scrip-repo-page-after-creating-git-repo.png" width=100%>

   * **Source Type**: choose **Github**.
   * **Repository URL**: enter your Git Repository. For example, https://github.com/katalon-studio-samples/ci-samples.
   * **Username**: enter your Git Username.
   * **Personal Access Token**: enter your Personal Access Token.
   
      > Notes:
      >
      > You can create an individual access token in GitHub. 
      >
      > See: [Create a Personal Access Token](https://help.github.com/en/github/authenticating-to-github/creating-a-personal-access-token-for-the-command-line).
      > 
      > Follow the instruction and make sure you choose **repo** in the **Select scopes** section in the **New personal access token** page.      
      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-git-test-project/new-personal-access-toke-page-git.png" width=100%>

4. Click **Connect**.

   Additional sections appear as below.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-git-test-project/script-repo-page-after-clicking-connect.png" width=100%>

   * **Branch**: choose a branch.
   * **Name**: enter your Project’s name.

5. Click **Create**.

You have created a new Git Test Project.

Next step:
* Plan Git Projects. See: [Schedule Test Runs](https://docs.katalon.com/katalon-analytics/docs/create-plan.html).
