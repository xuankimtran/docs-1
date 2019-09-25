---
title: "Custom Keywords Refactoring" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/custom-keywords-refactor.html 
---
Starting from **Katalon Studio version 7.0**, the custom keyword refactoring feature is available.

Specifically, when you move a custom keyword from a package to another one, Katalon Studio updates the new package and keyword identifier in test scripts accordingly.

Here is an example:

1. Open [the shopping cart sample project](https://docs.katalon.com/katalon-studio/docs/shopping-cart-prj.html) and any test case.

2. Create a new package in the Keywords folder. Then drag and drop the `Login` keyword from `Simple` to the newly created package.

3. Re-open the test case and observe. Katalon Studio has updated the package and keyword identifier in the test scripts accordingly.

**Before drag-and-drop**

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/custom-keyword-refactor/package-bf.png" width="" height="">

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/custom-keyword-refactor/identifier-bf.png" width="" height="">

**After drag-and-drop**

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/custom-keyword-refactor/package-aft.png" width="" height="">

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/custom-keyword-refactor/identifier-aft.png" width="" height="">
