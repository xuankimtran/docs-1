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

We use the demo site [Books](https://books-pwakit.appspot.com/explore?q=). All the elements in this demo website are under a shadow root. In this demonstration, we identify shadow DOM objects to perform test action Set Text: "hello World" into the website's search bar.

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

    <img src=”url” width=”%” alt="Create parent object">

5. Next, create the child object:
   
    - Go to **File > New > Test Object**. Name it as **input**.
    - In the **Object's Properties** section, define the inspected property from step 3.
    - After defining the property, in the **Settings** section, choose **Shadow DOM parent** option, then click **Browse**. An **Object Repository Browser** dialog opens.
    - In the open dialog, choose the `book_app` object from step 4. Click **OK**.

    <img src=”url” width=”%” alt="Create child object">

6. Next, create a new test **object** to represent an object in HTML DOM. Let's name this object as **aStoreLink**.

7. Create a property for this object, **aStoreLink**. This property has the _name as_ **href** and _value_ as [http://www.amazon.com/gp/product/1849693129/ref=as\_li\_qf\_sp\_asin\_il\_tl?ie=UTF8&camp=1789&creative=9325&creativeASIN=1849693129&linkCode=as2&tag=kaidez-20&linkId=CK7X5SMYEHL3BMEQ](http://www.amazon.com/gp/product/1849693129/ref=as_li_qf_sp_asin_il_tl?ie=UTF8&camp=1789&creative=9325&creativeASIN=1849693129&linkCode=as2&tag=kaidez-20&linkId=CK7X5SMYEHL3BMEQ)

![Katalon-DOM-astorelink](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/shadow_dom_elements_testing/Katalon-DOM-astorelink.png)

6. Select the Shadow Root Parent option, as shown below. Click on Browse and select **SectionAllBooks** from Object Repository Browser.

![Katalon-DOM-root-parent](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/shadow_dom_elements_testing/Katalon-DOM-root-parent.png)

Once finished, the aStoreLink object has Shadow Root Parent as below

![Katalon-shadow-root-parent-2](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/shadow_dom_elements_testing/Katalon-shadow-root-parent-2.png)

7. Now you're ready to start scripting. Let's create a test case with the name **Shadow DOM Test** and open it.

![Katalon-Shadow-DOM-test1](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/shadow_dom_elements_testing/Katalon-Shadow-DOM-test1-300x169.png)

8. Paste the following script into the test case's Script editor.

```groovy
import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject

import com.kms.katalon.core.webui.keyword.WebUiBuiltInKeywords as WebUI

'Open browser and navigate to the AUT website'
WebUI.openBrowser('http://www.kaidez.com/samples/template-shadowdom-practice/')

'Click on the destination book store link'
WebUI.click(findTestObject('aStoreLink'))

'Delay 5s to view the result'
WebUI.delay(5)

'Verify that a new window is opened'
WebUI.switchToWindowTitle('Object-Oriented JavaScript, 2nd Edition: Stoyan Stefanov, Kumar Chetan Sharma: 9781849693127: Amazon.com: Books')

'Close the browser to clean up'
WebUI.closeBrowser()

```

![Katalon DOM script editor](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/shadow_dom_elements_testing/Katalon-DOM-script-editor.png)

9. Now execute the test script by selecting Run > Chrome.

![Katalon-DOM-Execute-on-chrome](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/shadow_dom_elements_testing/Katalon-DOM-Execute-on-chrome.png)

10. Katalon Studio should successfully find the element within the shadow root and open the Amazon window to show the book.

![Katalon-DOM-Amazon-window](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/shadow_dom_elements_testing/Katalon-DOM-Amazon-window-1024x715.png)

Congratulations! You have successfully created and run your first Shadow DOM test script with Katalon Studio. For more advanced features and keywords, please visit Katalon Studio tutorials center

The sample project for this tutorial can be found at [https://github.com/katalon-studio/ShadowDOMSampleProject](https://github.com/katalon-studio/ShadowDOMSampleProject).