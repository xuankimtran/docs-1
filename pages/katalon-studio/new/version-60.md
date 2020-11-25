---
title: "Version History - 6.x"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/new/version-60.html
redirect_from:
    - "/katalon-studio/new/version-633/"
    - "/katalon-studio/new/version-633.html"
    - "/katalon-studio/new/version-630.html"
    - "/katalon-studio/new/version-630/"
    - "/katalon-studio/new/version-622/"
    - "/katalon-studio/new/version-622.html"
    - "/katalon-studio/new/version-620/"
    - "/katalon-studio/new/version-620.html"
    - "/katalon-studio/new/version-615/"
    - "/katalon-studio/new/version-615.html"
    - "/katalon-studio/new/version-613/"
    - "/katalon-studio/new/version-613.html"
    - "/katalon-studio/new/version-612/"
    - "/katalon-studio/new/version-612.html"
    - "/katalon-studio/new/version-611/"
    - "/katalon-studio/new/version-611.html"
    - "/katalon-studio/new/version-61.html"
    - "/katalon-studio/new/version-61/"
    - "/katalon-studio/new/version-606/"
    - "/katalon-studio/new/version-606.html"
    - "/katalon-studio/new/version-605/"
    - "/katalon-studio/new/version-605.html"
    - "/katalon-studio/new/version-60/"
description: Release notes v6.x
---
## Version 6.3.3

### Improvements

* Remove the SLF4J warning message in the execution log when running in Console mode.
* Add a menu item on Katalon Studio's main toolbar for manually updating WebDrivers.

### Fixes

* Bug: Cannot create or open a dynamic test suite.
* Bug: `Run from here` doesn't work if the script contains [Postfix](http://docs.groovy-lang.org/latest/html/documentation/core-operators.html#_unary_operators) expressions.

## Version 6.3.0 - 6.3.2

### New Features

* Support Dark theme in addition to the default Light theme. See [Using Katalon Studio in Dark theme](https://docs.katalon.com/katalon-studio/docs/dark-theme.html).
* Support spying, recording and executing the Mobile script on custom cloud-based testing tools; and an option to choose between AndroidDriver or iOSDriver when Appium is set as `Remote server type`. See [Testing Mobile Apps Using Custom Cloud Devices](/katalon-studio/docs/mobile-testing-apps-cloud-devices.html) and [Remote Desired Capabilities](https://docs.katalon.com/katalon-studio/docs/remote-desired-capabilities.html).
* Support testing existing applications on Android and iOS devices. See [[Mobile] Start Existing Application](/katalon-studio/docs/mobile-keyword-start-existing-apps.html) and [Spy and Record Utilities for testing an existing application](/katalon-studio/docs/mobile-spy-record-existing-apps.html).

### Improvements

* Allow Test Reports to be viewed directly in Test Suite and Test Suite Collection Views in Result Tab. See [Test Suite Report](https://docs.katalon.com/katalon-studio/docs/test-suite-report.html) or [Test Suite Collection Report](https://docs.katalon.com/katalon-studio/docs/test-suite-collection-report.html).
* Support sending custom headers in SOAP requests.
* Directly parameterize Global variables in Test Objects. See [Global Variables](https://docs.katalon.com/katalon-studio/docs/global-variables.html).
* Allow implementing variable binding without converting test data to strings. See [Enhanced Variable Binding](https://docs.katalon.com/katalon-studio/docs/bind-as-string.html#variable-binding-for-test-data-with-option-embind-into-test-case-as-stringem-enabled).
* Support implementing an annotation called BeforeTestDataBindToTestCase in test listener. See [[Quick tip] Enhanced Variable Binding](https://docs.katalon.com/katalon-studio/docs/bind-as-string.html).
* Support Move up and Move down items in the default profile. See [Global Variables](https://docs.katalon.com/katalon-studio/docs/global-variables.html).
* Support quickly setting up your devices by displaying sub-menus of Android, iOS and Kobiton devices in Mobile Spy and Recorder tool items.
* Enhancement: Remove the **-- disable-extensions** argument from Chrome Desired Capabilities.
* Support Chrome version 76.

### Fixes

* Bug: Test object references are displayed incorrectly when new test objects are created from the existing ones.
* Bug: The scroll bar disappears in the Variables section.
* Bug: Incorrectly detect and highlight Mobile Test Objects when using Mobile Recorder or Mobile Object Spy.
* Bug: Incorrectly detect Test Objects’ locations when using Mobile Recorder or Mobile Object Spy.
* Bug: Cannot record additional items when using Web Recorder on existing test cases.
* Bug: Cannot activate Katalon Studio after resetting the password.
* Bug: Cannot load test steps in Manual View of a test case when *Initially open Test Case in Script view* is set by default.
* Bug: Cannot run test cases with Microsoft Edge 18.0 on BrowserStack.
* Bug: Katalon Studio always uses Xpath as a default element locator instead of Web Locators defined by users.
* Bug: *Continue Recording* silently deletes WebService parameters.
* Bug: The new checkpoint dialog box is not resizable and does not display all UI elements on Windows 10.
* Bug: The Sender field is empty when users send an email.
* Bug: An issue related to running a test suite with too large test data.
* Bug: NullPointerException occurs when using Web Recorder on an empty test case.
* Bug: Global Variables initialization fails when an existing WebDrivers’ instance is used in a custom profile.
* Bug: "Bind to test case as string" checkbox in Test Data is always checked while a test suite is executed.
* Bug: Slow performance of adding Variables to test cases.
* Bug: HAR files fail to be logged when the **SendRequestAndVerify** keyword is used.
* Bug: The **TapAtPosition** keyword fails to run.

## Version 6.2.2

### Improvements

* Support sending emails from another email address in addition to the default username.

### Fixes

* Bug: Cannot save test cases when the Test Case default view is in Script Mode
* Bug: Cannot execute test cases with Microsoft Edge 18.17763.
* Bug: Cannot send emails with TLS Protocol.
* Bug: An open profile is required being saved when it is just reopened, and no modification has been made.

## Version 6.2.0 - 6.2.1

### Improvements

* Show plugins which failed to reload
* Support SSL client certificate
* Support Appium v1.12.1, iOS 12.2, Xcode 10.2
* Support overriding default WebDrivers per project
* Update selenium-standalone-server from 3.7.1 to 3.141.59
* Update appium-java-client from 5.0.0 to 7.0.0
* Remove embedded carthage, libimobiledevice, and ios-deploy

### Fixes

* Bug: Cannot send emails if the attachment is empty
* Bug: Cannot import Postman requests with protocol HTTP
* Bug: TimeoutException when evaluating variables for Web Service requests
* Bug: Cannot save a draft request to Object Repository
* Bug: Cannot edit build.gradle files
* Bug: [Linux] Icons on the toolbar aren't displayed
* Bug: [Linux] Katalon Studio UI hangs when selecting Keywords in Manual view
* Bug: Cannot filter files in Project Explorer using keywords containing uppercase characters
* Bug: Cannot import Postman collections containing requests with the same names
* Bug: Cannot import Postman collections with long folder names
* Bug: Cannot execute web testing projects on cloud mobile devices (e.g. Sauce Labs)
* Bug: Cannot import Postman collections containing requests with body information missing
* Bug: Cannot import Postman requests whose names are URLs
* Bug: Custom headers are not sent along with SOAP requests
* Bug: Postman collection's sub-folder structure was not preserved
* Bug: Katalon Studio is hanged when editing an argument type in Desired Capabilities dialog

## Version 6.1.3 - 6.1.5

### Plug-ins

* [**Test Suite Collection Scheduler Plugin**](https://store.katalon.com/product/74/Test-Suite-Collection-Scheduler): A plugin that lets Katalon Studio run a test suite collection at a specific time in the future.
* [**Katalon Studio Report Plugin**](https://store.katalon.com/product/59/Basic-Report): A plugin that replaces the current report feature of Katalon Studio. Starting from v6.1.5, the report feature is no longer available natively in Katalon Studio, users need to download this plugin to continue using this feature.

### Fixes and Improvements

*   Fixed a bug where Kobiton devices are duplicated.
*   Fixed a bug where Katalon Studio cannot be opened if a custom keyword plugin contains errors.
*   Fixed a bug where HAR files are not generated with the correct name.
*   Fixed a bug where Safari webdriver install requirements pop-up shows up before every test.
*   Fixed a bug where test execution crashes when failing to get recent projects.
*   Fixed a bug where executeJavaScript keyword  fails when there are 3 arguments.
*   Fixed a bug in Jira Plugin where Default JIRA Issue TypeType field in integration setting contains duplicated values.
*   Added some small UI improvements when selecting devices and app files.
*   \[BETA\] Added the capability to import Test Objects from Postman collection JSON file. Importable fields include Postman fields in Params, Headers, Body.
*   Added a scrollbar in dropdown when selecting execution profiles.
*   Added the capability to display all user folders/files in Tests Explorer.
*   Added the capability to allow configuration of plugin installlation location in Preferences -> Katalon -> Plugins.
*   Added the capability to use variables in XPaths when finding test objects.

## Version 6.1.2

### Fixes and Improvements

* Allowed users to disable auto-redirection for API test objects.
* Highlighted test steps that call `markFailed`.
* Fixed a bug that caused test cases to fail with status `Reason: BUG! exception in phase 'semantic analysis' in source unit`.
* Showed test case tags in HTML, CSV, and PDF reports.
* Added a tab to Search Dialog for searching test objects.
* Showed raw data of request and response when executing an API test object.
* Fixed a bug that caused the last step to by marked as `failed` if any previous steps had failed.
* Fixed an issue of API testing where POST request JSON Body content is disappeared.

### Build custom keywords with Settings

With this new feature, a **Settings** page under **Project Settings/Plugins** can be created for a custom-keyword plugin. This can be utilized to store project-scoped variables for users to customize.

#### Add Settings page

Custom Keyword Plugin declares the setting page UI in **katalon-plugin.json** with this sample:

    {
       "keywords": [],
       "configuration": {
          "settingId": "some id",
          "settingPage": {
             "name": "name",
             "components": [
                {
                   "key": "key1",
                   "type": "text",
                   "label": "My Label 1",
    	           "defaultValue":"My default value 1"
                },
                {
                   "key": "key2",
                   "type": "secret",
                   "label": "My Label 2"
                }, ...
             ]
          }
       }
    }


* **settingId**: id the setting file that stores user setting properties in the setting page. There is a file will generated to store user settings at location:

  `<Project dir>/settings/external/<settingId>.properties`

* **settingPage** : contains the following sub-properties
   * **name**: Name of the setting page
   * **components**: list of UI components
     * **key**:  key of the component
     * **label**:  label of the component
     * **type**:  type of the component ('text' or 'secret')
     * **defaultValue**:  default value of the component

#### Prepare to test

 1. Clone [https://github.com/katalon-studio/katalon-studio-excel-custom-keywords-plugin]
 2. **Open the project in Katalon Studio at least once**
 3. Modify katalon-plugin.json with this template

        {
           "keywords": ["com.katalon.plugin.keyword.excel.ExcelReadKeywords", "com.katalon.plugin.keyword.excel.ExcelWriteKeywords"],
           "configuration": {
              "settingId": "com.katalon.plugin.keyword.excel-keywords",
              "settingPage": {
                 "name": "Excel Keywords",
                 "components": [
                    {
                       "key": "username",
                       "type": "text",
                       "label": "Username"
                    },
                    {
                       "key": "password",
                       "type": "secret",
                       "label": "Password"
                    }
                 ]
              }
           }
        }

4. Build excel keyword project

   `gradle katalonPluginPackage`

   A jar file will be generated in **/build/libs** folder

5. Copy and paste the generated jar file to **Plugins** folder of a Katalon Studio project (Project A)

6. Open **Project A** and navigate to **Project Settings/Plugins/Excel Keywords**

7. Customize the settings as wish

#### Retrieve the setting values

The values can be retrieved in keyword script as the following sample:

```groovy
    import com.kms.katalon.core.configuration.RunConfiguration as RunConfiguration
    import com.kms.katalon.core.setting.BundleSettingStore as BundleSettingStore

    BundleSettingStore bundleSetting = new BundleSettingStore(RunConfiguration.getProjectDir(), '<setting_id>',
    true)
    println(bundleSetting.getString('username', ''))
    println(bundleSetting.getString('password', '')
```

## Version 6.1.1

### Fixes and Improvements

* Added a warning when executing CLI mode under the target project folder.
* Fixed an issue where Katalon Studio cannot reload plugins.
* Added the current version and commit ID to the Katalon Studio's window title bar.
* Updated chromedriver to version 73.0.3683.68
* Updated EdgeDriver to version 6.17134

### Auto-healing Smart XPath Plugin

* Fixed an issue where XPaths with incorrect syntax stop the healing process.
* Added screenshots of alternative XPaths' results to assist the review process.

### Package Test Listeners as plugins

* From Katalon Studio 6.1.1 Test Listeners can be packaged as plugins.
* For a sample plugin see https://github.com/katalon-studio/katalon-studio-result-summary-test-listeners-plugin.
* The only differences between Test Listeners and Custom Keywords plugins are in `build.gradle` and `katalon-plugin.json`:

`build.gradle`:
```groovy
sourceSets {
  main {
    groovy {
      srcDirs = ['Keywords', 'Libs', 'Test Listeners', 'Include/scripts/groovy']
    }
  }
}
```

`katalon-plugin.json`:
```json
{
	"keywords": [],
	"listeners": ["KatalonPluginResultSummary"]
}
```

## Version 6.1.0

### Custom Keyword Plugin

Introducing Custom Keyword Plugin for Katalon Studio v6.1.0 for collaboration.
Custom Keywords now can be shared among the project team or to the world via Katalon Store. Simply Create. Upload. and Share!

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-61/Window.png)

### Fixes and Improvements

* Fixed an issue where project having many GlobalVariables cannot be opened - [More details ](https://github.com/katalon-studio/katalon-studio/issues/74)
* Fixed merging Objects to Object Repository issue - [More details ](https://github.com/katalon-studio/katalon-studio/issues/103)
* Removed dialogs when Katalon Studio is closed - [More details ](https://forum.katalon.com/t/rate-us-pop-up-message/18830)
* Fixed an issue where RunConfiguration cannot be functioned - [More details ](https://forum.katalon.com/t/unable-to-apply-global-directory-file-storage-path-in-6-0-5/20747/12)
* Fixed an issue where the report is overlapped when running Test Suite Collection inCommand Line Mode - [More details ](https://github.com/katalon-studio/katalon-studio/issues/19)
* Fixed an issue where copied console log contains special characters - [More details ](https://forum.katalon.com/t/copy-paste-from-console-log/18458)
* Implemented a few adjustments on Katalon Studio UI
* Fixed an issue with loading Custom Keyword plugin - [More details ](https://forum.katalon.com/t/how-to-package-custom-keyword-as-plugin/20321/18?u=devalex88).

## Version 6.0.6

### Fixes and Improvements

* Fixed an issue where REST WS Object - URL field automatically added question mark right after saving
* Fixed an issue where recorder function is not working with Internet Explorer in Katalon Studio version 5.10.1
* Fixed an issue where script view for Profile variables is empty
* Provide more details in log error messages
* Fixed an issue where users can not set proxy settings to selenium grid for accessing applications behind the firewall
* Fixed overriding Global Variable for Test Suite Collection issue
* Fixed an issue where Test Suite Collection cannot be executed in CMD mode

## Version 6.0.5

### OAuth 2.0 Support

Since version 6.0.5, Katalon Studio supports OAuth 2.0 expanding Web Service testing capabilities. Most of the common grant types are supported including “Authorization code,” “Password Credentials,” “Client Credentials,” and “Refresh Token.”
[Learn more](https://docs.katalon.com/katalon-studio/docs/authorization-oauth2.html)

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/authorization-oauth2/5.png)

### Fixes and Improvements

* Fixed an issue where more than one keyword setText is displayed on Web Record dialog
* Fixed an issue where commented lines at the bottom of test script are accidentally deleted - [More details](https://forum.katalon.com/t/most-of-my-automation-script-got-deleted/16005/4)
* Fixed some minor bugs and made some enhancements for BDD
* Fixed Global variables issues - [More details](https://forum.katalon.com/t/groovy-error-unable-to-resolve-class-internal-globalvariable/9557/168)
* Allows users to create Web Service Object in code
* Fixed an issue where profiles are evaluated even though it is not in use
* Moved ScreenUtil from WebUIAbstractKeyword to ImageKeyword
* Display information log when using GlobalVariable, not in selected ExecutionProfile
* Fixed an issue where ScrollToText function does not work
* Fixed an issue where adding the value with multiple lines in the variable section can not be function(Global or Normal) - [More details](https://github.com/katalon-studio/katalon-studio/issues/46)
* Fixed an issue where commented lines at the bottom of test script are deleted accidentally

## Version 6.0

### Introduce Katalon Store Integration

Katalon Store is a platform that leads users to the world of amazing plugins for Katalon Studio. This is also a collaborative marketplace for both end-users and developers to build add-on products, in order to maximize Katalon Studio's test automation capabilities. Katalon Store website is available at www.store.katalon.com.  

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-60/3.png)
Each plugin in Katalon Store comes with a detailed description so that you can preview the functions and features before installing.

If you cannot find the suitable add-on to your wish, you are welcomed to be the publisher with the Publish A New Plugin and Manage Published Plugins functions.

### Download, Manage, and Search for Plugins from Your Katalon Studio

Directly linked to your Katalon Studio app., all of the installed plugins can be easily reloaded and managed from your local device. Learn more [here](http://docs-staging.katalon.com/store-staging/katalon-store/docs/user/getting-started.html)
![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-60/2.png)

### Install Executable JAR File Plugins

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-60/1.png)
Katalon allows you to install executable JAR plugins right on the Quick Access Toolbar. In case these JAR files are already available  on your computer, you can easily install them by navigating to **Plugin** > **Install Plugin**.

### Fixes and Improvements

* Fixed remembering chosen test cases issue in Test Case Browser model
* Fixed duplicating added test case to a test suite issue
* Allow to run a test suite with duplicated test cases using data binding
* Fixed an issue where Automatically check for new version does not work with unchecked
* Fixed an issue where SWTException thrown when clicking 'Capture Object'
* Fixed an issue on swipe command, losing objects references
* Fixed SwipeKeyword and TapAtPositionKeyword that didn't work properly
* Improve new project pop-up UI
