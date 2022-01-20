---
title: "Generating reliable object selector using Spy Web utility"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/generate_css_xpath_selector_spy_web_utility.html
redirect_from:
    - "katalon-studio/tutorials/generate_css_xpath_selector_spy_web_utility.html"
description: "Katalon Studio Spy Web Utility provides an intelligent object capturing capability and immediate feedback on CSS Selector & Xpath selector. Learn more!"
---
Katalon Studio Spy Web Utility provides an intelligent object capturing capability and immediate feedback on the uniqueness of selectors.

There are two widely used selectors: **CSS** and **XPath**. Locators are object attributes which are used to build up XPath or CSS selector. Locators help find and identify elements on the Web page under test. Katalon Studio builds the final XPath selector (Basic mode) by using any active object locators from users to locate Web Elements.

With CSS or XPath mode of Selection Method, users can further input and edit XPath or CSS object to identify objects on Web UI.

The following are some Web element locators:

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
To learn more about this utility, see [Spy Web Utility](http://docs.katalon.com/pages/viewpage.action?pageId=5117668).

## Working with XPath selector

The following guide shows how to leverage Katalon Studio Spy Web Utility to locate web element with XPath selector.

These Xpath axes methods are used to find complex or dynamic elements.

*   **Checking Multiple Attributes:**

As an example, you can identify the login button with multiple attributes

![Login-Button-Multiple-Attributes](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/generate_css_xpath_selector_spy_web_utility/Login-Button-Multiple-Attributes.png)

Xpath:

```groovy
//*[@id='btn-login'][@type='submit']

```

![Multiple-Attributes](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/generate_css_xpath_selector_spy_web_utility/Multiple-Attributes.png)

*   **Contains():**

Contains() is a method used in an XPath expression. It is used when the value of any attribute changes dynamically such as login information.

Example:

Contains method for heading CURA Healthcare Service

![CURA-Healthcare-Service](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/generate_css_xpath_selector_spy_web_utility/CURA-Healthcare-Service.png)

Xpath:

```groovy
 //h1[contains(.,'CURA Healthcare Service')]

```

![Xpath object selector](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/generate_css_xpath_selector_spy_web_utility/Contain-Method.png)

*   **Last():**

Last() is a method used in an XPath expression. It is used to get the very last node.

Example:

There are 3 Social Icon Links, and we want to get the 3rd and last item by using Last()

![Social-icons-by-using-Last](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/generate_css_xpath_selector_spy_web_utility/Social-icons-by-using-Last.png)

Xpath:

```groovy
//ul[@class='list-inline']/li[last()]

```

*   **Start-with():**

The Start-with method finds the element whose attribute value changes on refresh or any operation on the webpage. In this expression, the starting text of the attribute is used to find the element whose attribute changes dynamically. You can also find the element whose attribute value is static (not changing).

Example:

Starts-with() method for heading CURA Healthcare Service

![CURA-Healthcare-Service](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/generate_css_xpath_selector_spy_web_utility/CURA-Healthcare-Service.png)

Xpath:

```groovy
//h3[starts-with(.,'We Care About')]

```

*   **Xpath axes methods:** These Xpath axes methods are used to find complex or dynamic elements.

**a) Following**

Selects all elements in the document following the current node( )

Example:

By using Following we can identify the Password text box which is located after the Username name field.

Xpath:

```groovy
.//*[@id='txt-username']//following::input

```

**b) Ancestor**

This will select all ancestors (parent, grandparent, etc.) of the current node.

Example:

In the below screenshot we want to get the ancestors of the 'ul ' tag highlighted in red. These ancestors are highlighted in blue.

Xpath:

```groovy
//ul[@class='list-inline']/ancestor::div

```

**c) Child**

Selects all children of the current node.

Example:

Using Child we can identify all social links as shown in the below screenshot.

![identify-all-social-links-by-child](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/generate_css_xpath_selector_spy_web_utility/identify-all-social-links-by-child.png)

Xpath:

```groovy
//ul[@class='list-inline']/child::li

```

**d) Preceding**

Selects all nodes that come before the current node.

Example:

Using Preceding we can identify all nodes that come before the Login button.

![identify-all-nodes-before-the-Login-button](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/generate_css_xpath_selector_spy_web_utility/identify-all-nodes-before-the-Login-button.png)

Xpath:

```groovy
//*[@id='btn-login']//preceding::input

```

**e) Following-sibling:**

Selects the following siblings of the context node. Siblings are at the same level of the current node as shown in the screen below. It will find the element after the current node.

Example:

By following-sibling method, we can Identify Password text box which located after Username name field.

Xpath:

```groovy
.//*[@id='txt-username']//following::input

```

The source code is available to be downloaded [here](https://github.com/katalon-studio/katalon-web-automation).

For further instructions and help, please refer to [Katalon Studio Tutorials](/katalon-studio/tutorials/) and [Katalon Forum](https://forum.katalon.com/).