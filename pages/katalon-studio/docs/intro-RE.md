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
* KRE is compatible with both Katalon Studio 7 and Enterprise versions.

## License

### Node-Locked License

This license model is applied to local desktops or workstations with fixed hardware specifications (machine-blocked license):

* Virtual machine with fixed machine ID
* Physical machine

The number of licenses to acquire should be based on the number of processes and the maximum parallel sessions that you plan to execute.

* A license is linked to a single machine ID and for one execution session.
* A machine can be mapped to multiple licenses (if needed).
* The license can be transferred to a new machine for an online environment. For the offline environment, once converted, the license cannot be transferred to another machine until it is expired.

### Floating License

This license model is applied to cloud or virtual machines with dynamic hardware specifications (to execute tests in Docker, Azure, AWS). This kind of license provides Enterprise users license mobility when there is no machine quota.

Floating licenses are managed by Cloud Server on a per-session basis. You must have an active network connection to install and access floating licenses.

> Note: If you have no network connection to release a floating license, another user with a connection can release the floating license for you.

Please refer to [this document](https://docs.katalon.com/katalon-studio/docs/install-RE.html) for more details about downloading, activating and installing RE.
