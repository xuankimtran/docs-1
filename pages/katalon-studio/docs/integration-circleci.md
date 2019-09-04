---
title: "Katalon Studio E2E testing integration with CircleCI" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/integration-circleci.html 
description: Guidelines on how to set up Katalon Studio E2E Tests to run on continuous integration server CircleCI.
---
## Introduction to CircleCI

CircleCI is a continuous integration server where every commit executes an automated build and test. In this case, automated tests are integrated into a shared repository, can be configured to run at specific times and managed by all team members. You can read more about CircleCI features on the [official website](https://circleci.com/).

## The most important thing - config.yml file

To run Katalon tests on CircleCI you need to:

- Have a repository on GitHub or [create a new one](https://help.github.com/en/articles/create-a-repo);

- Add .yml file into .circleci folder (keep in mind that a folder with a period will be hidden by default) and commit to your GitHub repository. 

Here you can see an example of config.yml file that you need to add to the .circleci folder and commit to your GitHub repository together with your tests. Pay attention to folder structure - .circleci should be in the Katalon Studio Project Folder.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integration-circleci/1-command.png)

Keep in mind that this configuration can be changed according to your preferences. I run my tests from TestSuitCollection folder so I added a command option -testSuiteCollectionPath=<path>, but if you want to run your tests from Test Suite, you should use -testSuitePath=<path>. You can find more information on general Katalon Studio options [here](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#execute-katalon-in-cmd).

When the config.yml file is ready and committed, you should go to the CircleCI platform and follow these steps:

- Sign up to the CircleCi platform (use your GitHub account to join the platform);

- Add and set up your project (the initial condition is - you must have GitHub repository permissions to view or follow associated projects). After registering to circleci you should be able to see this window (see the image below). You just need to click **Set Up Project** and **Start Building** (you do not need to configure a yml file because you have done it previously).

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integration-circleci/2-set-up-project.png)

After “start building” is clicked and at least one change pushed, you will be able to see a job’s status - running, success, failed, on hold, queued. You can see more details by clicking on the status and expanding section details or moving and tracking your test result report on Katalon Analytics (read the chapter below on how to do that).

## Upload results to Katalon analytics

Katalon Studio has several ways to analyze test results - one of them is to integrate Katalon Analytics. This way you are able to get generated and detailed reports after every completed build in CircleCI. In order to send your test results to Katalon Studio Analytics you need to:

- Navigate and Login/Sign Up to Katalon Analytics;
- Open your Katalon Studio Project and Click ‘Project’ from the main menu;
- Select Settings -> Katalon Analytics -> Integration -> Fill in Katalon Analytics information;
- Click Apply -> Ok;
- Return to Katalon Analytics;
- Create a new project;
- Set Up Grid to automatically send results to Analytics;

Congratulations - now your test results should be able to reach Katalon Analytics after every completed build. 

## Switch environments easily by using Profiles

In this section, I will describe how to set up the same tests to run in several environments. Katalon Studio has a feature that creates a Profile. When you starting creating a Katalon Studio project a default profile is created. We can assume that the default profile is your dev environment. So, you wrote a lot of tests in the dev environment and you need to run the same tests on prod. Follow these steps to make it real:

- Create a separate test ‘NavigateToUrl’, add a global variable: 

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integration-circleci/3-navigatetourl.png)

- Add the created variable to the default profile, set an environment url:

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integration-circleci/4-set-environment-url.png)

- Create another Profile, e.g. prod, set another environment url;

- Create a New Test Suite Collection, Add Test Suites to created Collection and configure which browsers, profiles to run. 

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integration-circleci/5-create-new-test-suite.png)

## Conclusion

Katalon Studio can be integrated with many useful tools you just need to set up everything right and have an amazing automated solution for your project.

Automation processes should not be painful and hard to do. Don’t forget one of Agile’s principles - “Simplicity is the art of maximizing the work not done”.

----------------

_Published by [Auksė Žirgulė](https://www.linkedin.com/in/auksezirgule/) - QA Lead at Hostinger International_

_Original article: https://www.linkedin.com/pulse/katalon-studio-e2e-testing-integration-circleci-auks%C4%97-%C5%BEirgul%C4%97/_




