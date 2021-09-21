---
title: "Automation testing of Shadow DOM elements with Katalon Studio"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/shadow_dom_elements_testing.html
redirect_from:
    - "katalon-studio/tutorials/shadow_dom_elements_testing.html"
description:
---

> Requirements
> - Chrome Browser version from 53 onwards. You can see browser versions with shadow DOM support here: [Shadow DOM (V1)](https://caniuse.com/shadowdomv1)
> 

Shadow DOM allows DOM elements to contain child nodes and CSS, which helps web developers by better encapsulating their code. But this creates challenges for automation testing, because elements inside a shadow root technically don't exist in the main DOM.

In this article, we demonstrate how to test shadow DOM elements in the Katalon Studio framework.

We use the demo site [Books](https://books-pwakit.appspot.com/explore?q=). All the elements in this demo website are under a shadow root. In this demonstration, we identify shadow DOM objects, then verify them by successfully inputting: "hello World" into the website's search bar.

Do as follows:

1. Create a new project. Go to **File > New > Project**. Here, we name the project **Shadow DOM Testing**.

    <img src="https://github.com/katalon-studio/docs-images/raw/339de0f5ad5bce4f4dc1d8d7ef8f0ea6b5d0780a/katalon-studio/tutorials/shadow_dom_elements_testing/Katalon-DOM-testing.png" width="70%" alt="Create a project">

2. In the demo website, navigate to the search bar, **right-click > Inspect**. The **Chrome Developer** tool opens and highlights its elements.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/shadow_dom_elements_testing/KS-DOM-Inspect-web-object%20element%20.png" width="70%" alt="Inspect web object element">

3. At this point, there are two Shadow DOM elements that you need to identify in the **Chrome Developer** tool:
    - The property of the parent object. The parent object is the shadow host. In this demo site, `book-app` is the parent object.

    <img src="https://github.com/katalon-studio/docs-images/raw/59a8792abbe002830ddd808284c7a51a43fb5acb/katalon-studio/tutorials/shadow_dom_elements_testing/KS-DOM-Property-of-shadow-host.png" width="70%" alt="Identify the property of shadow host">

    - The property of the child object. The child object is the inspecting shadow DOM elements. In this example, we look at the property of the search bar's elements.
   
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/shadow_dom_elements_testing/KS-DOM-Property-of-shadow-DOM-elements.png" width="70%" alt="Identify the property of child object">

You can learn more about object properties from the Mozilla developer documentation here: [Working with objects](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Working_with_Objects).

4. After identifying the property of the parent object and the child object, return to the Katalon Studio framework to define object properties. 
    
    Katalon Studio supports the following selection methods to create the object's properties: Attributes, XPath, CSS, Image. You can learn more about using the best selection method for object properties here: [Selection Method](https://docs.katalon.com/katalon-studio/docs/web-selection-methods.html#change-the-css-selector-of-an-object-at-runtime). 
    
    In this example, we use the **Attributes** method.

    - Create the parent object: 

      - Go to **File > New > Test Object**. Name it as **book_app**.
      - In the **Object's Properties** section, click **Add**. An **Add Property** dialog opens. 
      - Fill in the **Add Property** dialog as shown below: 
        <table width="592">
        <tbody>
        <tr>
        <td><strong>Name</strong></td>
        <td><strong>Conditions</strong></td>
        <td><strong>Value</strong></td>
        </tr>
        <tr>
        <td>apptitle</td>
        <td>equals</td>
        <td>BOOKS</td>
        </tr>
        </tbody>
        </table>
      - Click **OK**. The `apptitle` property appears in the **Object's Properties** section.
      - Check the **Detect object by** box in the `apptitle` property line to generate a **Selected Locator** for the object.  

        <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/shadow_dom_elements_testing/KS-DOM-Results-after-creating-the-parent-objects.png" width="70%" alt="Results after creating the parent object">
    
    - Create the child object:
   
      - Go to **File > New > Test Object**. Name it as **input**.
      - In the **Object's Properties** section, click **Add**. An **Add Property** dialog opens. 
      - Fill in the **Add Property** dialog as shown below: 
        <table width="592">
        <tbody>
        <tr>
        <td><strong>Name</strong></td>
        <td><strong>Conditions</strong></td>
        <td><strong>Value</strong></td>
        </tr>
        <tr>
        <td>id</td>
        <td>equals</td>
        <td>input</td>
        </tr>
        </tbody>
        </table>

      - Check the **Detect object by** box in the `input` property line to generate a **Selected Locator** for the object.

        <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/shadow_dom_elements_testing/KS-DOM-after-creating-the-property-of-child-object.png" width="70%" alt="Results after creating the property child object">

      - After defining the property, in the **Settings** section, choose the **Shadow DOM parent** option, then click **Browse**. An **Object Repository Browser** dialog opens.
      - In the open dialog, choose the `book_app` object as the parent object. Click **OK**.
      - Once finished, the `input` object identifies `book_app` as its **Shadow Root Parent** as below.

        <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/shadow_dom_elements_testing/KS-DOM-after-defining-parent-object-for-the-child-object.png" width="70%" alt="Results after pointing the child object to the parent object">

5. Next, create a new test case. Go to **File > New > Test Case**. We name ours **Shadow DOM Test**.
   
6. In the new test case, switch to the Script tab, copy and paste the following script into the test script.

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
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/shadow_dom_elements_testing/KS-DOM-final-test-script.png" width="70%" alt="Write the Test Script">

You can also write the test case in the Manual tab. Learn more about the manual mode here: [How to create the test in Manual mode](https://docs.katalon.com/katalon-studio/videos/create_test_manual_mode.html)

8. Run the test script. In the main toolbar. Click **Run > Chrome**.

    Katalon Studio should successfully find the element within the shadow root and input the text: "hello World" into the search bar.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/shadow_dom_elements_testing/KS-DOM-final-results-after-running-the-test.png" width="70%" alt="Run the Test Script">
