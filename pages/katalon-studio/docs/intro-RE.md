---
title: "Introduction to Runtime Engine"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/intro-RE.html
description:
---
**Runtime Engine (RE)** is the test execution add-on of Katalon Studio. RE allows you to execute automation tests in CLI mode. It can be used in a variety of scenarios, such as scheduling your tests, integrating with CI/CD system, or bundling your tests to execute in virtual containers like Docker.

RE is only required for executing automation tests in CLI (command-line interface) mode. Here are the common scenarios for using RE:

* Scheduling your tests using Operating System services. [Learn more](https://docs.katalon.com/katalon-studio/docs/schedule-tests-to-execute.html).
* Creating batch operations for control multiple executions.
  * For example, setting up to autorun test suite B after running test suite A.
* Integrating your tests to your CI/CD system.
  * For example, setting up your tests to be trigger by Jenkins once the application under test (AUT) is updated.
* Execute your tests with distributed servers.
  * For example, setting up your tests to run with different Operating System, Browsers or Devices at the same time.
* Bundle your test execution into virtual containers.
  * For example, building a Docker image to execute your test with a specific environment.
* RE is compatible with both Katalon Studio 7 and Enterprise versions.

Please refer to [this document](https://docs.katalon.com/katalon-studio/docs/install-RE.html) for more details about downloading, activating and installing RE.
