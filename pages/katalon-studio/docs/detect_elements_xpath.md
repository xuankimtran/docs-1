---
title: "Detecting dynamic objects with XPath"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/detect_elements_xpath.html
redirect_from:
    - "/katalon-studio/tutorials/detect_elements_xpath.html"
---

With any application under test (AUT), the detection of UI elements is crucial to automated testing. However, identifying them manually requires much time and experience in HTML.

This task becomes even more challenging for elements that could not be identified by their common attributes, elements that change dynamically, or elements that are located deep within another element (nested elements). 

This article shows you how to use XPath in Katalon Studio to deal with nested elements and dynamic elements.

## What is XPath?

XPath stands for XML Path Language. In an XML document, XPath uses path expressions to navigate through elements, attributes, and select nodes or node-sets.

On a webpage using the HTML DOM (Document Object Model) structure, you can also use XPath to find the location of any element. To learn more about HTML DOM, you can refer to the W3schools documentation: [What is the HTML DOM?](https://www.w3schools.com/whatis/whatis_htmldom.asp)

There are two types of XPath: absolute XPath and relative XPath (smart XPath).

### Absolute XPath

XML documents are treated as trees of nodes, in which the topmost element of the tree is the root element.

Absolute XPath is the path starting from the root. An absolute XPath starts with HTML and forward-slash (/).

For example: `/html/body/div[1]/div[1]/div/div[3]/div[2]/div`

In Katalon Studio, the XPath capture strategy for absolute XPath is `xpath:position`. Using absolute XPath is a simple way to solve the problem when dealing with dynamic elements. However, if something changes in the structure of your web page, this XPath might fail. Therefore, absolute XPath is not recommended for detecting dynamic elements.

### Relative XPath

You might want to use the relative XPath method to observe a pattern in the attribute values like ID or Class of the web element. Relative XPath (smart XPath) is the path that starts from the middle of the HTML DOM structure. Unlike the absolute XPath that starts from the root, relative XPath starts with the double forward-slash (//), which means it can search for the element anywhere on the webpage. Therefore, you can start from the middle of the HTML DOM structure without writing a long XPath. For example: `//a[contains(text(), 'Katalon Studio')]`.

You can find a list of XPath capture strategies in Katalon Studio using relative XPath in this document: [Configure XPath](https://docs.katalon.com/katalon-studio/docs/web-selection-methods.html#configure-xpath).

## How to identify nested elements?

### What is a nested element?

Elements can contain other elements. Nested elements are children of their parent container. 

For example, the download link in the script below is an element nested in another.

```groovy
<div class="container">
	<div class="navbar-collapse navbar-right">
		<div class="nav-bar-decorated">
			<ul>
				<li><a class="pbtn-download" href="#katalon-download">Download</a> <!-- Deeply nested element  --></li>
			</ul>
		</div>
	</div>
</div>
```

It is difficult to identify a nested element, such as the `<a>` element in the script above. To define the XPath manually, we need to have solid knowledge about the DOM structure of the webpage.

### Identify nested elements using XPath

Identifying XPath is an effective way to find nested elements that cannot be identified by common properties such as ID, name, or class. Katalon Studio can generate and optimize XPath for HTML elements, regardless of how deeply nested they are. You can use these XPaths to identify elements without searching through the DOM tree.

The example below illustrates how Katalon Studio generates and optimizes XPath automatically when you spy on the **Make Appointment** object (a nested element).

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/detect_elements_xpath/xpath-capture.png" alt="detecting elements with Xpath by Katalon Studio" width="100%">

## Deal with dynamically changing elements

### What is a dynamic element?

One of the challenging and time-consuming tasks in test automation is to modify test scripts when the AUT is changed, especially in the early stages of software development. Developers may change identifiers and elements quite often from one build to another. In addition, during the execution, the AUT elements may change dynamically.

Dynamic web elements are elements whose IDs and any other attributes like class names or values keep changing when you refresh the page. Dynamic elements are database-driven or session-driven. For example, when you edit an element in a database, it changes a number of areas of the application under test.

### Deal with dynamic elements using XPath

To deal with dynamic elements, you might not want to use absolute XPaths for these elements in test cases. Instead, you might want to use relative XPaths based on specific patterns. 

XPath axes are used to search for the multiple nodes in the XML document from the current node context. Katalon Studio supports all XPath axes. The table below shows some common methods you can use to detect dynamic elements:

<table>
    <thead>
        <tr>
            <th>Method</td>
            <th>Description</th>
            <th>Example</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Checking Multiple Attributes</td>
            <td>Add more than one condition to search element using XPath.</td>
            <td><code>//*[@id='btn-login'][@type='submit']</code></td>
        </tr>
        <tr>
            <td>Index</td>
            <td>Specify a given tag name in terms of the index value you wish to locate. Use this when more than one element is present in the DOM with similar attributes, and it becomes difficult to search for them.</td>
            <td><code>//div[@class='form-group']//select[1]</code>
        </tr>
        <tr>
            <td>Chained XPath</td>
            <td>Use multiple XPath expressions and chain them.</td>
            <td><code>//section[@id='appointment']//span[@class='glyphicon glyphicon-calendar']</code></td>
        </tr>
        <tr>
            <td>Contains()</td>
            <td>Use the Contains() method to detect dynamic elements that contain static values.</td>
            <td><code>//button[contains(@id, 'btn-login')]</code><</td>
        </tr>
        <tr>
            <td>Last()</td>
            <td>Last() is a method used in an XPath expression. It is used to get the very last node.</td>
            <td><code>//ul[@class='list-inline']/li[last()]</code></td>
        </tr>
        <tr>
            <td>Start-with()</td>
            <td>The Start-with method finds the element using the starting text of an attribute. This method is useful when the first part of the attribute value is fixed (static), and the rest is dynamic.</td>
            <td><code>//h3[starts-with(text(),'We Care About')]</code></td>
        </tr>
        <tr>
            <td>Preceding</td>
            <td>Select all nodes that come before the current node.</td>
            <td><code>//*[@id='btn-login']//preceding::input</code></td>
        </tr>
        <tr>
            <td>Following</td>
            <td>Select all elements in the document following the current node( ).</td>
            <td><code>.//*[@id='txt-username']//following::input</code></td>
        </tr>
        <tr>
            <td>Following-sibling</td>
            <td>Select the following siblings of the context node.</td>
            <td><code>.//*[@id='txt-username']//following::input</code></td>
        </tr>
        <tr>
            <td>Ancestor</td>
            <td>Select all ancestors (parent, grandparent, etc.) of the current node.</td>
            <td><code>//ul[@class='list-inline']/ancestor::div</code></td>
        </tr>
        <tr>
            <td>Child</td>
            <td>Select all children of the current node.</td>
            <td><code>//ul[@class='list-inline']/child::li</code></td>
        </tr>
        <tr>
            <td>Descendant</td>
            <td>Select all descendant (child node, grandchild node, etc.) of the current node.</td>
            <td><code>//ul[@class='list-inline']/descendant::li</code></td>
        </tr>
    </tbody>
</table>

For more information on XPath axes, refer to the W3school documentation: [XPath Axes](https://www.w3schools.com/xml/xpath_axes.asp).

> To learn how to find object locators in Katalon Studio, see [Spy Web Utility](http://docs.katalon.com/pages/viewpage.action?pageId=5117668).

**Next step**:

Learn how to input and edit XPath or CSS objects to identify objects on Web UI via Spy Web Utility: [Generating reliable object selector using Spy Web utility](https://docs.katalon.com/katalon-studio/docs/generate_css_xpath_selector_spy_web_utility.html).
