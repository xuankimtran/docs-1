---
title: "AWS Device Farm Integration"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/aws-device-farm.html
---
**AWS Device Farm Integration** is a Proof of Concept (PoC) built for executing Katalon Studio tests on [AWS Device Farm](https://aws.amazon.com/device-farm/). AWS Device Farm only supports running tests using supported frameworks such as Appium. Hence, Katalon users cannot execute their tests on AWS Device farm directly. See AWS documentation on [Working with Appium and AWS Device Farm](https://docs.aws.amazon.com/devicefarm/latest/developerguide/test-types-appium.html).

By using AWS Device Farm Integration, you can execute your Katalon test scripts with devices provided on AWS Device Farm. This tutorial shows you how to configure Katalon projects, AWS device farm, and AWS Device Farm Integration to execute the usage sample, which is KatalonDemoProject. Also, at the end of this tutorial, we provide some configurations that you can try to execute your Katalon projects on AWS Device Farm.

> Requirements:
>
> * An active Katalon Runtime Engine license.
> * Katalon Runtime Engine version 7.8.0 onwards.
> * [Apache Maven](https://maven.apache.org/download.cgi) version 3.3.9 or later installed.
> * Java JDK 8 installed.

> Supported testing types and platforms:
>
> * Mobile app on Android
> * Mobile app on iOS
> * Web app on Android
>
> Web app on iOS is currently not supported.

## Configure your Katalon project

1. Open your desired Katalon Project.

    Your mobile test case should start with **Start Existing Application** keyword because AWS Device Farm already installs the application on tested device before every run. To learn more about this mobile keyword, see [[Mobile] Start Existing Application](https://docs.katalon.com/katalon-studio/docs/mobile-keyword-start-existing-apps.html).

2. Open **Project Settings > Desired Capabilities > Remote**.

    * In **Remote server URL**, enter the Appium server URL: http://127.0.0.1:4723/wd/hub
    * In **Remote server type**, select **Appium**.
    * In **Appium driver**, select **Android Driver** for Android devices or **iOS Driver** for iOS devices.

    Click **Add** to create a desired capability named `platformName` with the value `Android` for Android devices; or `iOS` for iOS devices.

    * For Android app testing, we need to add extra desired capabilities `appPackage: [app ID]` and `appActivity: [main activity name]`. Main activity can retrieve after uploading app to AWS Device Farm.
        
        <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/aws-device-farm-integration/1-android-main-activity.png" alt=" Android main activity" width=70%>

    * Press **Apply and Close**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/aws-device-farm-integration/project-settings.png" alt="configure desired capabilities" width=70%>

## Configure aws-device-farm-integration project

1. Download and unzip [aws-device-farm-integration](https://github.com/katalon-studio-samples/aws-device-farm-integration)
2. Open this open in any IDE choice (Eclipse, VSCode,...)
3. Zip your Katalon project and put in `src/test/resources` folder
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/aws-device-farm-integration/2-zip-demo-project.png" alt="zip demo project" width=70%>

4. Open `config.properties` file and change the following variables as your context:

    * `KATALON_VERSION`: Katalon Runtime Engine version
        * (e.g. "8.1.0, 7.8.2")
    * `KATALON_PROJECT_PACKAGE_FILE`: Your package file
        * (e.g. "KatalonDemoProject.zip")
    * `KATALON_EXECUTE_ARGS`: The arguments part of your Katalon run command
        * (e.g. `"-retry=0 -testSuitePath="Test Suites/Regression Tests" -executionProfile="default" -browserType="Remote" -reportFolder=$DEVICEFARM_LOG_DIR -apiKey="xxxxxx"")`

        > Notes:
        > * The `-browserType` argument must be set to `"Remote"`.
        > * The `-reportFolder=$DEVICEFARM_LOG_DIR` argument allows us can download the execution report in Files/Customer Artifact of the AWS Device Farm Job

5. To build the **aws-device-farm-integration**, at the folder **aws-device-farm-integration-main**, typing the below command in terminal:

`mvn clean package -DskipTests=true`

If the build runs successfully, you will see a zip name `zip-with-dependencies.zip` in the target folder. We will use this file for the next step.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/aws-device-farm-integration/2-build-project-with-maven.png" alt="build project with maven" width=40%>

## Configure test project on AWS Device Farm

1. In AWS Console, create or click on an existing project.
<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/aws-device-farm-integration/3-create-test-project.png" alt="create test project" width=70%>

2. click **Create a new run**.
3. The **Choose Application** page appears.

    * For Mobile app testing, select **Mobile App** tab and upload your tested application (.apk for Anroid application and .ipa for iOS application). When the app uploaded successfully, click **Next**.

        <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/aws-device-farm-integration/3-upload-mobile-app.png" alt="upload mobile app" width=70%>

    * For Web app testing, select **Web App**. Enter your run name, then click **Next**.

4. The **Configure** page appears. In the **Setup test framework** section, click the _dropdown_ button and select `Appium Java JUnit`. Upload the `zip-with-dependencies.zip` that was created from Maven in the previous step. In the **Chooose your execution environment**, choose **Run your test in a custom environment**, then click **Next**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/aws-device-farm-integration/3-upload-zip-file.png" alt="upload zip file" width=70%>

5. The **Select devices** page appears. Choose a suitable device pool then click **Next**.
6. The **Specify device state** page appears. Review other settings and change when needed then click **Next**.
7. The **Review and start run** page appears. Review all of configurations one last time then click **Confirm and Start Run**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/aws-device-farm-integration/3-finish-creating-run.png" alt="finish creating run" width=70%>

8. A run already starts, we can click on test run name and a specified device to view the test status.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/aws-device-farm-integration/3-view-test-run-status.png" alt="view test run status" width=70%>

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/aws-device-farm-integration/3-test-runs-finish.png" alt="test runs finish" width=70%>

    After the run finishes, we can download the execution report at Files/Customer Artifacts

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/aws-device-farm-integration/3-download-report.png" alt="download report" width=70%>

## Examples Katalon project and AUTs

* Sample Katalon project in `aut/KatalonDemoProject`
* Sample iOS application in `aut/Coffee Timer.ipa`

## CI/CD pipelines
[Jenkins integration](https://github.com/katalon-studio-samples/aws-device-farm-integration/raw/main/docs/Jenkins-integration.MD)
