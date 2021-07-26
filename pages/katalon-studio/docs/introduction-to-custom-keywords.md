---
title: "Introduction to Custom Keywords" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/introduction-to-custom-keywords.html 
redirect_from:
    - "/display/KD/Introduction+to+Custom+Keywords/"
    - "/display/KD/Introduction%20to%20Custom%20Keywords/"
    - "/x/8gAM/"
    - "/katalon-studio/docs/introduction-to-custom-keywords/"
    - "/display/KD/Define+custom+keywords/"
    - "/katalon-studio/tutorials/create_custom_keyword.html"
    - "/katalon-studio/tutorials/create-custom-keyword/"
description: 
---
In addition to built-in keywords, you can define custom keywords to extend the capabilities of Katalon Studio. Once created, custom keywords can be used when implementing test cases, just like other built-in keywords.

## Create a Package

A _package_ is a namespace that organizes a set of related classes and interfaces. Because software written in the Java programming language or similar languages can be composed of hundreds or _thousands_ of individual classes, it makes sense to keep things organized by placing related classes and interfaces into packages.

1. Select **File > New > Package** from the main menu. The **New Keyword Package** dialog is displayed. Enter a name for your package and click **OK**.

   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/introduction-to-custom-keywords/image2017-2-6-153A353A6.png)

2. A new package is created under the **Keywords** folder in Tests Explorer accordingly.

   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/introduction-to-custom-keywords/image2017-2-6-153A363A13.png)

## Create a Custom Keyword

1. Select **File > New > Keyword** from the main menu. The **New Keyword** dialog is displayed. Enter a name for your keyword and specify a **package** for the keyword. Click **OK**.

   By default, a class name cannot start with a number, contain spaces, or have special characters. The Java naming convention suggests creating a class name using a noun or a noun phrase, with the first letter of each word capitalized, to better manage the project.

    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/introduction-to-custom-keywords/image2018-4-2-143A373A16.png)

    > You can generate sample custom keywords for Web, Mobile, and API Testing. Refer to [this guide](https://docs.katalon.com/katalon-studio/docs/sample-custom-keywords.html).

2. A new keyword is created under the specified **package** accordingly.

    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/introduction-to-custom-keywords/image2017-2-6-153A503A48.png)  

3. Enter the following code snippet in your class to define a custom keyword:

   ```groovy
   @Keyword (keywordObject = "<category_name>")
   def keywordName(parameters…) {
   // enter your code here
   // you can use either Groovy or Java
   }
   ```

   where:
   
   | Item | Description | Required |
   | --- | --- | --- |
   | @Keyword | The annotation to indicate that the block of code below is the definition of a keyword. | Mandatory |
   |keywordObject| The category of your custom keyword (available from version 7.5.5)| Optional |
   | keywordName | The name that you would like to use for your custom keyword | Mandatory |
   | parameters | The list of parameters that would be used in the custom keyword | Mandatory |
   For example:

   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/introduction-to-custom-keywords/image2017-2-6-163A203A3.png)

   From version **7.5.5**, Custom Keywords in Keyword Browser are put in alphabetical order, and you can categorize them. In particular, the category name should be declared via `keywordObject` with the same mechanism as the built-in keywords. The below sample describes a keyword with the “Browser“ category:

   ```java
   @Keyword(keywordObject = "Browser")
   def refreshBrowser() {
   }
   ```

4. Save the **Keyword** file when you're done.

## Use Custom Keywords

### In Manual view

Follow the steps below to use your defined custom keywords in the **Manual** view of a Test Case:

1. Open a test case in the Manual view and select **Custom Keyword** from the command toolbar.
   
   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/introduction-to-custom-keywords/image2017-6-30-203A323A47.png)  

2. A new test step is added. Select one of your custom keywords.

   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/introduction-to-custom-keywords/image2017-2-6-163A443A46.png)

### In Script view

Follow the steps below to use your defined custom keywords in the **Script** view of a test case:

1. The **Class** _CustomKeywords_ of Katalon Studio allows you to access all custom keywords. Enter the following syntax into the script editor:

   ```groovy
   CustomKeywords.
   ```

2. The **Content Assist** function will be invoked right after you type the **dot** character. **Content Assist** provides users with context-sensitive suggestions for code completion. Therefore, all the custom keywords defined in your test project will be displayed as below:

   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/introduction-to-custom-keywords/image2017-6-30-203A353A9.png)

3. Select the recently created keyword and provide all parameters as required.

See also:

The following API docs may prove useful when working with custom keywords:

| Class | Method | Description |
| --- | --- | --- |
| [DriverFactory](https://docs.katalon.com/javadoc/com/kms/katalon/core/webui/driver/DriverFactory.html)| [getWebDriver()](https://docs.katalon.com/javadoc/com/kms/katalon/core/webui/driver/DriverFactory.html#getWebDriver()) | Get the current active web driver. |
| [Test Object](https://docs.katalon.com/javadoc/com/kms/katalon/core/testobject/TestObject.html)|[addProperty(String name, ConditionType condition, String value)](https://docs.katalon.com/javadoc/com/kms/katalon/core/testobject/TestObject.html#addProperty(java.lang.String,%20com.kms.katalon.core.testobject.ConditionType,%20java.lang.String))| Add a new property to the test object |
|| [setProperties(List&lt;TestObjectProperty&gt; properties)](https://docs.katalon.com/javadoc/com/kms/katalon/core/testobject/TestObject.html#setProperties(List%3CTestObjectProperty%3E)) | Set the properties of the test object |
|| [getObjectId()](https://docs.katalon.com/javadoc/com/kms/katalon/core/testobject/TestObject.html#getObjectId()) | Get object ID. |
|| [findPropertyValue(String name, boolean caseSensitive)](https://docs.katalon.com/javadoc/com/kms/katalon/core/testobject/TestObject.html#findPropertyValue(java.lang.String,%20boolean)) | Find the value of a property using the property name |
| [Keyword Util](https://docs.katalon.com/javadoc/com/kms/katalon/core/util/KeywordUtil.html) |[logInfo(String message)](https://docs.katalon.com/javadoc/com/kms/katalon/core/util/KeywordUtil.html#logInfo(java.lang.String)) | Log message as info |
|| [markError(String message)](https://docs.katalon.com/javadoc/com/kms/katalon/core/util/KeywordUtil.html#markError(java.lang.String)) | Mark a keyword to be error |
|| [markErrorAndStop(String message)](https://docs.katalon.com/javadoc/com/kms/katalon/core/util/KeywordUtil.html#markErrorAndStop(java.lang.String)) | Mark a keyword to be error and stop execution |
|| [markFailed(String message)](https://docs.katalon.com/javadoc/com/kms/katalon/core/util/KeywordUtil.html#markFailed(java.lang.String)) | Mark a keyword to be failed and continue execution |
|| [markFailedAndStop(String message)](https://docs.katalon.com/javadoc/com/kms/katalon/core/util/KeywordUtil.html#markFailedAndStop(java.lang.String)) | Mark a keyword to be failed and stop execution |
|| [markPassed(String message)](https://docs.katalon.com/javadoc/com/kms/katalon/core/util/KeywordUtil.html#markPassed(java.lang.String)) | Mark a keyword to be passed |
|| [markWarning(String message)](https://docs.katalon.com/javadoc/com/kms/katalon/core/util/KeywordUtil.html#markWarning(java.lang.String)) | Mark a keyword to be warning |
