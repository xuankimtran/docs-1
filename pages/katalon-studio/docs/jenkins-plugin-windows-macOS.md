---
title: "Use Katalon TestOps plugin for Jenkins on Window/MacOS"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/katalon-plugin-jenkins-window-macOS.html 
description: 
redirect from: 
    - "/katalon-studio/docs/jenkins-plugin-windows.html"
---

This tutorial shows you how to integrate Katalon with Jenkins on Windows and macOS via the **Katalon TestOps** plugin for Jenkins.

> Requirements:
> * An active Katalon Runtime Engine license. To learn more about activating the Katalon Runtime Engine license, you can refer to this document: [Activate Katalon License](https://docs.katalon.com/katalon-studio/docs/activate-license.html#activate-trial-license).

## Installation

Install Jenkins. Follow the instructions in the following Jenkins documents:
   - For Windows: [Windows](https://www.jenkins.io/doc/book/installing/windows/)
   - For macOS: [macOS](https://www.jenkins.io/doc/book/installing/macos/) 

## Execute Katalon Studio tests in Jenkins with the Katalon TestOps plugin
### Install the Katalon TestOps plugin

1. Install the **Katalon TestOps** plugin. Go to **Manage Jenkins > Manage Plugins > Available tab** and search for the **Katalon TestOps** plugin.

2. Select the plugin and click **Install without restart**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-plugin-windows/KS-JENKINS-Download-Katalon-Testops-plugin.png" width=70% alt="Install Katalon TestOps plugin">
### Upload your Katalon project on Jenkins

After installing the **Katalon TestOps** plugin, you can now start the Katalon Studio test in Jenkins. 

1. In the Jenkins Dashboard, go to **New Item** and create a **Freestyle project**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-plugin-windows/KS-JENKINS-Create-a-freestyle-project.png" width=70% alt="Create a new Freestyle project">

2. To upload your Katalon project on Jenkins, you can upload your Katalon project from a Git repository or your local workspace. Here, we use a Git repository. 

   - In the **Source Code Management** section, choose **Git**.
   - Enter your repository URL, then select branches to build, repository browser, and additional behaviors, if any.

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-plugin-windows/Picture4.png" width=70% alt="Upload Katalon project">
### Build your project

1. In the **Build** section, click **Add build step** and choose **Execute Katalon Studio Tests**. The **Execute Katalon Studio Tests** box opens, asking you to input the Katalon Runtime Engine version and command arguments.
   
2. Specify the Katalon Studio version you wish to execute with:

   - If you haven't downloaded Katalon Runtime Engine (KRE), you can input the KRE version you wish to execute with in the **Download Katalon Studio version** box. KRE will be downloaded and deployed automatically. You can retrieve the list of all releases on the Github repository: [Releases](https://github.com/katalon-studio/katalon-studio/releases).
   - If you want to use a pre-installed version, manually input the KRE version you have installed in the **Use pre-installed Katalon Studio** box with the following command line: ```<KRE stored folder>-<KRE pre-installed version>```. For example: ```/Users/yen.nguyen/Downloads/Katalon_Studio_Engine_MacOS-8.1.0```.
   
3. Input your command in the **Command arguments** box, for example:

   ``` groovy

   -browserType="Chrome" -retry=0 -statusDelay=15 -testSuitePath="Test Suites/TS_RegressionTest" -apikey=<YOUR_API_KEY>

   ```
   > Notices:
   >
   > When you use the **Katalon TestOps** plugin, you do not need to mention ```-noSplash``` and ```-runMode=console```.

   > Notes:
   > * From version 7.7.0 onwards, if you belong to more than one Organization subscribing to Runtime Engine licenses, you can choose which Organization validates your license usage with the following command line: `-orgID=<Katalon_OrgID>`.
   > * Make sure your current browser version is compatible with the KRE Webdriver version. To learn more about upgrading or downgrading WebDrivers, you can refer to this document: [Update or Downgrade WebDrivers](https://docs.katalon.com/katalon-studio/docs/update-or-downgrade-webdrivers.html#replace-a-webdriver).

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-plugin-windows/KS-JENKINS-Enter-command-line-in-freestyles-project.png" width=60% alt="Input command arguments">

4. After you are done with the configuration, click **Save**, then click **Build Now** to run the project.
   
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-plugin-windows/KS-JENKINS-Build-now.png" width=60% alt="Build your Jenkins project">

5. To view the console log, click on your current build on Jenkins and select **Console Output**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-plugin-windows/KS-JENKINS-console-output.png" width=60% alt="View console output">
### Troubleshoot empty videos recorded after running tests on Window

If you encounter an issue of having empty videos recorded after running your tests in Jenkins on Window, it is because the WebDriver hasn't launched during test execution. To fix this issue, please uninstall Jenkins of Windows services, and replace it by a DOS batch file containing the following codes:

```groovy
cd D:\Tools\Jenkins //path to Jenkins folder
java -jar --webroot=jenkins.war
```

_Credit to Sébastien Taniere and his [original topic](https://forum.katalon.com/t/video-is-empty-when-scenario-is-launched-by-katalon-runtime-trough-jenkins-windows-instance/43974)._


## See also

* [Execute Katalon Studio tests with Jenkins Pipeline Script (Jenkinsfile)](https://docs.katalon.com/katalon-studio/docs/execute-katalon-tests-with-jenkins-pipeline-script.html ).
