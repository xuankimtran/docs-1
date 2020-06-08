---
title: "Parameterize Web Test Objects"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/parameterize-web-objects.html
redirect_from:
    - "/x/A4C9/"
    - "/katalon-studio/docs/parameterize-webmobile-test-object-properties/"
    - "/katalon-studio/docs/parameterize+webmobile+test+object+properties/"
    - "/katalon-studio/docs/parameterize%20webmobile%20test%20object%20properties/"
    - "/display/KD/Parameterized+a+Test+Object"
    - "/display/KD/Parameterized+a+Test+Object/"
    - "/katalon-studio/docs/parameterize-web-test-object-properties.html"
---
## Parameterize Web Test Objects and their properties

With parameterizing test objects, you can update test objects' locators dynamically by using either local or global variables. This feature comes in handy in these use cases:

* You want to perform a bulk action on a group of similar elements without defining multiple Test Objects, such as checking on multiple checkboxes;
* You can only identify an object's locator during runtime because there's a group of similar objects and the chosen one cannot be specified beforehand in test scripts.

Katalon Studio supports parameterizing properties of test objects to handle dynamic objects. Dynamic objects are those that have some particular changes in their properties based on specific business rules. The example below describes how to apply this feature.

Open [the Health Care sample project](https://github.com/katalon-studio-samples/healthcare-tests), navigate to Object Repository/Page_Login.

1. Select the object whose properties you want to parameterize. In this case, the selected test object is `txt_Username`.
2. Capture its locator and create a variable with this syntax `${variable_name}` as a place holder for its dynamic property. For example, we create the `${id}` variable for the `id` property's value. You can parameterize test objects with different selection methods.

* Attributes\
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/param-web-object/attributes.png" width="896" height="398">

* XPath\
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/param-web-object/xpath-id.png" width="606" height="243">

* CSS\
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/param-web-object/css-id.png" width="395" height="130">

3. Using the parameterized test objects.

* **Manual View**

   Open your Test Case in the **Manual View** and double-click on the object that you want to parameterize its properties.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/param-web-object/1.declare.png" width="907" height="466">

   In the displayed **Test Object Input** dialog, declare the expected dynamic property as a variable in the **Variables** panel.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/param-web-object/2.variables-tab.png" width="576" height="697">

  * Param Type: the variable type (The default type is String).
  * Param: the variable name.
  * Value Type: the type of the variable's value.
  * Value: a specific value of that variable.

  In this case, Katalon Studio uses the `id` variable with its specific value as `4TH4T934253&#^%(` to find the `txt_UserName` object.

* **Script View**

   Once the property is declared, you can switch to the **Script View** and adjust the perceived value of the property. Typically, users want to pass the property value as a variable or refer to data files.

   The general syntax to find a test object using a dynamic property is as follows:

   ```groovy
   findTestObject('{your test object}', [('{property}') : '{value of property}'])
   ```

   For example:

  * One dynamic property:

    ```groovy
    findTestObject('Page_Login/txtUserName', ['id' : '48415648'])
    ```

  * Two dynamic properties:

    ```groovy
    findTestObject('Page_Login/txtUserName', ['id' : '48415648', [('name') : 'controler14585']])
    ```

  * Using the variable for the dynamic property's value:

    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/manage-test-object/image2017-6-30-203A223A13.png)

### Example

There are some cases in which you can identify an object's locator only when it's runtime.  In other words, the exact locator of the intended object cannot be specified beforehand in test scripts. In the [Cura Healthcare Center appointment web page](https://katalon-demo-cura.herokuapp.com/profile.php#login), for instance, there are three options of the healthcare program, and the selected one is only known with passing data during execution.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/manage-web-test-object/medicare.png" width="670" height="567">

How can we specify an option in a test script? By parameterizing its locator. You need to create only one Test Object, and you can determine which the exact object is with the passed data during execution.

Now for the exciting part: How do you determine which attribute(s) you have to adjust to parameterize this object's XPath? The answer to this question is mainly based on your knowledge of the web AUT. Knowing the pattern of how similar objects are grouped is the key. In this case, the index's value of **label** **attribute** is the value to parameterize for options on the current web screen.

Depending on your preferred [selection method](https://docs.katalon.com/katalon-studio/docs/working-with-objects-selection-method-for-spyrecord-web.html), including XPath (Smart XPath), Attributes or CSS, the captured object has a corresponding selected locator.

Below steps are how to apply parameterizing test objects in this case:

* Capture the **XPath** locator of those 3 options and save them to the Object Repository in Katalon Studio.

  * **Medicare**: `//*[@id=\"appointment\"]/div/div/form/div[3]/div/label[1]`
  * **Medicaid**: `//*[@id=\"appointment\"]/div/div/form/div[3]/div/label[2]`
  * **None**: `//*[@id=\"appointment\"]/div/div/form/div[3]/div/label[3]`

    As can be seen in the captured XPath locators of those 3 options, they share this same pattern `//*[@id=\"appointment\"]/div/div/form/div[3]/div/label`; hence, in this case, the property variation is the label index.
* In the test object view of the *Medicare* object, create an XPath property and enter the captured XPath locator as its value.
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/param-web-object/label1.png" width="" height="">

* Create a variable as a place holder for the property change in the locator with this syntax: `${Variable_name}`. In this case, it's the label index so we create `[${index}]`.

   Modify this XPath value with that variable. There are two options for you: to parameterize the whole XPath value or merely a part of it.
  * `${index}` = `//*[@id=\"appointment\"]/div/div/form/div[3]/div/label[1]`.
  * `${index}` = `[1]` => the XPath locator: `//*[@id=\"appointment\"]/div/div/form/div[3]/div/label[${index}]`.
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/param-web-object/index.png" width="" height="">

Above is a simple approach to leverage the '**Parameterized Test Object**', a powerful feature. There are other approaches you can apply in your test scripts to reduce the efforts of maintaining many Test Objects at the same time.

### Escaping, special characters

To use a special character like `$` or `\` as a regular one in any place that uses parameterized test objects, prepend it with a backslash: `\` (the so-called escape character).

```groovy
{
 	"productName": ${GlobalVariable.productName},
  	"unit": "\\bottle\",
  	"quantity": 50,
  	"discount": ${ if (productName == "wine") { return 30 } else { return 0}}
	"note": "Currency unit of ${GlobalVariable.productName} is \$."

}
```

* Without `\`: *note: Currency unit of ${GlobalVariable.productName} is $*.
* With `\`: *note: Currency unit of wine is $*.