---
title: "Find Mobile Objects"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/locators_object_identification.html
redirect_from:
    - "/katalon-studio/tutorials/locators_object_identification.html"
---

## Locator Strategies for detecting a mobile object

Before version 7.6, Katalon Studio only supports the Attributes Selection Method that allows selecting an object’s properties to generate its selector. The generated selector can be XPATH selector or in some cases, Android UiSelector. From 7.6, Katalon Studio fully supports [selector strategies supported by Appium except for Android Data Matcher](http://appium.io/docs/en/commands/element/find-elements/index.html#selector-strategies), including:

1. **Accessibility ID**: it is the `accessibility-id` attribute of an object for XCUITest, and the `content-desc` attribute of an object for Android .

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-selector-strategies/accessibility_id.png" width="369">

2. **Class name**: for IOS it is the full name of the XCUI element and starts with XCUIElementType; for Android it is the full name of the UIAutomator2 class (e.g.: android.widget.TextView)

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-selector-strategies/class_name.png" width=358>

3. **ID**: native element identifier: `resource-id` for android; `name` for iOS.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-selector-strategies/id.png" width=371>

4. **Name**

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-selector-strategies/name.png" width=372>

5. **XPath** (not recommended due to performance issues)

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-selector-strategies/xpath.png" width=369>

6. **Image**: Locate an object by matching its image with a Base64 file

   Prerequisites:

   * Set up [Image-based Testing for Mobile](https://docs.katalon.com/katalon-studio/docs/mobile-image-based-testing.html)
   * An active Katalon Studio Enterprise license

   The element's image: <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-selector-strategies/img_general.png" width=68.5>

   The Base64-encoded string:
   
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-selector-strategies/image.png" width=366>

7. **Android UiAutomator**

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-selector-strategies/android_ui_automator.png" width=370>

8. **Android View Tag**

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-selector-strategies/view_tag.png" width=364>

9. **iOS Predicate String**

   > [Locate an object by iOS Predicate String](http://appium.io/docs/en/writing-running-appium/ios/ios-predicate/)

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-selector-strategies/ios_predicate_string.png" width=368>

10. **iOS Class Chain**

    > [Locate an object by iOS Class Chain](https://github.com/facebookarchive/WebDriverAgent/wiki/Class-Chain-Queries-Construction-Rules)

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-selector-strategies/ios_class_chain.png" width=365>

11. **Custom**

    >[Learn more](http://appium.io/docs/en/advanced-concepts/element-finding-plugins/)
   
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-selector-strategies/custom.png" width=370>

### In Script View

1. **Accessibility ID**

```java
import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject
import com.kms.katalon.core.testobject.MobileTestObject
import com.kms.katalon.core.testobject.MobileTestObject.MobileLocatorStrategy

MobileTestObject mobileObject = findTestObject("Object Repository/New Mobile Object")
mobileObject.setMobileLocatorStrategy(MobileLocatorStrategy.ACCESSIBILITY)
mobileObject.setMobileLocator("ImageView")
```

2. **Class name**

```java
import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject
import com.kms.katalon.core.testobject.MobileTestObject
import com.kms.katalon.core.testobject.MobileTestObject.MobileLocatorStrategy

MobileTestObject mobileObject = findTestObject("Object Repository/New Mobile Object")
mobileObject.setMobileLocatorStrategy(MobileLocatorStrategy.CLASS_NAME)
mobileObject.setMobileLocator("General")
```

3. **ID**

```java
import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject
import com.kms.katalon.core.testobject.MobileTestObject
import com.kms.katalon.core.testobject.MobileTestObject.MobileLocatorStrategy

MobileTestObject mobileObject = findTestObject("Object Repository/New Mobile Object")
mobileObject.setMobileLocatorStrategy(MobileLocatorStrategy.ID)
mobileObject.setMobileLocator("General")
```

4. **Name**

```java
import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject
import com.kms.katalon.core.testobject.MobileTestObject
import com.kms.katalon.core.testobject.MobileTestObject.MobileLocatorStrategy

MobileTestObject mobileObject = findTestObject("Object Repository/New Mobile Object")
mobileObject.setMobileLocatorStrategy(MobileLocatorStrategy.NAME)
mobileObject.setMobileLocator("General")
```

5. **XPath**

```java
import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject
import com.kms.katalon.core.testobject.MobileTestObject
import com.kms.katalon.core.testobject.MobileTestObject.MobileLocatorStrategy

MobileTestObject mobileObject = findTestObject("Object Repository/New Mobile Object")
mobileObject.setMobileLocatorStrategy(MobileLocatorStrategy.XPATH)
mobileObject.setMobileLocator("//XCUIElementTypeApplication/XCUIElementTypeWindow[1]/XCUIElementTypeOther[1]/XCUIElementTypeOther[1]/XCUIElementTypeOther[1]/XCUIElementTypeOther[1]/XCUIElementTypeOther[1]/XCUIElementTypeOther[1]/XCUIElementTypeOther[1]/XCUIElementTypeTable[1]/XCUIElementTypeCell[2]/XCUIElementTypeStaticText[1]")
```

6. **Image**

```java
import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject
import org.apache.commons.io.FileUtils
import com.kms.katalon.core.testobject.MobileTestObject
import com.kms.katalon.core.testobject.MobileTestObject.MobileLocatorStrategy

MobileTestObject mobileObject = findTestObject("Object Repository/New Mobile Object")
mobileObject.setMobileLocatorStrategy(MobileLocatorStrategy.IMAGE)
byte[] fileContent = FileUtils.readFileToByteArray(new File(imageFilePath))
mobileObject.setMobileLocator(Base64.getEncoder().encodeToString(fileContent))
```

7. **Android UiAutomator**

```java
import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject
import com.kms.katalon.core.testobject.MobileTestObject
import com.kms.katalon.core.testobject.MobileTestObject.MobileLocatorStrategy

MobileTestObject mobileObject = findTestObject("Object Repository/New Mobile Object")
mobileObject.setMobileLocatorStrategy(MobileLocatorStrategy.ANDROID_UI_AUTOMATOR)
mobileObject.setMobileLocator('new UiSelector().className("android.widget.TextView").text("General").resourceId("android:id/title").packageName("com.android.settings").enabled(true).clickable(false).longClickable(false).checkable(false).checked(false).focusable(false).focused(false).scrollable(false).selected(false).index(0)')
```

8. **Android View Tag**

```java
import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject
import com.kms.katalon.core.testobject.MobileTestObject
import com.kms.katalon.core.testobject.MobileTestObject.MobileLocatorStrategy

MobileTestObject mobileObject = findTestObject("Object Repository/New Mobile Object")
mobileObject.setMobileLocatorStrategy(MobileLocatorStrategy.ANDROID_VIEWTAG)
mobileObject.setMobileLocator("MY VIEW TAG")
```

9. **iOS Predicate String**:

```java
import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject
import com.kms.katalon.core.testobject.MobileTestObject
import com.kms.katalon.core.testobject.MobileTestObject.MobileLocatorStrategy

MobileTestObject mobileObject = findTestObject("Object Repository/New Mobile Object")
mobileObject.setMobileLocatorStrategy(MobileLocatorStrategy.IOS_PREDICATE_STRING)
mobileObject.setMobileLocator("type == 'XCUIElementTypeStaticText' AND enabled == 1 AND label == 'General' AND name == 'General' AND name == 'General'")
```

10. **iOS Class Chain**:

```java
import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject
import com.kms.katalon.core.testobject.MobileTestObject
import com.kms.katalon.core.testobject.MobileTestObject.MobileLocatorStrategy

MobileTestObject mobileObject = findTestObject("Object Repository/New Mobile Object")
mobileObject.setMobileLocatorStrategy(MobileLocatorStrategy.IOS_CLASS_CHAIN)
mobileObject.setMobileLocator("**/XCUIElementTypeStaticText[`enabled == 1 AND label == 'General' AND name == 'General' AND value == 'General'`]")
```

11. **Custom**

```java
import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject
import com.kms.katalon.core.testobject.MobileTestObject
import com.kms.katalon.core.testobject.MobileTestObject.MobileLocatorStrategy

MobileTestObject mobileObject = findTestObject("Object Repository/New Mobile Object")
mobileObject.setMobileLocatorStrategy(MobileLocatorStrategy.CUSTOM)
mobileObject.setMobileLocator("foo")
```

## Mobile Test Object's View

In versions before 7.6, a Mobile object's view is the same as a Web object's view, which is not intuitive and misleading for users to design a Mobile test object. From 7.6 onwards, Katalon Studio launches a new UI of Mobile Test Object's view that reflects our latest enhancements for better designing Mobile objects.

## Mobile Object Spy

In previous versions, you can capture and rename captured objects but cannot change a Mobile object’s locator nor verify and highlight them. From version 7.6, you can capture, edit, verify and highlight a captured object to optimize its locator.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-selector-strategies/object-properties.png" width=438>

The **Object Properties** section now allows:

* Editing locator and locator strategy of an object.
* Verifying and highlighting the object with the newly updated locator.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-selector-strategies/object-properties-1.png" width=451>

## Mobile Recorder

In previous versions, in Mobile Recorder you can stimulate Mobile actions but cannot add built-in actions like in Web Recorder. From version 7.6, Katalon Studio supports adding built-in and custom actions when recording.

The new UI is similar to the Windows Recorder.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-selector-strategies/mobile-recorder-1.png">

Recorded Actions:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-selector-strategies/recorded-actions.png" width=411>

Captured Objects:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-selector-strategies/captured%20object.png" width=399>

## Known Limitation

Katalon Studio currently doesn’t support [Android Data Matcher](http://appium.io/docs/en/commands/element/find-elements/index.html#selector-strategies) since Appium Java Client 7.1.0 doesn’t support Android Data Matcher.

See also:

* [Create and Manage Mobile Test Objects](https://docs.katalon.com/katalon-studio/docs/manage-mobile-test-object.html#create-a-test-object)
* [Parameterize Mobile Test Object](https://docs.katalon.com/katalon-studio/docs/parameterize-mobile-test-object-properties.html#usage-example)
