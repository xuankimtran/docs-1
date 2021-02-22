---
title: "Upload Test Script From Git Repository" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/git-test-project.html 
description: 
---
This feature allows you to upload your projects stored in Git and execute them in Katalon TestOps without manually uploading to Script Repository.

## Create Git script repository

1. Navigate to Script Repository under Configuration to select "Create Git script repository" 

<img src="https://github.com/katalon-studio/docs-images/blob/master/katalon-analytics/docs/git-test-project/1-git-test-project.png" width="" height="">

2. Fill in information as below:
- Select a source type 
- **Repository URL**: your Git repository. (Example: https://github.com/katalon-studio-samples/ci-samples)
- **Username**: your Git username
- **Personal Access Token**: to create a personal access token in Github, refer to [this document](https://help.github.com/en/github/authenticating-to-github/creating-a-personal-access-token-for-the-command-line).


Click **Connect** to create the Git script repository.

<img src="https://github.com/katalon-studio/docs-images/blob/master/katalon-analytics/docs/git-test-project/2-git-test-project.png" width="" height="">


## Schedule Test Run From Git Repository

> You can only use Katalon Command to run jobs from Git.

1.  Navigate to to **Script Repository** to choose your git script 
2.  Click on **Schedule Test Run** button. [Learn more](https://docs.katalon.com/katalon-analytics/docs/create-plan.html)


