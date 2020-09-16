---
title: "Get Started with Katalium Framework in other IDEs" 
sidebar: katalon_studio_docs_sidebar
permalink: katalium-framework/docs/katalium-framework-get-started-other-ides.html 
description:
---

## Prerequisites

* Java Development Kit 8.

## Start Katalium Server

Please refer to [this guide](https://docs.katalon.com/katalium-server/docs/katalium-user-guide.html) to learn how to start Katalium Server.

## Run your first test in IDE

Refer to this guide to learn how to [create a test case](https://docs.katalon.com/katalium-framework/docs/katalium-framework-create-test-case.html) or [test suite](https://docs.katalon.com/katalium-framework/docs/katalium-framework-create-test-suite.html).

Example of a test case run in IntelliJ IDEA:

![](https://github.com/katalon-studio/docs-images/raw/master/katalium-framework/docs/katalium-framework-get-started-other-ides/run-test-ide.png)

## Run your first test in CLI

To run the default test suite configured in `pom.xml` use `mvn clean test`. Test suites can also be specified using command arguments, e.g. `mvn clean test -Dsurefire.suiteXmlFiles=src/test/resources/testng-parallel.xml`.
