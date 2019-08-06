---
title: "Binary Statements" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/binary-statements.html 
redirect_from:
    - "/display/KD/Binary+Statements/"
    - "/display/KD/Binary%20Statements/"
    - "/x/rgAM/"
    - "/katalon-studio/docs/binary-statements/"
description: 
---

## Definition

A Binary Statement represents a dual expression consisting of two single **expressions** (variables, strings, numbers, methods...) and an **operator** (e.g. +, -, *, <, <=, !, etc.). Refer to [Groovy Documents](http://groovy-lang.org/operators.html) for more details about using operators in Groovy.

## Usage

### Binary statements in Manual view

1.  Open a test case in **Manual** view, then navigate to **Binary Statement** from the command toolbar.  

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/binary-statements/image2017-6-30-203A433A7.png)  
      
    
2.  A test step representing a binary statement is added to the test case.  

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/binary-statements/image2017-2-10-133A463A52.png)

3.  Double click on the **Input** cell to edit those required components.  

Binary Statements are normally used to assign either values to test objects

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/binary-statements/Binary-Statement.png" width="675" height="196">

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/binary-statements/BS-1.png" width="337" height="46">

or test objects to variables to take the next steps.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/binary-statements/BS-2.png" width="665" height="220">

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/binary-statements/BS-3.png" width="528" height="121">


4.  Save the test case when you're done.
    
    > Once a test step is added as any of the **Binary Statement**, it will **not** be allowed to change it into another keyword.

### Binary statements in Scripting view

The **Script** view of a test case allows you to programmatically define and handle binary statements easily using either Groovy or Java languages.

 ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/binary-statements/11.png)

In the above example, **varA** and **varC** are left expressions; **varB** and **varD** right expression; "**+**" and "**==**" operators.



