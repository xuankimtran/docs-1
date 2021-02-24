---
title: "Upload Git Test Project" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/git-test-project.html 
description: 
---

This feature allows you to create your projects stored in Git and execute them in Katalon TestOps without manually uploading them to Test Projects.

## Create a new Git test project

Choose a project in which you want to create a new Git on Katalon TestOps.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/git-test-project/kt_choose_project_create_git.png)

On sidebar **Configurations** > **Script Repositories**. 

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/git-test-project/kt_config_script_repo.png)

Click button Create Git Script Repository.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/git-test-project/kt_click_create_git_script_repo.png)

Then fill in the below information:

- **Source Type**: choose Github.

- **Repository URL**: your Git repository. (Example: https://github.com/katalon-studio-samples/ci-samples)

- **Username**: your Git username.

- **Personal Access Token**: your **personal access token**. To create an individual access token in Github, refer to [this document](https://help.github.com/en/github/authenticating-to-github/creating-a-personal-access-token-for-the-command-line). In the https://github.com/settings/tokens, at **New personal access token** > **Select scopes**, we click **repo** for generating token.
   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/git-test-project/kt_token_select_scopes.png)

Then click the button **Connect**.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/git-test-project/kt_fill_script_repositories.png)

In **Script Repository**, the **Branch**, **Name**, and **Description** display.

- **Branch**: choose a branch.

- **Name**: your project’s name.

Click button **Create** to create the Git test project.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/git-test-project/kt_connect_script_repositories.png)

In the list of **Script Repositories**, we created a new Git. 

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/git-test-project/kt_git_sample_create.png)

## Plan your Git project

To plan your Git projects, go to sidebar **Test Planning**. [Learn more](https://docs.katalon.com/katalon-analytics/docs/create-plan.html)