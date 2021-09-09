---
title: "Automation testing of Shadow DOM elements with Katalon Studio"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/shadow_dom_elements_testing.html
redirect_from:
    - "katalon-studio/tutorials/shadow_dom_elements_testing.html"
description: "This article will show you how Katalon Studio solves Shadow DOM problem and let you test shadow DOM elements in a straightforward way"
---
<INTRODUCTION>

> Requirements
> - Chrome Browser version from 53 onwards. To see full browser version with shadow DOM support here: [Shadow DOM (V1)](https://caniuse.com/shadowdomv1)
> 

Shadow DOM is a useful solution for Web developers. It helps web developers to better encapsulate their code by allowing DOM elements to contain child node and CSS. Nevertheless, it becomes a challenge for automation testing because elements inside a shadow root technically don't exist in the main document DOM. Therefore, test automation frameworks that use the DOM query function don't work properly.

In this artical, we demonstrate how to test shadow DOM elements in Katalon Studio framework.

We use the demo site [Books](https://books-pwakit.appspot.com/explore?q=). All the elements in this demo website are under a shadow root. In this demonstration, we identify shadow DOM objects to test inputting: "hello World" into the website's search bar.

Do as follows:

1. Create a new project. Go to **File > New > Project**. Name it as **Shadow DOM Testing**.

    <img src=”https://github.com/katalon-studio/docs-images/raw/339de0f5ad5bce4f4dc1d8d7ef8f0ea6b5d0780a/katalon-studio/tutorials/shadow_dom_elements_testing/Katalon-DOM-testing.png” width=”70%” alt="Create a project">

2. In the demo website, to inspect the search bar's elements, right-click at it, then click **Inspect**. A Chrome Developer tool opens and highlights its elements.

    <img src=”url” width=”%” alt="Inspect web object element">

3. At this point, there are two Shadow DOM elements that you need to identify in the Chrome Developer tool:
    - The property of the parent object. The parent object is the shadow host. In this demo site, `book-app` is the parent object.
    - The property of the child object. The child object is the inspecting shadow DOM elements. In this example, we look at the property of the search bar's elements.
   
    <img src=”url” width=”%” alt="Property of shadow DOM elements">

4. Switch back to the Katalon Studio framework, create the parent object: 
   
    - Go to **File > New > Test Object**. Name it as **book_app**.
    - In the **Object's Properties** section, define the inspected property from step 3.

    <img src=”url” width=”%” alt="Create the parent object">

5. Next, create the child object:
   
    - Go to **File > New > Test Object**. Name it as **input**.
    - In the **Object's Properties** section, define the inspected property from step 3.
    - 
    <img src=”url” width=”%” alt="Define child object's property">

    - After defining the property, in the **Settings** section, choose **Shadow DOM parent** option, then click **Browse**. An **Object Repository Browser** dialog opens.
    - In the open dialog, choose the `book_app` object from step 4. Click **OK**.
    - Once finished, the `input` object has Shadow Root Parent as below

    <img src=”url” width=”%” alt="Results after creating the child object">

6. Next, create a new test case. Go to **File > New > Test Case**. Name it **Shadow DOM Test** and open it.
   
    <img src=”url” width=”%” alt="Create">

7. In the new test case, switch to the Script tab, copy and paste the following script into the test script.

    ```groovy
    import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject

    import com.kms.katalon.core.webui.keyword.WebUiBuiltInKeywords as WebUI

    //Open browser and navigate to the AUT website
    WebUI.openBrowser('https://books-pwakit.appspot.com/explore?q=')

    //Input text into the search bar
    WebUI.setText(findTestObject('Object Repository/input'), 'hello World')

    //Delay 5s to view the result
    WebUI.delay(5)

    //Close the browser to clean up
    WebUI.closeBrowser()

    ```
    <img src=”url” width=”%” alt="Write the Test Script">

You can also write the test case in the Manual tab. Learn more at: [How to create the test in Manual mode](https://docs.katalon.com/katalon-studio/videos/create_test_manual_mode.html)

8. Run the test script. In the main toolbar. Click **Run > Chrome**.
   
   <img src=”url” width=”%” alt="Run the Test Script">

Katalon Studio should successfully find the element within the shadow root and input text: "hello World" into the search bar.
