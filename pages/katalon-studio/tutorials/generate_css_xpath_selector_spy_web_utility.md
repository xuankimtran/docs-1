---
title: "Generating reliable object selector using Spy Web utility"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/generate_css_xpath_selector_spy_web_utility.html
redirect_from:
    - "katalon-studio/tutorials/generate_css_xpath_selector_spy_web_utility.html"
description: "Katalon Studio Spy Web Utility provides an intelligent object capturing capability and immediate feedback on CSS Selector & Xpath selector. Learn more!"
---

This article shows you some examples of generating reliable object selectors using Spy Web Utility.

Spy Web Utility provides an intelligent object capturing capability on websites. To learn more about this utility, see [Spy Web Utility](https://docs.katalon.com/katalon-studio/docs/spy-web-utility.html).

There are two widely used selectors: **CSS** and **XPath**. Locators are object attributes that are used to build up XPath or CSS selectors. Locators help find and identify elements on the web page under test. 

Based on the selected method, you can edit the **Selected Locator** to adjust the current selector of an object or manually add a selector using either an XPath or a CSS selector.

With the CSS or XPath mode of the **Selection Method**, you can further input and edit XPath or CSS objects to identify objects on web UI.

Below are some web element locators:

<table>
    <thead>
        <tr>
            <th>Web element locators</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Id</td>
            <td>Select elements with the specified @id attribute.</td>
        </tr>
        <tr>
            <td>Name</td>
            <td>Select the first element with the specified @name attribute.</td>
        </tr>
        <tr>
            <td>Link text</td>
            <td>Select links (anchor tag) element which contains text matching the specified link text.</td>
        </tr>
        <tr>
            <td>Partial link text</td>
            <td>Select links (anchor tag) element which contains text matching the specified partial link text.
        </tr>
        <tr>
            <td>Tag name</td>
            <td>Locate elements using a tag name.</td>
        </tr>
        <tr>
            <td>Class name</td>
            <td>Locate elements using a class name.</td>
        </tr>
        <tr>
            <td>CSS</td>
            <td>Select elements using CSS selectors.</td>
        </tr>
        <tr>
            <td>XPath</td>
            <td>Locate elements using an XPath expression.</td>
        </tr>
    </tbody>
</table>

## How to find object locators?

You can capture objects, get web element XPath or CSS locators, and manually input XPath or CSS object selectors using Spy Web Utility. Spy Web Utility provides instant feedback by auto-detecting and highlighting all elements that match with the provided selector.

In this section, we will illustrate how to use the Spy Web Utility to find object locators.

1. Open or create a new project. From the main toolbar, click on the **Spy Web** icon.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/generate_css_xpath_selector_spy_web_utility/spy-icon.png" alt="spy web utility" width=40%>

    The Object Spy window displays.

2. In the URL section, input the URL of the website you want to test. We use our demo page in this example: `http://demoaut.katalon.com/`

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/generate_css_xpath_selector_spy_web_utility/object-spy-dialog.png" alt="object spy dialog" width=70%>

3. To choose a browser, click on the dropdown icon of the **Start** button. For this example, we choose a new Chrome browser.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/generate_css_xpath_selector_spy_web_utility/choose-browser.png" alt="choose browser" width=70%>

4. Click **Start**. Katalon Studio opens a new Chrome browser and navigates to the demo website.

5. To capture test objects, first, hover the mouse over them. The focused web object is highlighted in red.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/generate_css_xpath_selector_spy_web_utility/capture-object.png" alt="capture object" width=100%>

    Then, by pressing **\<Alt + \`\>** or right-clicking and choosing **Capture Object**, the focused object is captured and added to the **Captured Objects** list.

    Katalon Studio automatically captures all available properties of the objects. You can change the folder name and edit the value of any properties.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/generate_css_xpath_selector_spy_web_utility/selected-locator.png" alt="selected locator" width="70%">

    In the **Selection Method** section, you can choose **XPath**, **Attributes**, **CSS**, or **Image** to locate captured objects.

6. In the **Selected Locator** section, you can manually input your XPath, then click **Verify and Highlight**. Katalon finds elements that match your XPath locator and highlights them on the web page.

    A single locator might identify many elements because a web page can have many elements that use the same formats and styles. The next section will guide you on how to create unique locators to find complex or dynamic elements. See below: [Working with XPath selector](https://docs.katalon.com/katalon-studio/docs/generate_css_xpath_selector_spy_web_utility.html#working-with-xpath-selector).

7. To save objects to the **Objects Repository**, click on **Save**.
    Then, select a folder to add the captured objects into. Click **OK** when done.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/generate_css_xpath_selector_spy_web_utility/Add-to-repo.png" alt="selected locator" width="70%">

## Working with XPath selector

The following guide shows how to leverage Katalon Studio Spy Web Utility to locate web elements with XPath selector.

These XPath axes methods are used to find complex or dynamic elements.

In the examples below, we are using our demo page: [http://demoaut.katalon.com/](http://demoaut.katalon.com/).

You can find our web sample project available to be downloaded here: [Katalon Web Automation Sample Project](https://github.com/katalon-studio/katalon-web-automation).

### Checking Multiple Attributes

You can identify an element with the combination of multiple attributes to build a unique locator. This method is useful when an element has multiple attributes, but using only one attribute cannot create a unique locator. 

For example, you can identify the login button with multiple attributes, like `@id` and `@type`, to locate the **Login** button.

XPath:

```groovy
//*[@id='btn-login'][@type='submit']
```

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/generate_css_xpath_selector_spy_web_utility/login.png" alt="multiple attributes" width="100%">

### Index

Specify a given tag name in terms of the index value you wish to locate. Use this when there are more than one element present in the DOM with similar attributes and it becomes difficult to search them.

For example, you want to locate the first dropdown in a page.

XPath:

```groovy
//div[@class='form-group']//select[1]
```

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/generate_css_xpath_selector_spy_web_utility/index.png" alt="index" width="100%">

### Chained XPath

You can use multiple XPath expressions and chain them.

For example, use the chained XPath to find the calendar icon in the appointment section.

XPath:

```groovy
//section[@id='appointment']//span[@class='glyphicon glyphicon-calendar']
```

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/generate_css_xpath_selector_spy_web_utility/chained.png" alt="chained" width="100%">

### Contains()

You can use the Contains() method to detect dynamic elements that contain static values.

Example:

Use the Contains() method to find the login button that contains the type: "submit".

XPath:

```groovy
//button[contains(@type,'submit')]
```

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/generate_css_xpath_selector_spy_web_utility/contain-example.png" alt="contain" width="100%">

### Last()

Last() is a method used in an XPath expression. It is used to get the very last node.

Example:

There are 3 social icon links, and you want to get the 3rd item by using `Last()`.

XPath:

```groovy
//ul[@class='list-inline']/li[last()]

```

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/generate_css_xpath_selector_spy_web_utility/last.png" alt="last" width="100%">

### Start-with()

The Start-with method finds the element using the starting text of an attribute. This method is useful when the first part of the attribute value is fixed (static), and the rest is dynamic.

Example:

To find the line: "We Care About Your Health", use the Starts-with() method to find the line that starts with "We Care About".

XPath:

```groovy
//h3[starts-with(text(),'We Care About')]
```

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/generate_css_xpath_selector_spy_web_utility/start-with-example.png" alt="start with" width=100%>

### XPath axes methods

These XPath axes methods are used to find complex or dynamic elements.

* **Following**

    Selects all elements in the document following the current node( ).

    Example:

    By using the following method, you can identify the **Password** text box, which is located after the **Username** name field.

    XPath:

    ```groovy
    .//*[@id='txt-username']//following::input
    ```

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/generate_css_xpath_selector_spy_web_utility/following.png" alt="following" width="100%">

* **Ancestor**

    This method selects all ancestors (parent, grandparent, etc.) of the current node.

    Example:

    In the screenshot below, you want to get the ancestors of the `ul` tag highlighted in red.

    XPath:

    ```groovy
    //ul[@class='list-inline']/ancestor::div
    ```

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/generate_css_xpath_selector_spy_web_utility/ancestor.png" alt="ancestor" width=100%>

* **Child**

    Select all children of the current node.

    Example:

    Using the child method, you can identify all social links as shown in the below screenshot.

    XPath:

    ```groovy
    //ul[@class='list-inline']/child::li
    ```

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/generate_css_xpath_selector_spy_web_utility/child.png" alt="chill" width=100%>

* **Preceding**

    Select all nodes that come before the current node.

    Example:

    Using the preceding method, you can identify all nodes that come before the **Login** button.

    XPath:

    ```groovy
    //*[@id='btn-login']//preceding::input
    ```

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/generate_css_xpath_selector_spy_web_utility/preceding.png" alt="preceding" width=100%>

* **Following-sibling**

    Select the following siblings of the context node. Siblings are at the same level as the current node, as shown in the screen below. It finds the element after the current node.

    Example:

    By using the following-sibling method, you can identify the **Password** text box which located after the **Username** name field.

    XPath:

    ```groovy
    .//*[@id='txt-username']//following::input

    ```
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/generate_css_xpath_selector_spy_web_utility/following-sibling.png" alt="following-sibling" width="100%">