---
title: "Handle conditional cases in your tests"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-recorder/docs/conditional-cases.html
description:
---

Katalon Recorder supports the following flow control methods:
- Branching.
- Loops


## Branching

Conditional branching allows your test to behave differently based on certain conditions.

### if
The `if` command opens a conditional branch. The target of an `if` command is an expression that evaluates to either `true` or `false`. The expression can be a JavaScript expression with variables. If the expression evaluates to `true`, all the steps following `if`  will be executed until a `else if`, `else` or `endif` command is found.

### else if
The `elseif` command is similar to the `if` command. If the steps between `if` and `elseif` are not executed, the expression in `elseif` will be evaluated. If the expression evaluates to `true`, all commands following `elseif` will be executed until a `else if`, `else`, or `endif` command is found.

### else
The `else` command usually follows the  `if` command. If the steps between `if` and `else` are not executed, the steps following `else` will be executed until a `endif` command is found.

### endif
The `endif` command terminates the conditional branching block. You need to add `endif` to your test, otherwise you will get an error message.

## Looping

Looping allows you to repeat steps until a condition is met.

### while
The `while` command starts a loop. The target of a `while` command is an expression that evaluates to either `true` or `false`. The expression can be a JavaScript with variables. If the expression evaluates to `true`, the steps following `while` will be executed until `endwhile` is found and the expression evaluates again. The steps between `while` and `endwhile` will be executed repeatedly until the expression evaluates to `false`.

### endWhile
The `endif` command terminates the looping branching block. You need to add `endif` to your test, otherwise you will get an error message.


## Sample Projects
Katalon Recorder comes with some sample projects (templates) to help you get started with flow controls.
1. In Katalon Recorder, go to Templates.
2. Choose *Conditional and loops* from the left-side bar.
3. Check the sample projects.
4. Click on the **Add Templates** button.

You should see the sample projects are added to your workspace.