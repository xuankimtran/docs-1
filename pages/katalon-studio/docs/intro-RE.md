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

#### Working with RE

First, you need to download the RE package from the [Katalon website](https://katalon.com/download), unzip the package and move to the preferred directory to execute automation tests.

Next, you need a valid RE license to use this add-on. RE license is a node-locked license. The number of licenses to acquire should be based on the number of processes and the maximum parallel sessions that you plan to execute.

* A license is linked to a single machine ID and for one execution session.
* A machine can be mapped to multiple licenses (if needed).
* The license can be transferred to a new machine for an online environment. For the offline environment, once converted, the license cannot be transferred to another machine until it is expired.

> Learn more about [RE License](https://docs.katalon.com/katalon-studio/docs/license.html).

To activate RE, there are different activation methods based on the execution environment which can be online or offline. [Learn more](https://docs.katalon.com/katalon-studio/docs/activate-RE.html).

Once ready, navigate to the RE directory and execute the Katalon automation test in command-line mode (CLI) as normal. Learn more about [execution in console mode](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#execute-katalon-in-cmd).
