---
title: "Automation testing of Shadow DOM elements with Katalon Studio"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/shadow_dom_elements_testing.html
redirect_from:
    - "katalon-studio/tutorials/shadow_dom_elements_testing.html"
description: "What is Shadow DOM? This article will show you how Katalon Studio solves Shadow DOM problem and let you test shadow DOM elements in a straightforward way"
---
<INTRODUCTION>

> Requirements
> - Chrome Browser version from 53 onwards. To see full browser version with shadow DOM support here: [Shadow DOM (V1)](https://caniuse.com/shadowdomv1)
> 

Shadow DOM is a useful solution for Web developers. It helps web developers to better encapsulate their code by allowing DOM elements to contain child node and CSS. Nevertheless, it becomes a challenge for automation testing because elements inside a shadow root technically don't exist in the main document DOM. Therefore, test automation frameworks that use the DOM query function don't work properly.

In this artical, we demonstrate how to test shadow DOM elements in Katalon Studio framework.

We use the demo site [Books](https://books-pwakit.appspot.com/explore?q=). All the elements in this demo website are under a shadow root. In this demonstration, we identify shadow DOM objects to perform test action Set Text: "shadow DOM" into the website's search bar.

Do as follows:

1. Create a new project. Go to **File > New > Project**. Name it as **Shadow DOM Testing**.

    <img src=”https://github.com/katalon-studio/docs-images/raw/339de0f5ad5bce4f4dc1d8d7ef8f0ea6b5d0780a/katalon-studio/tutorials/shadow_dom_elements_testing/Katalon-DOM-testing.png” width=”70%” alt="Create a project">

2. In the demo website, right-click at the search bar, click **Inspect** to inspect its elements. A Chrome Developer tool appears within the browser.

    <img src=”url” width=”%” alt="Inspect web object element">

   Here you can see the search bar' s elements are in a shadow tree, under the shadow root. Even though the DOM query function can not locate elements within a shadow DOM, it can find the shadow host. In this demo website, book-app is a shadow host. 

    <img src=”url” width=”%” alt="Shadow root element">



1. Create a new test object to represent a shadow root. Go to **File > New > Test Object**. Name it as **sectionBookApp**.

    <img src=”url” width=”%” alt="Test object sectionBookApp">

2. In the new object, click **Add** in the command toolbar. A new **Add property** dialog opens. 

    Add a property with the name **id** and the value **allBooks** for the **sectionAllBooks** object.

    <img src=”url” width=”%” alt="Test object sectionBookApp">

    ![Katalon DOM allbooks](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/shadow_dom_elements_testing/Katalon-DOM-allbooks.png)

3. Next, create a new test **object** to represent an object in HTML DOM. Let's name this object as **aStoreLink**.

4. Create a property for this object, **aStoreLink**. This property has the _name as_ **href** and _value_ as [http://www.amazon.com/gp/product/1849693129/ref=as\_li\_qf\_sp\_asin\_il\_tl?ie=UTF8&camp=1789&creative=9325&creativeASIN=1849693129&linkCode=as2&tag=kaidez-20&linkId=CK7X5SMYEHL3BMEQ](http://www.amazon.com/gp/product/1849693129/ref=as_li_qf_sp_asin_il_tl?ie=UTF8&camp=1789&creative=9325&creativeASIN=1849693129&linkCode=as2&tag=kaidez-20&linkId=CK7X5SMYEHL3BMEQ)

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