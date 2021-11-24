---
title: "Introduction to Runtime Engine"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/intro-RE.html
description:
---
**Katalon Runtime Engine (KRE)** is the test execution add-on of Katalon Studio. KRE allows you to execute automation tests in CLI mode. It can be used in a variety of scenarios, such as scheduling your tests, integrating with CI/CD system, or bundling your tests to execute in virtual containers like Docker.

## Use Cases

KRE is only required for executing automation tests in CLI (command-line interface) mode. Here are the common scenarios for using KRE:

* Scheduling your tests using Operating System services. [Learn more](https://docs.katalon.com/katalon-studio/docs/schedule-tests-to-execute.html).
* Creating batch operations for control multiple executions.
  * For example, setting up to autorun test suite B after running test suite A.
* Integrating your tests to your CI/CD system.
  * For example, setting up your tests to be trigger by Jenkins once the application under test (AUT) is updated.
* Execute your tests with distributed servers.
  * For example, setting up your tests to run with different Operating System, Browsers or Devices at the same time.
* Bundle your test execution into virtual containers.
  * For example, building a Docker image to execute your test with a specific environment.
* KRE is compatible with both Katalon Studio and Katalon Studio Enterprise.

> Katalon Runtime Engine is a paid product. You can enjoy KRE for free with a 30-day trial. To learn more about Katalon Runtime Engine licenses, see [Katalon Runtime Engine license](https://docs.katalon.com/katalon-studio/docs/license.html#katalon-runtime-engine).