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

## Decision-making statements

> Once a test step is added as any of the control statements, it will **not** be allowed to change it into another keyword.

### In Manual view

Open a test case in **Manual** view, then navigate to **Decision-making Statements** from command toolbar.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/control-statements/image2017-6-30-203A403A1.png)

Refer to the following table for the usage of each statement:

<table>
    <thead>
        <tr>
            <th>Statement</th>
            <th>Description</th>
            <th>Screenshot</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>If</td>
            <td>This statement requires a <strong>boolean condition</strong> as <strong>input value</strong>. Katalon Studio will execute all steps within once the condition is triggered.</td>
            <td>
                <p><img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/control-statements/image2017-2-9-143A233A17.png"></p>
            </td>
        </tr>
        <tr>
            <td>Else If</td>
            <td>Using <strong>Else If</strong> after <strong>If</strong>, you can create a combination of conditions where the steps within the <em>first</em> satisfied condition will be executed.</td>
        </tr>
        <tr>
            <td>Else</td>
            <td>This statement serves as the conclusion of the <strong>If - Else If - Else</strong> structure. The steps within this statement will be executed if <strong>all</strong> the conditions above it are <strong>not</strong> triggered.</td>
        </tr>
        <tr>
            <td>Switch</td>
            <td>This statement requires an expression, which is often referred to as <strong>the control expression</strong> (or <strong>control variable</strong>), as <strong>input value</strong>.</td>
            <td>
                <p><img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/control-statements/image2017-2-9-143A473A59.png"></p>
            </td>
        </tr>
        <tr>
            <td>Case</td>
            <td>
                <p>The <strong>Cases</strong> indicate the assumed value for the <strong>control expression</strong>, with corresponding steps to be executed when a match occurs.</p>
                <p>Each <strong>Case</strong> will have a <strong>Break</strong> by default which should be positioned at the end of the <strong>Case</strong> block to mark the end of it.</p>
            </td>
        </tr>
        <tr>
            <td>Default</td>
            <td>This statement is included automatically within every <strong>Switch</strong> statement. In situation which <strong>no</strong> <strong>Case</strong> value can be matched, the steps within <strong>Default</strong> will be taken.</td>
        </tr>
    </tbody>
</table>

### In Script view

The **Script** view of test cases allows you to programmatically define and handle **If-ElseIf-Else** or **Switch-Case** structure easily using either Groovy or Java language. Refer to [http://groovy-lang.org/semantics.html#\_conditional\_structures](http://groovy-lang.org/semantics.html#_conditional_structures) for more details about conditional structure in Groovy.

For example:

<table>
    <thead>
        <tr>
            <th>Decision-making statement</th>
            <th>Screenshot</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>If - Else If - Else</td>
            <td>
                <p>&nbsp;<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/control-statements/10.png"></p>
            </td>
        </tr>
        <tr>
            <td>Switch - Case</td>
            <td>&nbsp;<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/control-statements/11.png"></td>
        </tr>
    </tbody>
</table>

## Looping statements

> Once a test step is added as any of the control statements, it will **not** be allowed to change it into another keyword.

### In Manual view 

Open a test case in **Manual** view, then navigate to **Looping Statements** from command toolbar.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/control-statements/image2017-6-30-203A403A53.png)

Refer to following table for the usage of each statement:

<table>
    <thead>
        <tr>
            <th>Statement</th>
            <th>Description</th>
            <th>Screenshot</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>For</td>
            <td>This statement accepts a <em>range</em>,<em> list</em> or <em>array</em> as <strong>input value</strong> so that Katalon Studio knows <strong>how many times</strong> to execute all steps within the <strong>For</strong> structure.</td>
            <td>
                <p><img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/control-statements/image2017-2-9-153A493A5.png"></p>
            </td>
        </tr>
        <tr>
            <td>While</td>
            <td>This statement requires a <strong>boolean condition</strong> as <strong>input value</strong> so that Katalon Studio will keep executing all steps within <strong>until the condition fails</strong>.</td>
            <td>
                <p><img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/control-statements/image2017-2-9-153A533A44.png"></p>
            </td>
        </tr>
    </tbody>
</table>

### In Script view

The **Script** View of test cases allows you to programmatically define and handle **For** or **While** structure easily using either Groovy or Java language. Refer to [http://groovy-lang.org/semantics.html#\_looping\_structures](http://groovy-lang.org/semantics.html#_looping_structures) for more details about looping structures in Groovy.

For example:

<table>
    <thead>
        <tr>
            <th>Looping statement</th>
            <th>Screenshot</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>For</td>
            <td>
                <p><img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/control-statements/24.png"></p>
            </td>
        </tr>
        <tr>
            <td>While</td>
            <td>
                <p><img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/control-statements/25.png"></p>
            </td>
        </tr>
    </tbody>
</table>

## Branching statements

> Once a test step is added as any of the control statements, it will **not** be allowed to change it into another keyword.

### In Manual view 

Open a test case in **Manual** view, then navigate to **Branching Statements** from command toolbar.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/control-statements/image2017-6-30-203A413A31.png)

Refer to following table for the usage of each statement:

<table><thead><tr><th>Statement</th><th>Description</th><th>Screenshot</th></tr></thead><tbody><tr><td>Break</td><td>Katalon Studio will exit current code block and continue to next code block / test step.</td><td><p><img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/control-statements/image2017-2-9-163A363A37.png"></p></td></tr><tr><td>Continue</td><td>Katalon Studio will skip the remainder of the current loop and continue with the next iteration of the loop.</td><td><p><img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/control-statements/image2017-2-9-163A423A13.png"></p></td></tr><tr><td>Return</td><td>Katalon will exit from the current method/step, and the flow control is returned to where the method/step was invoked.</td><td><p><img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/control-statements/image2017-2-9-163A473A44.png"></p></td></tr></tbody></table>

### In Script view

The **Script** view of test cases allows you to programmatically define and handle **Break**, **Continue** & **Return** easily using either Groovy or Java language. 

For example:

| Decision-making statement | Screenshot |
| --- | --- |
| Break | ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/control-statements/36.png) |
| Continue | ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/control-statements/37.png) |
| Return | ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/control-statements/38.png) |

## Exception handling block

> Once a test step is added as any of the control statements, it will **not** be allowed to change it into another keyword.

### In Manual view 

Open a test case in **Manual** view, then navigate to **Exception Handling Statements** from command toolbar.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/control-statements/image2017-6-30-203A423A21.png)

Refer to following table for the usage of each statement:

<table><thead><tr><th>Statement</th><th>Description</th><th>Screenshot</th></tr></thead><tbody><tr><td>Try</td><td>This statement indicates that all steps within will be monitored by<strong> exception handlers</strong>.</td><td><p><img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/control-statements/image2017-2-28-113A513A55.png"></p></td></tr><tr><td>Throw</td><td>Before you can <strong>Catch</strong> an exception, some code must throw one. Regardless of what throws the exception, it's always involved with the <strong>Throw</strong> statement</td></tr><tr><td>Catch</td><td>Katalon Studio will&nbsp;execute all steps within when there is any issue occurred during execution of the <strong>Try</strong> block.</td></tr><tr><td>Finally</td><td>This is the last part of the <strong>Try-Catch-Finally</strong> structure and all steps within this will be executed regardless of any exception.</td></tr></tbody></table>

### In Script view

The **Script** view of test cases allows you to programmatically define and handle exception easily using either Groovy or Java language. Refer to [http://groovy-lang.org/semantics.html#\_try\_catch_finally](http://groovy-lang.org/semantics.html#_try_catch_finally) for more details about exception handling in Groovy.

For example:

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/control-statements/image2017-2-28-133A203A32.png)

## Binary Statements

A Binary Statement represents a dual expression consisting of two single **expressions** (variables, strings, numbers, methods...) and an **operator** (e.g. +, -, *, <, <=, !, etc.). Refer to [Groovy Documents](http://groovy-lang.org/operators.html) for more details about using operators in Groovy.

### In Manual view

1. Open a test case in **Manual** view, then navigate to **Binary Statement** from the command toolbar.  

   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/binary-statements/image2017-6-30-203A433A7.png)
2. A test step representing a binary statement is added to the test case.  

   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/binary-statements/image2017-2-10-133A463A52.png)

3. Double-click on the **Input** cell to edit those required components.  

   Binary Statements are normally used to assign either values to test objects

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/binary-statements/Binary-Statement.png" width="675" height="196">

   or test objects to variables to take the next steps.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/binary-statements/BS-2.png" width="665" height="220">

4. Save the test case when you're done.
   
   > Once a test step is added as any of the **Binary Statement**, it will **not** be allowed to change it into another keyword.

### In Script view

The **Script** view of a test case allows you to programmatically define and handle binary statements easily using either Groovy or Java languages.

**For example**:

* To assign a value to a test object

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/binary-statements/BS-1.png" width="337" height="46">

* To assign a test object to a variable

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/binary-statements/BS-3.png" width="528" height="121">

## Method Call Statements

Method Call statement allows you to make calls to other methods provided by the built-in libraries of Katalon Studio.

### In Manual view

1. Open a test case in **Manual** view, then navigate to **Method Call Statement** from command toolbar.  
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/method-call-statements/image2017-6-30-203A443A47.png)  

2. A test step representing a method call is added to the test case.  
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/method-call-statements/image2017-2-10-153A223A34.png)  

3. Double-click on the Input cell to edit the called method.  
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/method-call-statements/image2017-2-10-153A273A26.png)  

4. Save the test case when you're done.
    
    > Once a test step is added as **Method Call Statement**, it will **not** be allowed to change into another keyword.

### In Script view

The **Script** View of a test case allows you to programmatically define and handle method calls easily using either Groovy or Java language.

For example:

 ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/method-call-statements/11.png)

## Assert Statements

An assert statement contains a **boolean expression** where this condition must hold true for the test execution to continue. Thus, execution of the assertion causes evaluation of the **boolean expression** and an error is reported if the expression evaluates as **false**.

### In Manual view

1. Open a test case in **Manual** view, then navigate to **Assert Statements** from command toolbar.  
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/assert-statements/image2017-6-30-203A443A0.png)  
      
    
2. A test step represents assert expression is added to the test case.  
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/assert-statements/image2017-2-10-143A353A6.png)  
      
    
3. Double-click on the **Input** cell to edit the assertion.  
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/assert-statements/image2017-2-10-153A23A25.png)
    
    > Once a test step is added as **Assert Statement**, it will **not** be allowed to change into another keyword.

### In Script view

The **Script** view of test cases allows you to programmatically define and handle assertions easily using either Groovy or Java language. Refer to [http://docs.groovy-lang.org/docs/latest/html/documentation/core-testing-guide.html](http://docs.groovy-lang.org/docs/latest/html/documentation/core-testing-guide.html) for more details regarding assertions in Groovy.

For example:

 ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/assert-statements/11.png)

## Define Method

A method consists of instructions to perform a specific task. Defined methods can be called for being reused later. Refer to [Method Call Statements](/display/KD/Method+Call+Statements) for more details regarding how to call a defined method.

### In Manual view

1. Open a test case in **Manual** view, then select to add **Method** from command toolbar.
   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/define-method/image2017-6-30-203A453A48.png)

2. The **Method builder** dialog is displayed.
  ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/define-method/image2017-2-10-153A483A9.png)
   Specify the required information for your method as following:

   <table><thead><tr><th>Field</th><th>Description</th></tr></thead><tbody><tr><td>Name</td><td>The name of the method.</td></tr><tr><td>Return type</td><td><p>The object type that this method will return after its execution.</p></td></tr><tr><td>Setup, Teardown options</td><td>Select any checkbox to indicate whether it should be a setup() or teardown() method. Refer to <a href="#DefineMethod-SetUp()andTearDown()inManualview">SetUp() and TearDown() in Manual view</a> for more details.</td></tr><tr><td>Parameter list</td><td><p>Any parameter needed to pass into the method.</p><p>By clicking on the <strong>Insert</strong> button, a row will be appended into the grid. You can then change the type and name of the parameter by double clicking and editing the appropriate cell.</p></td></tr></tbody></table>

   Click **OK** after configuring the method details.

3. A test step representing the recently defined method is added to the test case. You can switch to **Script** view to [define content for the method](/display/KD/Define+method#Definemethod-DefineamethodinScriptingview).
   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/define-method/image2017-2-28-143A553A16.png)

4. Save the test case when you're done.

   > Once a test step is defined as **Method**, it will **not** be allowed to change into another keyword.

### In Script view

The **Script** view of a test case allows you to programmatically define and handle methods easily using either Groovy or Java language. Refer to [http://groovy-lang.org/structure.html#_methods](http://groovy-lang.org/structure.html#_methods) for details about methods in Groovy.

For example:

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/define-method/1.png)