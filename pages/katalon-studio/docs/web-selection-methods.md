---
title: "Selection Methods for Web Tests"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/web-selection-methods.html
---

This article guides you through how to choose different strategies to locate WebUI objects in Katalon Studio.

## Configure Test Design

To set the default selection method used in Spy/Recorder of a project:

* From 7.6.0 backward: Go to **Project > Settings > Test Design > Web Locators**.
* From 7.6.0 onwards: Go to **Project > Settings > Test Design > Web UI**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/selection-methods/project-settings.png" width="100%" alt="web UI settings">

Select one of these provided options:

* [XPath](http://docs.katalon.com/katalon-studio/docs/web-selection-methods.html#xpath): Once a test object is captured by using Spy/Recorder, a set of XPath locators are generated. The first value is the object's default XPath locator.
* [Attributes](http://docs.katalon.com/katalon-studio/docs/web-selection-methods.html#attributes)
* [CSS](http://docs.katalon.com/katalon-studio/docs/web-selection-methods.html#css)
* [Image](http://docs.katalon.com/katalon-studio/docs/web-selection-methods.html#image)

If you choose XPath or Attributes, you need to configure some additional settings.

### Configure XPath

You can set the priority of XPath locators by drag and drop the XPath locators list. 

To return to the default order, click **Reset Default**.

Below is a list of  XPath captured strategies:

<table>
	<thead>
		<tr>
			<th>
				<p>XPath captured strategy</p>
			</th>
			<th>
				<p>Description</p>
			</th>
			<th>
				<p>Example</p>
			</th>
		</tr>
    </thead>
    <tbody>
        <tr>
			<td>
				<p>xpath:link</p>
			</td>
			<td>
				<p>Builds XPath locator for specifically the link element</p>
			</td>
			<td>
				<p>//a[contains(text(), 'Katalon Studio')]</p>
			</td>
		</tr>
		<tr>
			<td>
				<p>xpath:img</p>
			</td>
			<td>
				<p>Builds XPath locator for specifically the image element</p>
			</td>
			<td>
				<p>//img[@alt="Katalon logo"]</p>
			</td>
		</tr>
		<tr>
			<td>
				<p>xpath:attributes</p>
			</td>
			<td>
				<p>Builds XPath locator that's based on the selected element&rsquo;s tag name and its attributes.</p>
				<br />
				<p>There are 5 preffered attributes to build the element locators: ['id', 'name', 'value', 'type', 'action', 'onclick'].</p>
				<br />
				<p>If the element has more than one of those attributes, the locator will combine the attributes with an operator.</p>
			</td>
			<td>
				<p>//div[@id="search"]</p>
				<p>//select[@id="cars" and @name="cars"]</p>
				<p>//input[@type="submit" and @value="Submit"]</p>
			</td>
		</tr>
		<tr>
			<td>
				<p>xpath:idRelative</p>
			</td>
			<td>
				<p>Builds XPath locator that is the relative XPath from the nearest parent that has id attributes.</p>
			</td>
			<td>
				<p>//div[@id="search"]/a</p>
				<p>//select[@id="cars"]/div/div[2]/input[@type="submit"]</p>
			</td>
		</tr>
		<tr>
			<td>
				<p>xpath:href</p>
			</td>
			<td>
				<p>Builds XPath locator of an element that has href attribute that match or contains the given value.</p>
			</td>
			<td>
				<p>//a[@href='https://katalon.com']</p>
				<p>//a[contains(@href, 'katalon')]</p>
			</td>
		</tr>
		<tr>
			<td>
				<p>xpath:position</p>
			</td>
			<td>
				<p>Builds XPath locator that is the absolute XPath of the selected element</p>
			</td>
			<td>
				<p>/html/body/div[1]/div[1]/div/div[3]/div[2]/div</p>
				<p>/html/body/section/div/div[2]/div[5]/div[2]/div/div/div[2]/table/tbody/tr[13]/td[1]/div/a/span[3]/span</p>
			</td>
		</tr>
		<tr>
			<td>
				<p>xpath:customAttributes</p>
			</td>
			<td>
				<p>Builds XPath locator based on the selected element tag name and its attributes. The XPath value combines one or more attributes of all default and customized attributes. (Available from version 8.2.5)</p>
			</td>
			<td>
				<p>//&lt;tagname&gt;[@id='1234' and @custom1 = 'a1' and @custom2 = 'a2' and @custom3 = 'a3' and @custom4 = 'a4']</p>
				<br />
				<p>Other examples:</p>
				<br />
				<p>//div[@id="search" and @custom1 = 'a1']</p>
				<p>//select[@id="cars" and @name="cars" and @custom1 = 'a1' and @custom2 = 'a2']</p>
				<p>//input[@type="submit" and @value="Submit" and @custom2 = 'a2' and @custom3 = 'a3' and @custom4 = 'a4']</p>
			</td>
		</tr>
		<tr>
			<td>
				<p>xpath:neighbor</p>
			</td>
			<td>
				<p>Build XPath locator based on the more robust neighbors of the selected element.</p>
			</td>
			<td>
				<p>(.//*[normalize-space(text()) and normalize-space(.)=&rsquo;How AI can save our humanity&rsquo;])[2]/preceding::div[3]</p>
			</td>
		</tr>
		<tr>
			<td>
				<p>dom:name</p>
			</td>
			<td>
				<p>Identify and locate a web element using DOM (Document Object Model). This applies only to elements within a named form.</p>
			</td>
			<td>
				<p>"document.forms["home"].elements["userName"]"</p>
			</td>
		</tr>
	</tbody>
</table>

### Configure Attributes

You can select the attributes used for detecting an object. 

* To return to the default setting, slick **Reset Default**.
* To add new attributes, click on the **Add** icon.
* To delete an attributes, select the attributes and click **Delete**.
* To delete all attributes, click **Clear**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/selection-methods/xpath-attribute.png" alt="configure attribute" width="100%">

## Switch Selection Method in an object view

In an object view, you can freely switch from one selection method to another. The detailed content of each selection method is saved automatically.

In an object view, you can:

* Choose an object locating strategy among XPath, Attributes, CSS or Image
* Check only preferred properties of an object
* Input a desired XPath or CSS locator in the Selector Editor manually

## XPath

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/selection-methods/object-view.png" alt="object view" width="100%">

For better object recognition, Katalon Studio supports Smart XPath (a.k.a Relative XPath). If an element cannot be consistently located using its direct attributes, Katalon Studio identifies the element by using its more robust neighbors. This method is visually intuitive as it reflects the way users often identify a visible element on the user interface.

Working with XPath, you can:
* Set the priority of XPath locators while with Attributes.
* Decide which object properties to be used for recognizing objects.
* Override the global settings in a specific object: Open an object view, configure a selection method used for this object particularly.

If **XPath** is set as the default selection method when spying and recording, Katalon Studio generates a list of **Smart XPaths** automatically.

> [Learn more about how Katalon detects objects with XPath](https://docs.katalon.com/katalon-studio/tutorials/detect_elements_xpath.html)

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/selection-methods/object-spy.png" alt="object spy" width="70%">

## Attributes

A test object is typically built up by several properties. During test execution, Katalon Studio uses them to detect an object.

If **Attributes** is set as the default selection method during spying and recording, Katalon Studio generates **XPath** locator automatically that combines all the selected object properties to locate that object. Again, you can check/uncheck preferred properties in the **Object's Properties** table.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/selection-methods/attribute.png" alt="attributes" width=100%>

## CSS

Those who wish to input their **CSS** locator of a test object manually can select the **CSS** option. Open an object's view and enter a **CSS** locator value in **Selector Editor**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/selection-methods/css.png" alt="CSS" width="70%">

### Change the CSS selector of an object at runtime

To change a Test Object's CSS value at runtime, you can use the following code snippet:

```java
import com.kms.katalon.core.testobject.SelectorMethod

TestObject to = findTestObject('your_test_object_id')

//Change value of CSS selector
to.setSelectorValue(SelectorMethod.CSS, 'your_desired_value')

//Change selection method from another selector to CSS selector
to.setSelectorMethod(SelectorMethod.CSS)
```

See also:

* [getSelectorCollection](https://docs.katalon.com/javadoc/com/kms/katalon/core/testobject/TestObject.html#getSelectorCollection())
* [getSelectorMethod](https://docs.katalon.com/javadoc/com/kms/katalon/core/testobject/TestObject.html#getSelectorMethod())
* [setSelectorMethod](https://docs.katalon.com/javadoc/com/kms/katalon/core/testobject/TestObject.html#setSelectorMethod(com.kms.katalon.core.testobject.SelectorMethod))
* [setSelectorValue](https://docs.katalon.com/javadoc/com/kms/katalon/core/testobject/TestObject.html#setSelectorValue(com.kms.katalon.core.testobject.SelectorMethod,%20java.lang.String))

## Image

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/selection-methods/image.png" alt="image" width="70%">

From 7.2.2 onwards, Katalon supports [visual object recognition](https://docs.katalon.com/katalon-studio/docs/manage-web-test-object.html#visual-object-recognition). You can learn more about [how to create image property for an object](https://docs.katalon.com/katalon-studio/docs/web-image-based-object-recognition.html)

See also

* [Self-healing Tests](https://docs.katalon.com/katalon-studio/docs/self-healing.html)
* [Generate reliable object locators](https://docs.katalon.com/katalon-studio/docs/generate_css_xpath_selector_spy_web_utility.html)
