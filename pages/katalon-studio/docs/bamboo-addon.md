---
title: "Bamboo Add-on"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/bamboo-addon.html
redirect_from:
    - "/katalon-studio/docs/bamboo+plugin/"
    - "/katalon-studio/docs/bamboo-plugin.html"
    - "/katalon-studio/docs/bamboo-integration/"
    - "/katalon-studio/docs/bamboo-integration.html"
description:
---
> Katalon TestOps CI is an easier way to execute Katalon Studio tests remotely or schedule remote Katalon Studio execution. [Learn more](https://docs.katalon.com/katalon-analytics/docs/kt-remote-execution.html)

The Katalon DevOps for Bamboo plugin enables you to download, deploy and execute Katalon Studio tests on Bamboo CI server automatically. Try it for free on [Atlassian Marketplace](https://marketplace.atlassian.com/apps/1220235/katalon-devops-for-bamboo).

## Prerequisites

* You need an active Katalon Runtime Engine license.
* You need Bamboo administrative permission to configure the integration.

## Install the Add-on

1. Log into your Bamboo instance as an admin.
2. Click **Administration** and select **Manage Apps**.
3. Click **Find new apps** from the left-hand side of the page.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/bamboo-integration/find-apps.png" width="117" height="">

4. Locate **Katalon for Bamboo** via search.
5. Click **Try it free** to start your trial or **Buy now** to purchase a license for executing Katalon Tests.
6. Enter your information and click **Generate license** when redirected to MyAtlassian.
7. Click **Apply license**.

## Configure the integration

Once you have installed the plugin, you will need to configure **Execute Katalon Studio Tests** task to complete the integration.

1. Create and configure a new plan in Bamboo. Read more about how to create a new plan [here](https://confluence.atlassian.com/bamboo/creating-a-plan-289276868.html).

2. Add **Execute Katalon Studio Tests** to your jobs of the newly created plan.

    * In **Tasks**, click **Add task**.
    * In the **Task types** window, locate **Execute Katalon Studio Tests** via search or find it under the Tests category.
    * Add **Execute Katalon Studio Tests** to your job list.
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/bamboo-integration/bamboo-tasktypes.png)

3. Configure the **Execute Katalon Studio Tests** task and click **Save** to create it.
    
    * **Download Katalon version**: Specify the Katalon Studio (prior to 7.0) or Katalon Runtime Engine (7.0+) that is downloaded automatically to execute the tests. Or

    * **Use pre-installed Katalon Studio**: Provide a link to Katalon Studio (prior to 7.0) or Katalon Runtime Engine (7.0+) app that has been already installed.

    * **Command Arguments**: you can enter the arguments directly in the text area or copy and paste the generated command from Katalon Studio.

      > Please remove any irrelevant argument such as `-runmode`. See [Command Arguments in Common Configuration](https://docs.katalon.com/katalon-studio/docs/common-configuration.html#command-arguments) for more details.

      ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/bamboo-integration/command.png)

      For the list of supported Katalon command syntax and how to generate command, please read more [here](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html).

    * **Xvfb-run configuration**: Learn more [here](http://manpages.ubuntu.com/manpages/xenial/man1/xvfb-run.1.html). If you are not sure, only change the resolution 1024x768x24 and leave other options as-is.

## Artifacts

If you want to keep Katalon Studio artifact from the build, you can specify the **Copy Pattern** as `Reports/**/*.*`

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/bamboo-integration/bamboo-artifactdefinition.png)

After a build, execution log files created by Katalon Studio are stored under the **Artifacts** tab.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/bamboo-integration/bamboo-viewartifact.png)

