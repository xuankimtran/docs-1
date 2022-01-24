---
title: "Generating reliable object selector using Spy Web utility"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/generate_css_xpath_selector_spy_web_utility.html
redirect_from:
    - "katalon-studio/tutorials/generate_css_xpath_selector_spy_web_utility.html"
description: "Katalon Studio Spy Web Utility provides an intelligent object capturing capability and immediate feedback on CSS Selector & Xpath selector. Learn more!"
---

This article shows you some examples on how you can generate reliable object selectors using Spy Web Utility.

Spy Web Utility provides an intelligent object capturing capability and immediate feedback on the uniqueness of selectors. To learn more about this utility, see [Spy Web Utility](http://docs.katalon.com/pages/viewpage.action?pageId=5117668).

There are two widely used selectors: **CSS** and **XPath**. Locators are object attributes which are used to build up XPath or CSS selector. Locators help find and identify elements on the web page under test. Katalon Studio builds the final XPath selector (Basic mode) by using any active object locators from users to locate web elements.

With CSS or XPath mode of Selection Method, you can further input and edit XPath or CSS object to identify objects on web UI.

The following are some web element locators:

1.  **Id**: Select element with the specified @id attribute.
2.  **Name**: Select first element with the specified @name attribute.
3.  **Link text**: Select link (anchor tag) element which contains text matching the specified link text
4.  **Partial Link text**: Select link (anchor tag) element which contains text matching the specified partial link text
5.  **Tag name**: Locate Element using a Tag name
6.  **Class name**: Locate Element using a class name.
7.  **CSS**: Select the element using CSS selectors.
8.  **Xpath**: Locate an element using a XPath expression.

## How to find object locators?

You can capture objects, get web element XPath or CSS locator, and manually input object selectors with XPath or CSS selection method mode using Spy Web Utility. Spy Web Utility provides instant feedback by auto-detecting the numbers of matching element with provided selector and highlighting it.

In this section, we will give you an example on how to find object locators using Spy Web Utility. We use our demo page in this example: [http://demoaut.katalon.com/](http://demoaut.katalon.com/).

**Step 1:** Click on **Spy Web** on the Katalon Studio main toolbar.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/generate_css_xpath_selector_spy_web_utility/spy-icon.png" alt="spy web utility" width=40%>

**Step 2:** The Object Spy window is shown as the following.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/generate_css_xpath_selector_spy_web_utility/object-spy-dialog.png" alt="object spy dialog" width=70%>

**Step 3:** Type the application URL in the URL text box and select the desired browser.  Click on **Start**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/generate_css_xpath_selector_spy_web_utility/choose-browser.png" alt="choose browser" width=70%>

Once you click on Start, Katalon Studio will launch the browser and navigates to the respective website.

**Step 4:** To capture test objects, hover the mouse over them. The focused web object would be highlighted.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/generate_css_xpath_selector_spy_web_utility/capture-object.png" alt="capture object" width=100%>

By pressing the <Alt + ~> keys the focused object will be highlighted green, which means that it has been stored in the Captured Objects list.

Katalon Studio will automatically capture all available properties of captured objects. You can change the folder name and edit the value of any properties.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/generate_css_xpath_selector_spy_web_utility/selected-locator.png" alt="selected locator" width="70%">

Katalon Studio allows users to select **Selection Method** to locate captured objects. **Basic mode** is recommended to manual testers who just started automation journey. With **Basic** mode, Katalon Studio's intelligent selector generator will **automatically generate** a robust and unique XPath **selector** which combined all properties of captured objects.

For advanced testers who wish to **manually input selectors** have the option to select between **CSS** or **XPath mode**.

Click on **Add** to **Object Repository** from the command toolbar to save objects in Objects Repository. Select a folder to add the captured objects into. Click **OK** when done.

## Working with XPath selector

The following guide shows how to leverage Katalon Studio Spy Web Utility to locate web element with XPath selector.

These Xpath axes methods are used to find complex or dynamic elements.

In the examples below, we are using our demo page: [http://demoaut.katalon.com/](http://demoaut.katalon.com/).

You can find our web sample project available to be downloaded here: [Katalon Web Automation Sample Project](https://github.com/katalon-studio/katalon-web-automation).

*   **Checking Multiple Attributes:**

As an example, you can identify the login button with multiple attributes

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/generate_css_xpath_selector_spy_web_utility/login.png" alt="multiple attributes" width="100%">

Xpath:

```groovy
//*[@id='btn-login'][@type='submit']

```

*   **Contains():**

Contains() is a method used in an XPath expression. It is used when the value of any attribute changes dynamically such as login information.

Example:

Contains method for heading CURA Healthcare Service

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/generate_css_xpath_selector_spy_web_utility/contain.png" alt="contain" width="100%">

Xpath:

```groovy
 //h1[contains(.,'CURA Healthcare Service')]

```

*   **Last():**

Last() is a method used in an XPath expression. It is used to get the very last node.

Example:

There are 3 Social Icon Links, and we want to get the 3rd and last item by using Last()

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/generate_css_xpath_selector_spy_web_utility/last.png" alt="last" width="100%">

Xpath:

```groovy
//ul[@class='list-inline']/li[last()]

```

*   **Start-with():**

The Start-with method finds the element whose attribute value changes on refresh or any operation on the webpage. In this expression, the starting text of the attribute is used to find the element whose attribute changes dynamically. You can also find the element whose attribute value is static (not changing).

Example:

Starts-with() method for heading CURA Healthcare Service

Xpath:

```groovy
//h3[starts-with(.,'We Care About')]

```

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/generate_css_xpath_selector_spy_web_utility/start-with.png" alt="start with" width="100%>

*   **Xpath axes methods:** These Xpath axes methods are used to find complex or dynamic elements.

**a) Following**

Selects all elements in the document following the current node( )

Example:

By using Following we can identify the Password text box which is located after the Username name field.

Xpath:

```groovy
.//*[@id='txt-username']//following::input

```

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/generate_css_xpath_selector_spy_web_utility/following.png" alt="following" width="100%">

**b) Ancestor**

This will select all ancestors (parent, grandparent, etc.) of the current node.

Example:

In the below screenshot we want to get the ancestors of the 'ul ' tag highlighted in red. These ancestors are highlighted in blue.

Xpath:

```groovy
//ul[@class='list-inline']/ancestor::div

```

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/generate_css_xpath_selector_spy_web_utility/ancestor.png" alt="ancestor" width=100%>

**c) Child**

Selects all children of the current node.

Example:

Using Child we can identify all social links as shown in the below screenshot.

Xpath:

```groovy
//ul[@class='list-inline']/child::li

```

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/generate_css_xpath_selector_spy_web_utility/child.png" alt="chill" width=100%>

**d) Preceding**

Selects all nodes that come before the current node.

Example:

Using Preceding we can identify all nodes that come before the Login button.

Xpath:

```groovy
//*[@id='btn-login']//preceding::input

```

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/generate_css_xpath_selector_spy_web_utility/preceding.png" alt="preceding" width=100%>

**e) Following-sibling:**

Selects the following siblings of the context node. Siblings are at the same level of the current node as shown in the screen below. It will find the element after the current node.

Example:

By following-sibling method, we can Identify Password text box which located after Username name field.

Xpath:

```groovy
.//*[@id='txt-username']//following::input

```
<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/generate_css_xpath_selector_spy_web_utility/following-sibling.png" alt="following-sibling" width="100%">