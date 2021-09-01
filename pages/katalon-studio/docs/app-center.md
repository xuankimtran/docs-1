---
title: "App Center Integration"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/app-center.html
---

**Sideload** is built for executing Katalon Studio tests on App Center Test. [App Center Test](https://docs.microsoft.com/en-us/appcenter/test-cloud/) only supports running tests using supported frameworks such as [Appium tests written in Java with JUnit](https://docs.microsoft.com/en-gb/appcenter/test-cloud/preparing-for-upload/appium); hence, Katalon users cannot execute their tests on App Center Test directly.

You can execute your Katalon test scripts with devices provided on App Center Test by using **sideload** to package Katalon projects in JUnit format. This tutorial shows you how to integrate with App Center Test using **sideload**. We also provide the **KatalonDemoProject** as a usage example.

## Integrate with App Center

> **Requirement**
>
> * An active [Katalon Runtime Engine](https://docs.katalon.com/katalon-studio/docs/license.html#katalon-runtime-engine) license
> * A [Katalon API Key](https://docs.katalon.com/katalon-analytics/docs/ka-api-key.html)
> * Katalon Studio version 7.6.0 onwards
> * [Apache Maven](https://maven.apache.org/download.cgi) version 3.3.9 or later installed
> * [NodeJS](https://nodejs.org/es/blog/release/) version 6.3 or later installed
> * [App Center CLI](https://docs.microsoft.com/en-us/appcenter/cli/#installation) installed and logged in

To run your Katalon projects with App Center Test, you have to configure your Katalon project and make updates in **sideload** properly.

### Configure your Katalon Project

Before executing any test, you need to manually create an **Appium Driver instance** and set it as the currently used instance in Katalon Studio.

1. Open your project in Katalon Studio. At the beginning of your test script or in the `Before Test Case` listener, input the following snippet:

```groovy
import com.kms.katalon.core.appium.driver.AppiumDriverManager
import org.openqa.selenium.remote.DesiredCapabilities
import io.appium.java_client.MobileElement
import io.appium.java_client.android.AndroidDriver
import io.appium.java_client.remote.MobileCapabilityType

String remoteServerUrl = System.getenv('XTC_SERVICE_ENDPOINT_APPIUM') + 'wd/hub'

DesiredCapabilities capabilities = new DesiredCapabilities();
capabilities.setCapability(MobileCapabilityType.DEVICE_NAME, 'S10 Plus')
capabilities.setCapability(MobileCapabilityType.PLATFORM_NAME, 'android')
capabilities.setCapability('appActivity', 'com.hmh.api.ApiDemos')
capabilities.setCapability('appPackage', 'com.hmh.api')
capabilities.setCapability('appWaitActivity', '*')
capabilities.setCapability(MobileCapabilityType.AUTOMATION_NAME, AppiumDriverManager.UIAUTOMATOR2)
capabilities.setCapability('autoGrantPermissions', true)

AndroidDriver<MobileElement> driver = new AndroidDriver<MobileElement>(new URL(remoteServerUrl), capabilities)
AppiumDriverManager.setDriver(driver)
```

2. Change the [desired capabilities](http://appium.io/docs/en/writing-running-appium/caps/) corresponding to your app.

    Since you have created a custom Appium driver, you need to comment out or remove all the `Mobile.startApplication(...)` or `Mobile.startExistingApplication(...)` in your current test cases.

3. Package your Katalon project into a **.zip** file.

### Update sideload

1. Clone or download **sideload** from our repository: [Katalon Studio sideload](https://github.com/katalon-studio/sideload).

2. Inside sideload, place your Katalon Project .**zip** file in this directory: `src/test/resources`.

3. Configure sideload.

    There are two ways to update sideload for you to choose:

    * Configure .bat file: `upload.sh/upload.bat`
    * Configure .java file: `src/test/java/com/katalon/sideload/SideloadTest.java`

    > **Notes**
    >
    > If both files contain the configuration, the configuration in the **.bat** file will be prioritized.

    **Configure .bat file**

    Open the upload.bat file. Change the following variables as your context:

    * `<app_name>`: Your App Name on App Center
    * `<device_id/device_name>`: Device ID or Device Name on App Center. To find your Device ID or Device Name on App Center, go to `Test > Device sets`.
    * `<path_to_app_file>`: The App to upload to App Center
    * `<katalon_version>`: The version of Katalon Studio used to execute. Left blank or set as "latest" to run with the latest version of Katalon Studio.
    * `<katalon_project_package_file>`: Your package file
    * `<katalon_project_path>`: Relative path of Katalon project's folder inside the  `zip`  package
    * `<katalon_execute_args>`: The arguments part of your Katalon run command
        * The argument `browserType` must be set as `"Chome"`
        * The argument `projectPath` must be excluded from this parameter
        * For more arguments, refer to [Command Syntax](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#general-options)

    For example:

      ``` groovy
      appcenter test run appium ^
      --app "katalon/Sideload" ^
      --devices "katalon/nexus" ^
      --app-path "apps/APIDemos.apk" ^
      --test-series "master" ^
      --locale "en_US" ^
      --build-dir target/upload ^
      --test-parameter "test_env=KATALON_VERSION=" ^
      --test-parameter "test_env=KATALON_PROJECT_PACKAGE_FILE=KatalonDemoProject.zip" ^
      --test-parameter "test_env=KATALON_PROJECT_PATH=" ^
      --test-parameter "test_env=KATALON_EXECUTE_ARGS=-retry=0 -testSuitePath=""Test Suites/Regression Tests"" -executionProfile=default -browserType=Chrome -apiKey=""12345678-aaaa-bbbb-cccc-91011121314"""
      ```

    **Configure .java file**

      Open `src/test/java/com/katalon/sideload/SideloadTest.java`, find the `SideloadTest` section and change the following variables as your context:

      * **API_KEY**: Your API key
      * **KATALON_VERSION**: The version of Katalon Studio used to execute. Left blank or set as "latest" to run with the latest version of Katalon Studio.
      * **KATALON_PROJECT_PACKAGE_FILE**: Your package file<br>
      * **KATALON_PROJECT_PATH**: Path to the Katalon project inside the package file.<br>
      * **KATALON_EXECUTE_ARGS**: The arguments part of your Katalon run command<br>
        * The argument `browserType` must be set as `"Chome"`
        * The argument `projectPath` must be excluded from this parameter
        * For more arguments, refer to [Command Syntax](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#general-options)

    For example:

    ``` java
    public class SideloadTest {
    /**
     * Your Katalon API Key
     */
    private static final String API_KEY = "12345678-aaaa-bbbb-cccc-91011121314";

    /**
     * Katalon version which will be used to run the test
     */
    private static final String KATALON_VERSION = ""; // Leave it blank to always use the latest version

    /**
     * The package file under the "src/test/resources" folder
     */
    private static final String KATALON_PROJECT_PACKAGE_FILE = "KatalonDemoProject.zip";

    /**
     * Path to the katalon project inside the package file.
     * If not specified it will use the same name with the package file.
     * (In this case, it is: KatalonDemoProject)
     */
    private static final String KATALON_PROJECT_PATH = "";

    /**
     * Katalon arguments
     * @apiNote Remember to always set "browserType" to "Chrome". This will prevent Katalon from inject inappropriate configurations in execution.
     * @apiNote Besides, you do not need to include project path in the argument list.
     */
    private static final String KATALON_EXECUTE_ARGS = String.format("-retry=0 -testSuitePath=\"Test Suites/Regression Tests\" -executionProfile=default -browserType=Chrome -apiKey=\"%s\"", API_KEY);
    ```

4. To pack your sideload project, execute the file `package.bat`/`package.sh`.

5. Upload sideload:
    * Before uploading, you should configure in the file `upload.sh`/`upload.bat`.
    * To upload and run your sideload project on the App Center, execute  the file `upload.sh`/`upload.bat`.

## Executing KatalonDemoProject

This section provides you a usage example on how to upload **KatalonDemoProject** packaged in JUnit by **sideload** and start a test run in App Center Test.

1. Clone or download **sideload** from our repository: [Katalon Studio sideload](https://github.com/katalon-studio/sideload).
2. Open the workspace of the usage example project by following the path: `src/test/resources/KatalonDemoProject.zip`.

    On App Center Test, create and start a new test run. See Microsoft documentation: [Starting a test run](https://docs.microsoft.com/en-us/appcenter/test-cloud/starting-a-test-run#new-test-run).

    * Device: Android 7.1.1 or prior. Ex: Motorola Nexus 6
    * Test framework: Appium

3. To pack your sideload project, execute the file `package.bat`/`package.sh`.

4. Upload sideload:

    * Before uploading, you should configure in the file `upload.sh`/`upload.bat`.
    * To upload and run your sideload project on the App Center, execute  the file `upload.sh`/`upload.bat`.

    You can view test reports on App Center Test. See Microsoft documentation: [Test reports](https://docs.microsoft.com/en-us/appcenter/test-cloud/test-reports).