---
title: "Flutter-based application testing with custom SetText keyword" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/flutter-based-application-testing.html 
description: 
---

Flutter is a UI toolkit for building applications for mobile, web, desktop, and embedded devices from a single codebase.

> Known limitation:
>
> Katalon Studio partially supports Flutter-based applications. If elements of a Flutter-based app are rendered as in a native app, Katalon Mobile Recorder can capture elements. If those elements are rendered in web view, which is a use case of a hybrid Mobile app, Katalon Studio partially supports elements capturing.

You can use Mobile keywords to automate your Flutter-based application. However, Katalon Mobile Spy and Recorder currently cannot detect **EditText** elements in Flutter-based applications. This tutorial provides a workaround to automatically test the Flutter-based application using a custom SetText keyword package.

## Set up Appium Flutter Driver

To set up Katalon Studio for Flutter-based app mobile automated testing, you need to use Appium Flutter Driver. Appium Flutter Driver is a test automation tool for Flutter apps on multiple platforms/OSes. Appium Flutter Driver is part of the Appium mobile test automation tool maintained by the community.

You can clone or download Appium Flutter Driver at Appium's repository on GitHub: [Appium Flutter Driver](https://github.com/appium-userland/appium-flutter-driver).

To use Appium Flutter Driver with Katalon Studio, follow these requirements:

* Your Flutter App Under Test (AUT) must be compiled in `debug` or `profile` mode because Flutter Driver does not support running in release mode.
* Your Flutter AUT has `enableFlutterDriverExtension()` before `runApp` in source code.

In Katalon Studio, specify this desired capability to let Katalon Studio run with Appium Flutter Driver: Go to **Project Settings > Desired Capabilities > Mobile**. Select Android or iOS, then create a desired capabilities, which value is `Flutter`.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/flutter-based-application-testing/desired-capabilities.png" alt="desired capabilities" width=70%>

## Run Flutter-based application test with custom SetText keyword

1. In Katalon Studio, open your project and create a new test case. Record your mobile testing script. Use [Tab keyword](https://docs.katalon.com/katalon-studio/docs/mobile-tap.html) on elements **EditText - Email** and **EditText - Password**, then click **Save**.

2. In the **Tests Explorer** section on the left side of Katalon Studio, navigate to the **Keywords** folder and create a new keyword package. Name the package **com.kms.katalon.core.mobile.keyword.builtin**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/flutter-based-application-testing/create%20package.png" alt="create package" width=70%>

3. Right click on the **com.kms.katalon.core.mobile.keyword.builtin** package and create a new keyword named **SetTextKeyword**. See also: [Introduction to Custom Keywords](https://docs.katalon.com/katalon-studio/docs/introduction-to-custom-keywords.html).

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/flutter-based-application-testing/create%20keyword.png" alt="create Class name" width="70%">

    In the **SetTextKeyword.groovy** file, copy and paste the following script and save it.

    **<details><summary>SetTextKeyword.groovy script</summary>**

    ```groovy
    package com.kms.katalon.core.mobile.keyword.builtin

    import java.text.MessageFormat

    import org.openqa.selenium.InvalidElementStateException
    import org.openqa.selenium.Keys
    import org.openqa.selenium.WebElement
    import org.openqa.selenium.interactions.KeyInput
    import org.openqa.selenium.interactions.Sequence;

    import com.kms.katalon.core.annotation.internal.Action
    import com.kms.katalon.core.configuration.RunConfiguration
    import com.kms.katalon.core.exception.StepFailedException
    import com.kms.katalon.core.helper.KeywordHelper
    import com.kms.katalon.core.keyword.internal.SupportLevel
    import com.kms.katalon.core.mobile.constants.StringConstants
    import com.kms.katalon.core.mobile.keyword.internal.MobileAbstractKeyword
    import com.kms.katalon.core.mobile.keyword.internal.MobileDriverFactory
    import com.kms.katalon.core.mobile.keyword.internal.MobileKeywordMain
    import com.kms.katalon.core.model.FailureHandling
    import com.kms.katalon.core.testobject.TestObject
    import com.kms.katalon.selenium.util.SeleniumKeysUtil;

    import groovy.transform.CompileStatic
    import io.appium.java_client.AppiumDriver

    @Action(value = "setText")
    public class SetTextKeyword extends MobileAbstractKeyword {

        @CompileStatic
        @Override
        public SupportLevel getSupportLevel(Object ...params) {
            return super.getSupportLevel(params)
        }

        @CompileStatic
        @Override
        public Object execute(Object ...params) {
            TestObject to = getTestObject(params[0])
            String text = (String) params[1]
            int timeout = (int) params[2]
            FailureHandling flowControl = (FailureHandling)(params.length > 3 && params[3] instanceof FailureHandling ? params[3] : RunConfiguration.getDefaultFailureHandling())
            setText(to,text,timeout,flowControl)
        }

        @CompileStatic
        public void setText(TestObject to, String text, int timeout, FailureHandling flowControl) throws StepFailedException {
            MobileKeywordMain.runKeyword({
                KeywordHelper.checkTestObjectParameter(to)
                timeout = KeywordHelper.checkTimeout(timeout)
                WebElement element = findElement(to, timeout * 1000)
                if (element == null) {
                    MobileKeywordMain.stepFailed(MessageFormat.format(StringConstants.KW_MSG_OBJ_NOT_FOUND, to.getObjectId()), flowControl, null, true)
                    return
                }
                element.clear()
                try {
                    element.sendKeys(text.toString())
                } catch (InvalidElementStateException e) {
                    AppiumDriver driver = MobileDriverFactory.getDriver()
                    element.click()
                    KeyInput keyboard = new KeyInput("keyboard");
                    Sequence sendKeys = new Sequence(keyboard, 0);

                    for (int i = 0; i < text.length(); i++) {
                        String c = text.charAt(i).toString()

                        sendKeys.addAction(keyboard.createKeyDown(c.codePointAt(0)));
                    }

                    driver.perform(Arrays.asList(sendKeys));
                }
                String readableText = SeleniumKeysUtil.getReadableText(text)
                logger.logPassed(MessageFormat.format(StringConstants.KW_LOG_PASSED_TEXT_HAS_BEEN_SET_TO_ELEMENT, [
                    readableText,
                    to.getObjectId()] as Object[]))
            }, flowControl, true, to != null ? MessageFormat.format(StringConstants.KW_MSG_FAILED_TO_SET_ELEMENT_TEXT, to.getObjectId()) : StringConstants.KW_MSG_FAILED_TO_SET_ELEMENT_TEXT)
        }
    }
    ```

    </details>

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/flutter-based-application-testing/KS-flutter-based-application-testing-folder.png" alt="create custom keyword" width="100%">

4. In the toolbar, select **Window > Reset Perspective...**

5. Create a Test Case and switch to **Script** mode. Enter **Mobile.setText**, then select `setText(TestObject to, String text, int timeout, FailureHandling flowcontrol)`. See also: [[Mobile] Set Text](https://docs.katalon.com/katalon-studio/docs/mobile-set-text.html#description).

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/flutter-based-application-testing/KS-flutter-setText.png" alt="settext option" width=100%>

7. Run your Test Case and see if it passes successfully.

## How to switch contexts?

For the test engine to know whether you want to automate the native aspects of the app or the web views, Katalon Studio provides two keywords that help you switch contexts:

* [Switch to Native](https://docs.katalon.com/katalon-studio/docs/mobile-switch-to-native.html)
* [Switch to WebView](https://docs.katalon.com/katalon-studio/docs/mobile-switch-to-web-view.html)

The following is a code sample that automates elements of the app:

``` groovy

Mobile.switchToWebView()
DriverFactory.changeWebDriver(MobileDriverFactory.getDriver())

TestObject cdmDetails = new TestObject()
cdmDetails.addProperty("id", ConditionType.EQUALS, "119")
WebUI.setText(cdmDetails, "123")

Mobile.switchToNative()
```
