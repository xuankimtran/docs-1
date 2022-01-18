---
title: "Detecting objects with XPath"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/detect_elements_xpath.html
redirect_from:
    - "/katalon-studio/tutorials/detect_elements_xpath.html"
---

UI elements of the application under test (AUT) are the main objects in test cases and test scripts. Therefore, detecting UI elements is crucial for automated testing. However, identifying them manually requires much time and experience in HTML.

This task becomes even more challenging for objects that could not be identified by their common attributes, elements dynamically changing, or elements are located deep within another element (nested elements). 

This article shows you how to use XPath in Katalon Studio to deal with nested elements and dynamic elements.

## What is XPath?

XPath stands for XML Path Language. In an XML document, XPath uses path expressions to navigate through elements, attributes, and select nodes or node-sets.

On a webpage using HTML DOM (Document Object Model) structure, you can also use XPath to find the location of any element. To learn more about HTML DOM, you can refer to W3schools documentation: [What is the HTML DOM?](https://www.w3schools.com/whatis/whatis_htmldom.asp).

There are two types of XPath: absolute XPath and relative XPath (smart XPath).

### Absolute XPath

XML documents are treated as trees of nodes, in which the topmost element of the tree is the root element.

Absolute XPath is the path starting from the root.

For example: `/html/body/div[1]/div[1]/div/div[3]/div[2]/div`

In Katalon Studio, the XPath captured strategy for absolute XPath is `xpath:position`. Using absolute XPath is a simple way to solve the problem when you are dealing with dynamic elements. However, if something changes in the structure of your web page, your code will break and this XPath fails. Therefore, using absolute XPath is not a recommended method for detecting dynamic elements.

### Relative XPath

You might want to use the relative XPath method when you observe a pattern in the attribute values like ID or Class of the web element. Relative XPath (smart XPath) is the path that starts from the middle of the HTML DOM structure. Unlike the absolute XPath that starts from the root, relative XPath starts with the double forward slash (//), which means it can search the element anywhere on the webpage. Therefore, you can start from the middle of the HTML DOM structure without writing a long XPath. For example: `//a[contains(text(), 'Katalon Studio')]`.

You can find a list of XPath captured strategies in Katalon Studio using relative XPath at this documentation: [Configure XPath](https://docs.katalon.com/katalon-studio/docs/web-selection-methods.html#configure-xpath).

## How to identify nested elements?

### What is a nested element?

Elements can contain other elements. Nested elements are children of their parent container. 

For example, the download link in the script below is an element nested in another.

```groovy
<div class="container">
<div class="navbar-collapse navbar-right" aria-expanded="true">
<div class = "nav-bar-decorated"
<ul class="nav navbar-nav">
<Li>
<a class="pbtn-download" href="#katalon-download">Download</a> <!-- Deeply nested element  -->
</li>
</div>
</div>
</div>

```

It is difficult to identify a nested element, such as the `<a>` element in the script above. To define the XPath manually, we need to have solid knowledge about the DOM structure of the webpage.

### How to identify nested elements?

Identifying XPath is an effective way to find nested elements which cannot be identified by common properties such as **ID**, **Name**, or **Class**. Katalon Studio can generate and optimize XPath for HTML elements, regardless of how deeply nested they are. You can use these XPaths to identify elements without having to search through the DOM tree.

The example below illustrates how Katalon Studio generates and optimizes XPath automatically when you spy on the **Make Appointment** object (a nested element).

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/detect_elements_xpath/xpath-capture.png" alt="detecting elements with Xpath by Katalon Studio" width="100%">

## Deal with dynamically changing elements

### What is a dynamic element?

One of the challenging and time-consuming tasks in test automation is to modify test scripts when the AUT is changed, especially in the early stages of software development. Developers may change identifiers and elements quite often from one build to another. In addition, during the execution, the AUT elements may change dynamically.

Dynamic web elements are elements that IDs and any other attributes like class names or values keep changing when you refresh the page. Dynamic elements are database-driven or session-driven. For example, when you edit an element in a database, it changes a number of areas of the application under test. Dynamic elements are strictly content, with formatting being laid out in the design. Dynamic identifiers are generally used for text-boxes and buttons.

### Deal with dynamically changing elements

To deal with dynamic elements, you might not want to set fixed XPaths for these elements in test cases. Instead, script XPaths dynamically based on certain patterns. Katalon Studio supports all XPath Axes, such as:

* following-sibling
* preceding-sibling
* contains
* descendant
* starts-with

Here are a few examples:

| Xpath value | Description |
| --- | --- |
| .//h2\[text()='Make Appointment'\] | Locate the **h2** tag element that has text matching exactly "Make Appointment" |
| //*\[contains(text(),'Login')\] | Locate any element that contains the text "Login" |
| //a\[starts-with(@id='LoginPanel')\] | Locate the **a** tag element that has the ID starting with "LoginPanel" |

For more information on XPath Axes, refer to W3school documentation: [XPath Axes](https://www.w3schools.com/xml/xpath_axes.asp).

**Next step**:

Learn how to input and edit XPath or CSS objects to identify objects on Web UI via Spy Web Utility: [Generating reliable object selector using Spy Web utility](https://docs.katalon.com/katalon-studio/docs/generate_css_xpath_selector_spy_web_utility.html).
