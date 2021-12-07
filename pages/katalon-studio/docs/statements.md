---
title: "Statements"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/statements.html
redirect_from:
    - "/katalon-studio/docs/method-call-statements.html"
    - "/display/KD/Method+Call+Statements/"
    - "/display/KD/Method%20Call%20Statements/"
    - "/x/sgAM/"
    - "/katalon-studio/docs/method-call-statements/"
    - "/katalon-studio/docs/control-statements.html"
    - "/display/KD/Control+Statements/"
    - "/display/KD/Control%20Statements/"
    - "/x/rAAM/"
    - "/katalon-studio/docs/control-statements/"
    - "/katalon-studio/tutorials/common_condition_control_statements.html"
    - "/display/KD/Control+Statements#ControlStatements-Decision-makingstatements"
    - "/display/KD/Control+Statements#ControlStatements-Loopingstatements"
    - "/display/KD/Control+Statements#ControlStatements-Branchingstatements"
    - "/display/KD/Control+Statements#ControlStatements-Exceptionhandlingblock"
    - "/katalon-studio/docs/binary-statements.html"
    - "/display/KD/Binary+Statements/"
    - "/display/KD/Binary%20Statements/"
    - "/x/rgAM/"
    - "/katalon-studio/docs/binary-statements/"
    - "katalon-studio/docs/assert-statements.html"
    - "/display/KD/Assert+Statements/"
    - "/display/KD/Assert%20Statements/"
    - "/x/sAAM/"
    - "/katalon-studio/docs/assert-statements/"
    - "/tutorials/common-validation/"
    - "/katalon-studio/tutorials/common_validation_statements_katalon_studio.html"
    - "/katalon-studio/docs/define-method.html"
    - "/display/KD/Define+Method/"
    - "/display/KD/Define%20Method/"
    - "/x/tgAM/"
    - "/katalon-studio/docs/define-method/"
    - "/display/KD/Define+method/"
description: 
---

In Katalon Studio, you can add statements as test steps. There are seven types of statements:

* Decision-making Statements
* Looping Statements
* Branching Statements
* Exception Handling Statements
* Binary Statement
* Assert Statement
* Method Call Statement

This article guides you through how to add these statements to your test case and how to define a method in both manual and script view.
## Decision-making Statements

> Once a test step is added as any of the control statements, it is not allowed to change into another keyword.

### In Manual view

Open a test case in **Manual** view. Click on the drop-down icon of the **Add** button, then choose **Decision-making Statements**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/statements/statement.png" alt="add statements" width="70%">

To add a keyword under a statement, select that statement then click **Add**. A test step is created under that statement.

Refer to the following table and example for the usage of each statement:

* **If - Else If - Else**:

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/statements/if-else.png" alt="if-else statements" width="100%">

<table>
    <thead>
        <tr>
            <th>Statement</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>If</td>
            <td>This statement requires a boolean condition as an input value. Once the condition is triggered, Katalon Studio starts executing all steps within.</td>
        </tr>
        <tr>
            <td>Else If</td>
            <td>Using <strong>Else If</strong> after <strong>If</strong>, you can create a combination of conditions where the steps within the first satisfied condition start being executed.</td>
        </tr>
        <tr>
            <td>Else</td>
            <td>This statement serves as the conclusion of the <strong>If - Else If - Else</strong> structure. If all the conditions above it are not triggered, test steps within this statement start being executed.</td>
        </tr>
    </tbody>
</table>

* **Switch - Case**:

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/statements/switch-case-default.png" alt="switch statement" wisth="100%">

<table>
    <thead>
        <tr>
            <th>Statement</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
            <td>Switch</td>
            <td>This statement requires an expression, which is often referred to as the  <strong>control expression</strong> (or <strong>control variable</strong>), as <strong>input value</strong>.</td>
        </tr>
        <tr>
            <td>Case</td>
            <td>
                <p>The <strong>Cases</strong> indicate the assumed value for the <strong>control expression</strong>, with corresponding steps to be executed when a match occurs.</p>
                <p>Each <strong>Case</strong> has a <strong>Break</strong> by default, which should be positioned at the end of the <strong>Case</strong> block to mark the end of it.</p>
            </td>
        </tr>
        <tr>
            <td>Default</td>
            <td>This statement is included automatically within every <strong>Switch</strong> statement. In situation which <strong>no</strong> <strong>Case</strong> value can be matched, the steps within <strong>Default</strong> will be taken.</td>
        </tr>
    </tbody>
</table>

### In Script view

The **Script** view of test cases allows you to programmatically define and handle **If-ElseIf-Else** or **Switch-Case** structure using either Groovy or Java language. For more details about conditional structure in Groovy, refer to this Groovy documentation: [Control structures](http://groovy-lang.org/semantics.html#_conditional_structures).

For example:

* **If - Else If - Else**:

    ``` groovy

    if (true) {
        WebUI.click(findTestObject('Page_CuraAppointment/chk_Medicaid'), FailureHandling.STOP_ON_FAILURE)
    } else if (true) {
        WebUI.click(findTestObject('Page_CuraAppointment/chk_Medicare'), FailureHandling.STOP_ON_FAILURE)
    } else {
        WebUI.click(findTestObject('Page_CuraAppointment/chk_None'), FailureHandling.STOP_ON_FAILURE)
    }
    ```

* **Switch - Case**:

    ``` groovy

    switch (true) {
        case true:
            WebUI.click(findTestObject('Page_CuraAppointment/chk_Medicaid'), FailureHandling.STOP_ON_FAILURE)

            break
        case true:
            WebUI.click(findTestObject('Page_CuraAppointment/chk_Medicare'), FailureHandling.STOP_ON_FAILURE)

            break
        default:
            WebUI.click(findTestObject('Page_CuraAppointment/chk_None'), FailureHandling.STOP_ON_FAILURE)

            break
    }
    ```

## Looping Statements

> Once a test step is added as any of the control statements, it is not allowed to change into another keyword.

### In Manual view 

Open a test case in **Manual** view. Click on the drop-down icon of the **Add** button, then choose **Looping Statements**.

To add a keyword under a statement, select that statement then click **Add**. A test step is created under that statement.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/statements/for-while.png" alt="looping statement" width="70%">

Refer to following table for the usage of each statement:

<table>
    <thead>
        <tr>
            <th>Statement</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>For</td>
            <td>This statement accepts a <em>range</em>,<em> list</em> or <em>array</em> as <strong>input value</strong> so that Katalon Studio knows <strong>how many times</strong> to execute all steps within the <strong>For</strong> structure.</td>
        </tr>
        <tr>
            <td>While</td>
            <td>This statement requires a <strong>boolean condition</strong> as <strong>input value</strong> so that Katalon Studio will keep executing all steps within <strong>until the condition fails</strong>.</td>
        </tr>
    </tbody>
</table>

### In Script view

The **Script** view of test cases allows you to programmatically define and handle **For** or **While** structure using either Groovy or Java language. For more details about looping structures in Groovy, refer to this Groovy documentation: [Looping Structures](http://groovy-lang.org/semantics.html#_looping_structures).

For example:

* **For**:

``` groovy

for (def index : (0..5)) {
    WebUI.acceptAlert(FailureHandling.STOP_ON_FAILURE)
}
```

* **While**:

``` groovy

while (varA == true) {
    WebUI.acceptAlert(FailureHandling.STOP_ON_FAILURE)
}
```

## Branching Statements

> Once a test step is added as any of the control statements, it is not allowed to change into another keyword.

### In Manual view 

Open a test case in **Manual** view. Click on the drop-down icon of the **Add** button, then choose **Branching Statements**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/statements/branching-statement.png" alt="branching statement" width="70%">

To add a keyword under a statement, select that statement then click **Add**. A test step is created under that statement.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/statements/break-continue-return.png" alt="branching statement in manual view" width="100%">

Refer to following table for the usage of each statement:

<table>
    <thead>
        <tr>
            <th>Statement</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Break</td>
            <td>Katalon Studio exits current code block and continue to next code block/ test step.</td>
        </tr>
        <tr>
            <td>Continue</td>
            <td>Katalon Studio skips the remainder of the current loop and continues with the next iteration of the loop.</td>
        </tr>
        <tr>
            <td>Return</td>
            <td>Katalon exits from the current method/ step, and the flow control is returned to where the method/step was invoked.</td>
        </tr>
    </tbody>
</table>

### In Script view

The **Script** view of test cases allows you to programmatically define and handle **Break**, **Continue** and **Return**, using either Groovy or Java language. 

For example:

* **Break**:

``` groovy
for (int i = 0; i < max; i++) {
	// interested only in p's
	if (searchMe.charAt(i) != 'p') {
		break;
	}
	
	// process p's
	numPs++;
}
```

* **Continue**:

``` groovy
for (int i = 0; i < max; i++) {
	// interested only in p's
	if (searchMe.charAt(i) != 'p') {
		continue;
	}
	
	// process p's
	numPs++;
}
```

* **Return**:

``` groovy
for (int i = 0; i < max; i++) {
	// interested only in p's
	if (searchMe.charAt(i) != 'p') {
		return true;
	}
	
	// process p's
	numPs++;
}
```

## Exception Handling statements

> Once a test step is added as any of the control statements, it is not allowed to change into another keyword.

### In Manual view 

Open a test case in **Manual** view. Click on the drop-down icon of the **Add** button, then choose **Exception Handling Statements**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/statements/exception-handling-statements.png" alt="exception handling statement" width="70%">

To add a keyword under a statement, select that statement then click **Add**. A test step is created under that statement.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/statements/exception-handling.png" alt="exception handling statements in manual view" width="100%">

Refer to following table for the usage of each statement:

<table>
    <thead>
        <tr>
            <th>Statement</th>
            <th>Description</th><
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Try</td>
            <td>This statement indicates that all steps within is monitored by<strong> exception handlers</strong>.</td>
        </tr>
        <tr>
            <td>Throw</td>
            <td>Some code must throw an exception before you can <strong>Catch</strong> an exception. Regardless of what code throws the exception, it is always involved with the <strong>Throw</strong> statement.</td>
        </tr>
        <tr>
            <td>Catch</td>
            <td>When there is any issue occurred during execution of the <strong>Try</strong> block, Katalon Studio executes all steps within.</td>
        </tr>
        <tr>
            <td>Finally</td>
            <td>This is the last part of the <strong>Try-Catch-Finally</strong> structure. All steps within this is executed regardless of any exception.</td>
        </tr>
    </tbody>
</table>

### In Script view

The **Script** view of test cases allows you to programmatically define and handle exception using either Groovy or Java language. For more details about exception handling in Groovy, refer to this Groovy documentation: [Try - Catch - Finally](http://groovy-lang.org/semantics.html#_try_catch_finally).

For example:

``` groovy
    try {
        WebUI.openBrowser('')

        WebUI.navigateToUrl('katalon.com')

        if (WebUI.getText(findTestObject('Object Repository/txt_singin')).length() < 0) {
            throw new com.kms.katalon.core.exception.StepFailedException('Value required')
        }
    }
    catch (StepErrorException e) {
        this.println(e)
    } 
    catch (Exception e) {
        this.println("General issue occurs.")
    } 
    finally { 
        this.println("Navigate to a page.")
    }
```

## Binary Statements

A Binary statement represents a dual expression consisting of two single **expressions** (variables, strings, numbers, methods...) and an operator, for example: +, -, *, <, <=, !, etc.). For more details about using operators in Groovy, refer to this Groovy documentation: [Operators](http://groovy-lang.org/operators.html).

### In Manual view

1. Open a test case in **Manual** view. Click on the drop-down icon of the **Add** button, then choose **Binary Statements**.

    To add a keyword under a statement, select that statement then click **Add**. A test step is created under that statement.  

   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/binary-statements/image2017-6-30-203A433A7.png)

2. A test step representing a binary statement is added to the test case.  

   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/binary-statements/image2017-2-10-133A463A52.png)

3. Double-click on the **Input** cell to edit those required components.  

   Binary statements are normally used to assign either values to test objects

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/binary-statements/Binary-Statement.png" width="70%">

   or test objects to variables to take the next steps.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/binary-statements/BS-2.png" width="70%">

4. Save the test case when you're done.
   
   > Once a test step is added as any of the **Binary Statement**, it is not allowed to change into another keyword.

### In Script view

The **Script** view of a test case allows you to programmatically define and handle binary statements using either Groovy or Java languages.

**For example**:

* To assign a value to a test object

    ``` groovy
    myText = 'Welcome to Katalon Studio'
    ```

* To assign a test object to a variable

    ``` groovy
    myObject = findTestObject('my object')
    WebUI.setText(myObject, 'Welcome to Katalon Studio')
    WebUI.verifyTextPresent('Welcome to Katalon Studio', false)
    ```

## Method Call Statements

Method Call statement allows you to make calls to other methods provided by the built-in libraries of Katalon Studio.

### In Manual view

1. Open a test case in **Manual** view. Click on the drop-down icon of the **Add** button, then choose **Method Call Statements**.

    To add a keyword under a statement, select that statement then click **Add**. A test step is created under that statement.  

    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/method-call-statements/image2017-6-30-203A443A47.png)  

2. A test step representing a method call is added to the test case.

    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/method-call-statements/image2017-2-10-153A223A34.png)  

3. Double-click on the Input cell to edit the called method.

    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/method-call-statements/image2017-2-10-153A273A26.png)  

4. Save the test case when you're done.
    
    > Once a test step is added as **Method Call Statement**, it is not allowed to change into another keyword.

### In Script view

The **Script** View of a test case allows you to programmatically define and handle method calls easily using either Groovy or Java language.

For example:

``` groovy
WebUiBuiltInKeywords.openBrowser('', FailureHandling.STOP_ON_FAILURE)
WebUiBuiltInKeywords.navigateToUrl(GlobalVariable.global_Gmail_Url, FailureHandling.STOP_ON_FAILURE)
WebUiBuiltInKeywords.setText(ObjectRepository.findTestObject(null), 'varA'.toString(), FailureHandling.STOP_ON_FAILURE)
Integer.notifyAll()
```

## Assert Statements

An assert statement contains a **boolean expression** where this condition must hold true for the test execution to continue. Thus, execution of the assertion causes evaluation of the **boolean expression** and an error is reported if the expression evaluates as **false**.

### In Manual view

1. Open a test case in **Manual** view. Click on the drop-down icon of the **Add** button, then choose **Assert Statements**.

    To add a keyword under a statement, select that statement then click **Add**. A test step is created under that statement.

    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/assert-statements/image2017-6-30-203A443A0.png)  
      
    
2. A test step represents assert expression is added to the test case.  
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/assert-statements/image2017-2-10-143A353A6.png)  
      
    
3. Double-click on the **Input** cell to edit the assertion.  
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/assert-statements/image2017-2-10-153A23A25.png)
    
    > Once a test step is added as **Assert Statement**, it is not allowed to change into another keyword.

### In Script view

The **Script** view of test cases allows you to programmatically define and handle assertions using either Groovy or Java language. For more details regarding assertions in Groovy, refer to this Groovy documentation: [Core Testing Guide.html](http://docs.groovy-lang.org/docs/latest/html/documentation/core-testing-guide.html).

For example:

``` groovy
WebUiBuiltInKeywords.openBrowser('', FailureHandling.STOP_ON_FAILURE)
WebUiBuiltInKeywords.navigateToUrl(GlobalVariable.global_Gmail_Url, FailureHandling.STOP_ON_FAILURE)
assert varA == true
```

## Define Method

A method consists of instructions to perform a specific task. Defined methods can be called for being reused later. For more details regarding how to call a defined method, refer to [Method Call Statements](/display/KD/Method+Call+Statements) .

### In Manual view

1. Open a test case in **Manual** view. Click on the drop-down icon of the **Add** button, then choose **Method**.

    To add a keyword under a statement, select that statement then click **Add**. A test step is created under that statement.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/statements/method-statement.png" alt="method statement" width="50%">

2. The **Method builder** dialog is displayed.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-listeners-test-hooks/method-builder.png" alt="method builder" width="80%">

   Specify the required information for your method as following:

<table>
    <thead>
        <tr>
            <th>Field</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Name</td>
            <td>The name of the method.</td>
        </tr>
        <tr>
            <td>Return type</td>
            <td><p>The object type that this method will return after its execution.</p></td>
        </tr>
        <tr>
            <td>Setup, Teardown options</td>
            <td>Select any checkbox to indicate whether it should be a setup() or teardown() method. Refer to <a href="#DefineMethod-SetUp()andTearDown()inManualview">SetUp() and TearDown() in Manual view</a> for more details.</td>
        </tr>
        <tr>
            <td>Parameter list</td>
            <td><p>Any parameter needed to pass into the method.</p><p>By clicking on the <strong>Insert</strong> button, a row will be appended into the grid. You can then change the type and name of the parameter by double clicking and editing the appropriate cell.</p></td>
        </tr>
    </tbody>
</table>

   After configuring the method details, click **OK**

3. A test step representing the recently defined method is added to the test case. You can switch to the script view to define content for the method.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-listeners-test-hooks/setup-teardown-manual.png" alt="setUp and tearDown in manual view" width="100%">

4. When you're done, save the test case.

   > Once a test step is defined as **Method**, it is not allowed to change into another keyword.

### In Script view

The **Script** view of a test case allows you to programmatically define and handle methods easily using either Groovy or Java language. For details about methods in Groovy, refer to Groovy documentation: [Methods](http://groovy-lang.org/structure.html#_methods).

For example:

* **Method declaration**:

    ``` groovy
    Integer myMethod(def param1, def param2) {
        return param1 + param2
    }
    ```

* **Method call**:

    ``` groovy
    myVar = myMethod1(varA, varB)
    ```
