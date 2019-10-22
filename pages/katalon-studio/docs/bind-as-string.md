---
title: "Enhanced Variable Binding" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/bind-as-string.html 
description: Update new feature starting from v6.3.0
---

> Starting from version 6.3.0, variable binding can be configured to read test data values as the intended data types. This feature is only applicable for Test data of type Excel and Database.

You can enable this feature to obtain old variable binding behaviors. Old test data continue to be read as string to ensure that we don't break existing test cases.

In this example, we create a test suite and a test case with variables. _booleanVar_ is a test case variable of type Boolean; _numberVar_ a test case variable of type Number; and, _stringVar_ a test case variable of type String.

<table>
    <thead>
        <tr>
            <th>Boolean</th>
            <th>Integer</th>
            <th>String</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>TRUE</td>
            <td>1</td>
            <td>one</td>
        </tr>
        <tr>
            <td>FALSE</td>
            <td>2</td>
            <td>zero</td>
        </tr>
        <tr>
</table>

* Create the following custom keyword **TestDataKeyword**:

```groovy
public class testdata {
	
	public static void printString(String str) {
		println str;
	}
	
	public static void printInt(BigDecimal integer) {
		println integer;
	}
	
	public static void printBoolean(boolean bool) {
		println bool;
	}
	
}
```

* Use them in the test case Sample Test Case as followed:

```groovy
TestDataKeyword.takeBooleanAndPrint(booleanVar);
TestDataKeyword.takeNumberAndPrint(numberVar);
TestDataKeyword.takeStringAndPrint(stringVar);
```

where _booleanVar_, _numberVar_, _stringVar_ are test case variables.

## Variable binding for Test Data with option _bind to test case as string_ enabled

* Create a Test Data with the data provided above and the _bind to test case as string_ option enabled.

    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/bind-as-string/option-enabled.png)

* Follow [this document](https://docs.katalon.com/katalon-studio/docs/run-test-case-external-data.html) to run the test case, and then we will have the result as below:

    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/bind-as-string/2-failed.png)

    The test suite should fail when the first keyword function *takeBooleanAndPrint* does not expect a String; however, due to the enabled _bind to test case as string_ option, the test data values are read as string.

## Variable binding for Test Data with option _bind to test case as string_ disabled

* Create a Sample Test Data with option _bind to test case as string_ disabled.

    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/bind-as-string/option-disabled.png)

* Repeat the same steps as above, and then we have the result as below:

    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/bind-as-string/4-passed.png)
    
    The test suite should pass because _bind to test case as string_ is disabled. Test data values are read as-is, and all keyword functions receive their expected data types.

> **Quick tips**
>
>* To push customizability further, Katalon now supports an annotation called `BeforeTestDataBindToTestCase` which allows the annotated functions to operate on Test Data variables before they are bound to test cases.
>* Before Katalon 6.3, you would have to compile another set of Test Data for each requirement. Increasingly varied requirements would then further complicate Test Data management.
>* Starting from version 6.3, you need one raw Test Data file and then define the rules of transformation in different functions using the new annotation. With this feature, deciding how Test Data variables are used occurs at run-time.
