---
title: "Integration with CircleCI (Katalon Orb)" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/integration-circleci.html 
---
> Katalon TestOps CI is an easier way to execute Katalon Studio tests remotely or schedule remote Katalon Studio execution. [Learn more](https://docs.katalon.com/katalon-analytics/docs/kt-remote-execution.html)

Orbs are shareable packages of configuration elements, including jobs, commands, and executors [(definition from CircleCI)](https://circleci.com/docs/2.0/orb-intro/).

Katalon Orb allows executing Katalon tests with your CircleCI CI/CD pipeline easily. We recommend getting the latest version from the CircleCI Orb registry page. Download **katalon/katalon-studio@23.0.8** [here](https://circleci.com/orbs/registry/orb/katalon/katalon-studio). Please note that [katalon/katalonstudio@36.0.0](https://circleci.com/orbs/registry/orb/kms-technology/katalonstudio) is deprecated.

**Prerequisites**:

* Katalon Studio version 7.0+.
* An active [Katalon Runtime Engine license](https://docs.katalon.com/katalon-studio/docs/intro-RE.html#license).

## Setup and Configuration

First, you need to establish a connection between your Katalon project in GitHub and CircleCI, then run the test with the Katalon Orb.

### In GitHub

1. Use your repository on GitHub or create a new one storing your Katalon project code.
2. Add a `.yml` file containing Katalon commands to run the test to the `.circleci` folder in the above GitHub repository (e.g. `katalon-studio-samples/ci-samples/.circleci/config.yml`) and commit. Please see the example of the `config.yml` file below.
   >**Notes**: In the Orb source code, you can only configure `katalonstudio/run` to run Katalon tests. Please refer to the [command syntax document](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#katalon-studio-plugins-in-console-mode) for the supported options.
   
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integration-circleci/circleci4.png" width="" height="">

### In CircleCI

Log into CircleCI and configure CircleCI environment variables in your GitHub projects.

1. Select **Settings** > choose a Git Organization
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/circleci/circleci1.png" width="" height="">
2. Select **Projects** > click on the **Settings** icon of your preferred project
3. Under **Build Settings**, select **Environment Variables**
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/circleci/circleci2.png" width="" height="">
4. **Import Variables** or **Add Variable** to your project. E.g. KATALON_API_KEY
   > Katalon API Key
   >
   > You must get the API Key from [Katalon TestOps](https://analytics.katalon.com/) and then set it as an environment variable in CircleCI to secure this string. Please do NOT store it in source code.
   > See also: [How to create API Keys in Katalon TestOps](https://docs.katalon.com/katalon-analytics/docs/ka-api-key.html)

## Execute tests with Katalon Orb

Katalon Orb automatically executes Katalon tests after each commit to the configured GitHub repository.

After running Katalon tests in CircleCI, you can download test execution reports in the **Artifact** tab.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integration-circleci/circleci5.png" width="" height="">

## Usage Examples

> CI sample projects of Katalon Studio are available [here](https://github.com/katalon-studio-samples/ci-samples/).

Below is an example demonstrating how to use Katalon Orb to execute a test suite with the latest version of Katalon Studio.

```groovy
version: 2.1
orbs:
  katalon-studio: katalon/katalon-studio@23.0.2
workflows:
  build:
    jobs:
      - katalon-studio/run:
          version: latest
          command_arguments: >-
            -browserType='Chrome' -retry=0 -statusDelay=15 -testSuitePath='Test
            Suites/TS_RegressionTest'
```

In case you prefer setting up the integration manually, you can refer to the section below.

<details><summary>E2E testing integration with CircleCI</summary>
<p>

Credit to [Auksė Žirgulė](https://www.linkedin.com/in/auksezirgule/) - QA Lead at Hostinger International. The original article is available [here](https://www.linkedin.com/pulse/katalon-studio-e2e-testing-integration-circleci-auks%C4%97-%C5%BEirgul%C4%97/).

## Introduction to CircleCI

CircleCI is a continuous integration server where every commit executes an automated build and test. In this case, automated tests are integrated into a shared repository, can be configured to run at specific times and managed by all team members. You can read more about CircleCI features on the [official website](https://circleci.com/).

## The most important thing - config.yml file

To run Katalon tests on CircleCI, you need to:

- Have a repository on GitHub or [create a new one](https://help.github.com/en/articles/create-a-repo);

- Add .yml file into .circleci folder (keep in mind that a folder with a period will be hidden by default) and commit to your GitHub repository.

Here you can see an example of config.yml file that you need to add to the .circleci folder and commit to your GitHub repository together with your tests. Pay attention to folder structure - .circleci should be in the Katalon Studio Project Folder.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integration-circleci/1-command.png)

Keep in mind that this configuration can be changed according to your preferences. I run my tests from TestSuitCollection folder so I added a command option -testSuiteCollectionPath=<path>, but if you want to run your tests from Test Suite, you should use -testSuitePath=<path>. You can find more information on general Katalon Studio options [here](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#execute-katalon-in-cmd).

When the config.yml file is ready and committed, you should go to the CircleCI platform and follow these steps:

- Sign up to the CircleCi platform (use your GitHub account to join the platform);

- Add and set up your project (the initial condition is - you must have GitHub repository permissions to view or follow associated projects). After registering to circleci you should be able to see this window (see the image below). You just need to click **Set Up Project** and **Start Building** (you do not need to configure a yml file because you have done it previously).

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integration-circleci/2-set-up-project.png)

After “start building” is clicked and at least one change pushed, you will be able to see a job’s status - running, success, failed, on hold, queued. You can see more details by clicking on the status and expanding section details or moving and tracking your test result report on Katalon TestOps (read the chapter below on how to do that).

## Upload results to Katalon TestOps

To analyze test results, you can integrate Katalon Studio with Katalon TestOps. This way you are able to get generated and detailed reports after every completed build in CircleCI. In order to send your test results to Katalon Studio TestOps you need to:

- Navigate and Login/Sign Up to Katalon TestOps;
- Open your Katalon Studio Project and Click ‘Project’ from the main menu;
- Select Settings -> Katalon TestOps -> Fill in Katalon TestOps information;
- Click Apply -> Ok;
- Return to Katalon TestOps;
- Create a new project;
- Set Up Grid to automatically send results to TestOps;

Congratulations - now your test results should be able to reach Katalon TestOps after every completed build.

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
</p>
</details>
