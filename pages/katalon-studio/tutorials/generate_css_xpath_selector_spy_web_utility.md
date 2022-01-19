---
title: "Generating reliable object selector using Spy Web utility"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/generate_css_xpath_selector_spy_web_utility.html
redirect_from:
    - "katalon-studio/tutorials/generate_css_xpath_selector_spy_web_utility.html"
description: "Katalon Studio Spy Web Utility provides an intelligent object capturing capability and immediate feedback on CSS Selector & Xpath selector. Learn more!"
---
Katalon Studio Spy Web Utility provides an intelligent object capturing capability and immediate feedback on the uniqueness of selectors. To learn more about this utility, see [Spy Web Utility](http://docs.katalon.com/pages/viewpage.action?pageId=5117668).

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

1. Click on **Spy Web** on the Katalon Studio main toolbar.

    ![Find-Object-locators](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/generate_css_xpath_selector_spy_web_utility/Find-Object-locators.png)

2. The Object Spy window is shown as the following.

    ![The-Object-Spy-window](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/generate_css_xpath_selector_spy_web_utility/The-Object-Spy-window.png)

3. Type the application URL in the URL text box and select the desired browser.  Click on **Start**.

    ![application URL in Object Spy](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/generate_css_xpath_selector_spy_web_utility/application-URL-in-Object-Spy.png)

    Once you click on Start, Katalon Studio will launch the browser and navigates to the respective website.

4. To capture test objects, hover the mouse over them. The focused web object would be highlighted.

    ![Capture-test-objects](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/generate_css_xpath_selector_spy_web_utility/Capture-test-objects.png)

    By pressing the <Alt + ~> keys the focused object will be highlighted green, which means that it has been stored in the Captured Objects list.

    Katalon Studio will automatically capture all available properties of captured objects. You can change the folder name and edit the value of any properties.

    ![Locate captured Xpath selector](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/generate_css_xpath_selector_spy_web_utility/Locate-captured-objects.png)

Katalon Studio allows users to select **Selection Method** to locate captured objects. **Basic mode** is recommended to manual testers who just started automation journey. With **Basic** mode, Katalon Studio's intelligent selector generator will **automatically generate** a robust and unique XPath **selector** which combined all properties of captured objects.

For advanced testers who wish to **manually input selectors** have the option to select between **CSS** or **XPath mode**.

Click on **Add** to **Object Repository** from the command toolbar to save objects in Objects Repository. Select a folder to add the captured objects into. Click **OK** when done.
