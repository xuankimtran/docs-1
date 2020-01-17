---
title: "Mobile Testing with Kobiton Devices"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/integrate_with_kobiton.html
description: "Using Katalon Studio, you can easily execute automated tests on Kobiton’s devices, thanks to the built-in integration feature supported by Katalon Studio."
redirect_from:
    - "/katalon-studio/tutorials/integrate_with_kobiton.html"
---

You need to install the Kobiton Integration plugin and enable the integration. If you haven't configured the integration yet, please refer to [this document](https://docs.katalon.com/katalon-studio/docs/enable-kobiton-integration.html) for instructions.

Please follow the instructions to execute your Katalon Studio automation test with Kobiton mobile devices.

1\. Navigate to Kobiton Portal: [https://portal.kobiton.com](https://portal.kobiton.com) and log in with your username and password.

2\. In Kobiton, upload your app to [Kobiton App Repository](https://docs.kobiton.com/#managing-apps).![Kobiton App Repository](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/integrate_with_kobiton/Kobiton-App-Repository.png)

3\. From the Repository view, select 'more actions' and select **_Automation snippet._** Copy the app ID (the one in bold, for example, **_kobiton-store:184_** as shown below) and save it.  
![Automation snippet](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/integrate_with_kobiton/Automation-snippet.png)

4\. Click on the **Devices** menu and select your devices by "_Mark as favorite"._![Kobiton Devices menu](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/integrate_with_kobiton/Devices.png)

5\. In Katalon Studio, open your mobile test case and switch to the **Scripts** view. Locate this line of code:

```groovy
Mobile.startApplication(appPath,false).

```

Next, replace the `appPath` with the Kobiton **App ID** saved in Step 3, as shown below:

![replace the "appPath" with the Kobiton app id](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/integrate_with_kobiton/Kobiton-app-id.png)

```groovy
import static com.kms.katalon.core.testcase.TestCaseFactory.findTestCaseMobile.comment('Story: Verify correct alarm message')Mobile.comment('Given that user has started an application')'Get full directory\'s path of android application'

//def appPath = PathUtil.relativeToAbsolutePath(GlobalVariable.G_AndroidApp, RunConfiguration.getProjectDir())

Mobile.startApplication('kobiton-store:184', false)

Mobile.comment('And he navigates the application to Activity form')

Mobile.tap(findTestObject('Application/android.widget.TextView - App'), 10)

Mobile.tap(findTestObject('Application/App/android.widget.TextView-Activity'), 10)

Mobile.comment('When he taps on the Custom Dialog button')

Mobile.tap(findTestObject('Application/App/Activity/android.widget.TextView-Custom Dialog'), 10)

'Get displayed message on the dialog'

def message = Mobile.getText(findTestObject('Application/App/Activity/Custom Dialog/android.widget.TextViewCustomDialog'),10)

Mobile.comment('Then the correct dialog message should be displayed')

Mobile.verifyEqual(message, 'Example of how you can use a custom Theme.Dialog theme to make an activity that looks like a customized dialog, here with an ugly frame.')

Mobile.closeApplication()

```

6\. From the main toolbar, click on the drop-down menu of **Run**, and select the option to run with **Kobiton Device**.  
![run with Kobiton Device](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/integrate_with_kobiton/Run.png)

7\. On the Kobiton Favorite Devices screen, a list of **Favorite Devices** from _Step 4_ will be displayed in _Device Name_.  

Select your preferred device and click **Ok**.

You can also modify this list by updating your **Favorite Devices** from [https://portal.kobiton.com/devices](https://portal.kobiton.com/devices).

![Kobiton Favorite Devices](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/integrate_with_kobiton/Favorite-Devices.png)

8\. Once Katalon Studio is finished, automation test execution will be uploaded to Kobiton. Navigate to **Sessions** menu to view:
![automation test execution uploaded to Kobiton](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/integrate_with_kobiton/Sessions.png)
