---
title: "Create your first API test with Katalon Studio"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/create_first_api_test_katalon_studio.html
description: "API testing has become more important. This tutorial will demonstrate how to use Katalon Studio to create your first API test from scratch."
redirect_from:
    - "/katalon-studio/tutorials/create_first_api_test_katalon_studio"
    - "/katalon-studio/tutorials/create_first_api_test_katalon_studio.html"
---

Introduction
------------

**API testing** (or Web service testing in the context of a Web application) has become more important in software testing. The interest in API testing has been increasing over the last five years, according to [Google Trends](https://trends.google.com/trends/explore?date=today%205-y&q=api%20testing). This trend possibly indicates that the demand for applying API testing has become more prevalent. Testing API or web services is no longer performed solely by the original developer. This activity is now a common practice among outsourcing teams who independently verify and validate their products.

This tutorial will demonstrate how to use Katalon Studio to create your first API/Web service test from scratch with good practices.

Installing and setting up Katalon Studio
----------------------------------------

Please refer to the guide for all the basic steps, from downloading to activating the build [Installing and Setting up Katalon Studio](https://www.katalon.com/resources-center/tutorials/web/get-started/install-setup-katalon-studio/).

Creating a new project and setting up API automation test
---------------------------------------------------------

### Step 1: Create a new project

*   Go to **File** \-> **New** \-> **Project** and enter a project name and its location to start a new project.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/creat-first-API-testing/KS-API-Create-a-new-project.png" width="70%" alt="Create new project using Katalon Studio">

*   Once the project is confirmed to be created, we will see a folder structure in the **Tests Explorer** This folder system is responsible to keep all the test resources and is also the place where we start our first API test.

### Step 2: Create the first API test

Before creating our first API test, let's have a look at the format we use to set up a testing project.

**Object Repository**

*   Object Repository is a place which stores all the Web service endpoints along with all information of Request method, URL, Header, Content, and Authentication.
*   Web service test objects in Object Repository are integrated by a folder system for better management.

**Test Cases**

*   Test Cases stores all test scenarios and is grouped by a folder system. Each test case includes a few steps illustrating a test scenario.
*   We can execute a test case individually with a specified execution profile.

**Test Suites**

*   Test Suites is the place where all test suites are stored. A test suite is a collection of test cases verifying a specific target.
*   Test cases at the test suite level can be executed with a data-driven approach.
*   Test reports are also generated at the test suite level

**Test Suite Collection**

*   Test Suite Collection is a collection of Test Suites verifying a larger target.
*   Test Suite at Test Suite Collection level has specific Test environments specified.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/creat-first-API-testing/API-Testing-Tutorial-2.png" width="100%" alt="Plan test execution">

### Step 3: Create a new RESTful endpoint at Object Repository

**Object Repository** -> **New** \-> **Web Service Request**

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/creat-first-API-testing/KS-API-Create-a-new-object.png" width="70%" alt="Create new RESTful endpoint at Object Repository">

Katalon Studio stores Web service endpoint for testing at **Object Repository**, which is similar to **Test Object** in UI Test. At the **Create New Web Service Request** dialog, you can either choose to create a RESTful or a SOAP request.

**Request type** is a required field. You need to specify it exactly at this step. In contrast, **URL** is not required. You can set this value later in the next step.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/creat-first-API-testing/KS-API-Name-the-object.png" width="70%" alt="Create new RESTful endpoint at Object Repository">

Click **OK**, then we are ready to input more details to the first RESTful test.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/creat-first-API-testing/KS-API-Functions-in-RESTFUL-object.png" width="100%" alt="Functions in a  RESTful object">

There are some important concepts needed to specify when testing a RESTful request:

**(1) Request method**

We can choose one of these following methods for your first request test: **GET, POST, PUT, DELETE**. The method needs to match with the URL to have a valid request. For instance, let's assume that our first test is a public API from Jira Cloud version. We should use the **GET** method to receive information on an existing ticket using its ID.

**(2) Request URL**

Along with the request method, **request URL** is used to tell the web server which API is utilized under test. Any mismatch between method and URL will lead to invalid request exception at runtime or wrong data response.

**(3) Authorization**

Authorization is an essential part of an API. It is used to get the correct data under permission (unless the data is public). Katalon Studio supports common authentication methods:

The basic method requires username and password. Don't forget to click **Update to HTTP Header** so that the authentication can be applied to **HTTP Header**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/creat-first-API-testing/KS-API-Authorization.png" width="70%" alt="Authorization">

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/creat-first-API-testing/KS-API-HTTP-header.png" width="70%" alt="HTTP header">


**(4) Verification**

Verification is the place where you define the assertion to ensure the response will contain the expected information.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/creat-first-API-testing/KS-API-Verify-the-object.png" width="100%" alt="Verify the RESTful object">

The verification tab of a request is similar to the Script tab of a test case. In other words, you can write custom scripts with built-in keywords or Groovy/Java scripts to verify the response data. Besides built-in keywords, Katalon Studio also supports built-in snippets, which help you to generate assertions with a single click. It is useful for testers who might find it difficult to deal with parsing and to assert with JSON data format.

The right panel of the request is the response displayed in nice format automatically and the result of verification at Verification Log. To include verification script when sending the request, you need to choose the **Test Request and Verify** option from the execution button.

The Verification script helps you have quick feedback of the request status rather than an actual test. You can add more assertions to the test case level in the next step.

**(5) Variables**

Variables make API testing more robust and dynamic with the data-driven approach. In Katalon Studio, every part of the request can be parameterized. In other words, dynamic data can be used for: URL, Authentication, HTTP Header, and HTTP Body to maximize the capability of data-driven testing. Following setup works the same with the above example:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/creat-first-API-testing/KS-API-Variables.png" width="100%" alt="Variables in the RESTful object">


**(6) Formatter**

The response will be automatically displayed in a neat format: JSON, XML, HTML, and JavaScript. It is helpful for a quick view of the response status.

### Step 4: Create a new test case with an existing request

While the request at **Object Repository** is helpful for fast testing, we can add the request verification at the test case level for better managing and reporting.

### Step 5: Add an existing request to a test case

A request can be inserted into a test case with Web service built-in keywords. There are many keywords can be used to send the request, to verify the response, and to make the request as part of a bigger testing flow.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/creat-first-API-testing/KS-API-Add-webservice-keywords.png" width="70%" alt="Web service keywords">

Following test case illustrates how we can call the request with verification steps from a test case:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/creat-first-API-testing/KS-API-Input-object-in-a-test-case.png" width="100%" alt="Verify the RESTful object in a test case">

The test case can be executed as a normal test case in Katalon Studio. Each verification step can be viewed from the log.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/creat-first-API-testing/KS-API-log-viewer.png" width="100%" alt="Log viewer">

### Step 6: Add the test case to the test suite

A test case can be added to a test suite via either the drag-and-drop feature or the **Add test case** tool. Once the test case is added to the test suite, we can execute the whole test suite with the Run button (without selecting the browser as in UI testing).

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/creat-first-API-testing/KS-API-Add-test-case-to-a-test-suite.png" width="100%" alt="Add test case to a test suite">

### Next steps

Now we finish creating our first test. In order to create tests for a real project with a practical solution, we would need to create more tests with more techniques:

*   Parameterize your tests
*   Apply data-driven approach
*   Create custom keywords/packages
*   Call tests and reuse code
*   Include error handling
*   View test reports after test suite execution

### Create Custom API/Web Service Methods

> This feature is only available for Katalon Studio Enterprise users.

You can create **Custom API/Web Service Methods** to expand RESTful Web Service Testing capabilities by going to **Project > Settings > Test Design > Web Service > Custom Method**. Katalon handles custom API methods on top of the default set of supported methods.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/creat-first-API-testing/KS-API-Create-custom-webservice-method.png" width="100%" alt="Create a custom method">

Conclusion
----------

This complete tutorial helped us go through all the steps and concepts needed for users to create the first API test. In order to achieve the best outcomes and save time and effort, we have to learn how to use API testing properly. For example, we need to have an appropriate implementation of techniques and awareness of whether an API should be tested automatically or manually. Therefore, if we make enough effort and master your Katalon Studio skills, the tool will definitely help us significantly increase the quality of any target product.
