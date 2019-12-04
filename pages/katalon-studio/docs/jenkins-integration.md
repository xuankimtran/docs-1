---
title: "Jenkins Integration"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/jenkins-integration.html
redirect_from:
    - "/display/KD/Jenkins+Integration/"
    - "/display/KD/Jenkins%20Integration/"
    - "/x/XwAM/"
    - "/katalon-studio/docs/jenkins-integration/"
    - "/katalon-studio/tutorials/jenkins_ci_integration.html"

description:
---

This feature has been moved to [Jenkins plugin](https://docs.katalon.com/katalon-studio/docs/jenkins-plugin-windows.html).

<details><summary>Deprecated Content</summary>

Prerequisites
-------------

1.  Katalon Studio command to be used for console mode execution. Refer to section [Console Mode Execution](/display/KD/Console+Mode+Execution) for how to build up a Katalon command. Here is the basic command template:

    ```groovy
    katalon -runMode=console -projectPath="<YOUR PROJECT>" -reportFolder="Reports" -reportFileName="report" -retry=0 -testSuitePath=<YOUR TEST SUITE PATH> -browserType="Chrome"
    ```


> Your command should NOT include -noExit and -consoleLog parameters so that CI logs can be displayed directly from the job view

2. CI tool is installed and setup properly. In this example, we will use [Jenkins](https://jenkins.io/), which is a popular CI and easy to integrate with.

3. The command will invoke Katalon Studio for execution so a Katalon build is needed for each execution machine.

Configuration Steps
-------------------

1.  Create a New item in Jenkins
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-integration/Screen-Shot-2017-07-10-at-14.07.17.png)

2. Enter job name (e.g "Katalon Studio Tests"), and then choose "Freestyle Project"![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-integration/Screen-Shot-2017-07-10-at-14.08.54.png)

3. Add execution step

**Linux and mac OS**

Add "Execute Shell" step

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-integration/Screen-Shot-2017-07-10-at-14.11.26.png)

Paste in generated Katalon Studio command

```bash
./Katalon\ Studio.app/Contents/MacOS/katalon --args -runMode=console -projectPath="/Users/admin/Katalon Studio/Samples/Sample Project.prj" -reportFolder="Reports" -reportFileName="report" -retry=0 -testSuitePath="Test Suites/TS_RegressionTest" -browserType="Chrome"
```

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-integration/Screen-Shot-2017-07-10-at-16.28.34.png)

**Windows**

Add "Execute Windows batch command"

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-integration/Screen-Shot-2017-07-11-at-13.48.38.png)


Paste in generated Katalon Studio command.

```bash
katalon -runMode=console -projectPath="C:\Project\Sample Project.prj" -reportFolder="Reports" -reportFileName="report" -retry=0 -testSuitePath="Test Suites/TS_RegressionTest" -browserType="Chrome"
```

4. Check on 'Delete workspace before build starts' in current job configuration to prevent corrupted project folder after long run.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-integration/build-environment.png)

Exit Codes
----------

When you execute Katalon Studio command from CI , exit code will be generated as the output of your execution. You can use this exit code to know whether your execution is successful, passed or failed.
![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-integration/image2016-9-8-103A433A50.png)

Publish JUnit reports
---------------------

> Since Katalon Studio 6.1.5, please install [Basic Report](https://store.katalon.com/product/59/Basic-Report) plugin to use this feature.

From Katalon Studio 4.7, JUnit report is generated when you execute a test suite. In order for Jenkins to store , analyze and show results, please add '[Publish JUnit test result report](https://wiki.jenkins.io/display/JENKINS/JUnit+Plugin)' item.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-integration/Screen-Shot-2017-07-11-at-11.53.43.png)

Set the 'Test Report XMLs' value to your Reports folder to fetch all generated JUnit reports.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-integration/Screen-Shot-2017-07-11-at-11.52.37.png)

After executions from Jenkins job, click on '[Test Results Analyzer](https://wiki.jenkins.io/display/JENKINS/Test+Results+Analyzer+Plugin)' item

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-integration/Screen-Shot-2017-07-11-at-11.57.27.png)

All test executions from the folder you've specified will be summarized and displayed in visualize way.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-integration/Screen-Shot-2017-07-11-at-11.48.34.png)

</details>
