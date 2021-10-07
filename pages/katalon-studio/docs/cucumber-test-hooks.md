---
title: "Create Cucumber Test Hooks" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/cucumber-test-hook.html
redirect_from:
description: 
---

The integration of Cucumber framework in Katalon Studio allows you to include Cucumber test hooks, which work at the start and the end of a scenario in a behavior-driven development (BDD) test. To learn more about test hooks in Cucumber framework, you can refer to this document: [Cucumber reference](https://cucumber.io/docs/cucumber/api/#hooks)

This guide shows you how to create and use Cucumber hooks in Katalon Studio.

## Set up Cucumber Hooks

### Create Feature file
To apply hooks in Cucumber BDD test, first you need to create a Cucumber Feature file and its corresponding Step definitions. Follow this guide to set up your Feature file: [Add Feature files and Step definitions](https://docs.katalon.com/katalon-studio/docs/cucumber-features-file.html)

### Add Cucumber Hooks

1. Create a separate Step definition or Custom Keyword that includes the Cucumber hooks:

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/cucumber-test-hooks/KS-sample-test-hooks.png" width="100%" alt="Sample test hooks">

2. Run the Feature file or test case and test suite that include the Cucumber Keyword and verify the message of Cucumber hooks in **Console** log:

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/cucumber-test-hooks/KS-test-hooks-log.png" width="100%" alt="Test hooks log in Console">

**See also**: 

* [Cucumber Integration in Katalon Studio](https://docs.katalon.com/katalon-studio/docs/cucumber-features-file.html)
* [Sample project](https://github.com/katalon-studio-samples/katalon-bdd-cucumber-tests)
