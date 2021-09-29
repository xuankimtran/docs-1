---
title: "AWS Device Farm Integration"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/aws-device-farm.html
---
**aws-device-farm-integration** is built for executing Katalon Studio tests on [AWS Device Farm](https://aws.amazon.com/device-farm/). AWS Device Farm only supports running tests using supported frameworks such as Appium. Hence, Katalon users cannot execute their tests on AWS Device farm directly. See this AWS document for further information:  [Working with Appium and AWS Device Farm](https://docs.aws.amazon.com/devicefarm/latest/developerguide/test-types-appium.html).

You can execute your Katalon test scripts with devices provided on AWS Device Farm by using **aws-device-farm-integration**. This tutorial shows you how to integrate with AWS Device Farm using **aws-device-farm-integration**. We also provide the **KatalonDemoProject** as a usage example.

## Example Katalon project

You can clone or download our sample project and iOS application here. This step is optional, you can still use your own project in this tutorial.

* Sample Katalon project: [KatalonDemoProject](https://github.com/katalon-studio-samples/aws-device-farm-integration/tree/main/aut/KatalonDemoProject)
* Sample iOS application: [Coffee Timer.ipa](https://github.com/katalon-studio-samples/aws-device-farm-integration/blob/main/aut/Coffee%20Timer.ipa)

> Notes:
>
> For CI/CD pipelines with Jenkins, clone or download from our repository: [Jenkins integration](https://github.com/katalon-studio-samples/aws-device-farm-integration/raw/main/docs/Jenkins-integration.MD).

## Integrate with AWS Device Farm

To run your Katalon project with AWS Device Farm, you have to configure your Katalon projects and make updates in the **aws-device-farm-integration**.

> Requirements:
>
> * An active Katalon Runtime Engine license.
> * Katalon Runtime Engine version 7.8.0 onwards.
> * [Apache Maven](https://maven.apache.org/download.cgi) version 3.3.9 onwards.
> * Java JDK 8 installed.

> Supported testing types and platforms:
>
> * Mobile app on Android
> * Mobile app on iOS
> * Web app on Android
>
> Web app on iOS is currently not supported.

### Configure your Katalon project

1. In Katalon Studio, open your desired Katalon Project. Prepare your Katalon test cases and test suites that can successfully run on your local device.

    Your mobile test case should start with the keyword: **Start Existing Application**. This is because AWS Device Farm already installs the application on devices under test before every run. To learn more about this mobile keyword, see [[Mobile] Start Existing Application](https://docs.katalon.com/katalon-studio/docs/mobile-keyword-start-existing-apps.html).

2. To change the desired capabilities corresponding to your app, open **Project Settings > Desired Capabilities > Remote**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/aws-device-farm-integration/project-settings.png" alt="configure desired capabilities" width=70%>

    * In **Remote server URL**, enter the Appium server URL: [http://127.0.0.1:4723/wd/hub](http://127.0.0.1:4723/wd/hub)
    * In **Remote server type**, select **Appium**.
    * In **Appium driver**, select **Android Driver** for Android devices or **iOS Driver** for iOS devices.

    Click **Add** to create a desired capability named `platformName` with the value `Android` for Android devices, or `iOS` for iOS devices.

    When you are done with the configuration, click **Apply and Close**.

    > Notes:
    >
    >For Android app testing, we need to add two extra desired capabilities: `appPackage: [app ID]` and `appActivity: [main activity name]`. The main activity can retrieve after uploading the app to AWS Device Farm.
    >
    > <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/aws-device-farm-integration/android-main-activity.png" alt=" Android main activity" width=50%>

3. Package your Katalon project into a .zip file.

### Update aws-device-farm-integration project

1. Clone or download **aws-device-farm-integration** from our repository: [Katalon Studio AWS Device Farm Integration](https://github.com/katalon-studio-samples/aws-device-farm-integration).
2. Inside **aws-device-farm-integration**, place your Katalon Project .zip file in this directory: `src/test/resources`.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/aws-device-farm-integration/zip-demo-project.png" alt="zip demo project" width=60%>

3. Open the `config.properties` file and change the following variables as your context:

    * `KATALON_VERSION`: Katalon Runtime Engine version.
    * `KATALON_PROJECT_PACKAGE_FILE`: Your package file.
    * `KATALON_EXECUTE_ARGS`: The arguments part of your Katalon run command
        * The `-browserType` argument must be set to `"Remote"`.
        * The `-reportFolder=$DEVICEFARM_LOG_DIR` argument allows us to download the execution report in Files/Customer Artifact of the AWS Device Farm Job.
        * For more arguments, refer to [Command Syntax](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#general-options).

    For example:

    ``` java

    KATALON_VERSION=8.1.0
    KATALON_PROJECT_PACKAGE_FILE=KatalonDemoProject.zip
    KATALON_EXECUTE_ARGS=-retry=0 -testSuitePath="Test Suites/Regression Tests" -executionProfile=default -browserType=Remote -reportFolder=$DEVICEFARM_LOG_DIR -apiKey=xxxxxxxx
    ```

4. To build the **aws-device-farm-integration**, at the folder **aws-device-farm-integration**, typing the below command in the terminal:

    `mvn clean package -DskipTests=true`

    When the build runs successfully, in the `target` folder, you will see a .zip file named `zip-with-dependencies.zip`.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/aws-device-farm-integration/2-build-project-with-maven.png" alt="build project with maven" width=40%>

## Configure a test project on AWS Device Farm

After preparing your Katalon Project, log in to the AWS Console and go to **Device Farm > Mobile Device: Projects** to create a new project.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/aws-device-farm-integration/3-create-test-project.png" alt="create test project" width=70%>

Input your **Project Name**, then hit **Create**.

This section guides you through 4 steps to configure your Katalon test project on AWS Device Farm.

1. **Choose application**

    Choose between **Mobile App** and **Web App** with the toggle button.

    * For mobile app testing, select **Mobile App**. Upload your application under test, which is an **.apk** file for an Android application or an **.ipa** file for an iOS application. Wait for the file to upload, then click **Next**.

        <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/aws-device-farm-integration/3-upload-mobile-app.png" alt="upload mobile app" width=70%>

    * For Web app testing, select **Web App**. Enter your run name, then click **Next**. The **Configure** page appears.

2. **Configure**

    In the **Setup test framework** section, click the _dropdown_ button and select `Appium Java JUnit`.

    In the **Selected File** section, upload the `zip-with-dependencies.zip` file.

    In the **Choose your execution environment**, choose **Run your test in a custom environment**, then click **Next**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/aws-device-farm-integration/3-upload-zip-file.png" alt="upload zip file" width=70%>

3. **Select Devices**

    Choose a suitable device pool, then click **Next**.

    The **Specify device state** page appears. Review other settings and change when needed, then click **Next**.

4. **Review and start Run**

    Review all of the configurations one last time, then click **Confirm and Start Run**.

    In AWS Console, a new test run is created. Its status is pending.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/aws-device-farm-integration/3-finish-creating-run.png" alt="finish creating run" width=70%>

    After the run starts, you can click on the test run name and a specified device to view the test status.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/aws-device-farm-integration/3-view-test-run-status.png" alt="view test run status" width=70%>

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/aws-device-farm-integration/3-test-runs-finish.png" alt="test runs finish" width=70%>

    After the run finishes, you can download the execution report at Files/Customer Artifacts.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/aws-device-farm-integration/3-download-report.png" alt="download report" width=70%>
