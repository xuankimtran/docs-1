---
title: "Data-driven testing with web service" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/ddt-with-web-service.html 
redirect_from:
description: 
---

Web Service Object Parameterization in Katalon Studio allows you to perform data-driven testing (DDT) with web services.

This tutorial shows you how to apply DDT to a web service test. The test includes:

* Requests to web service for user registration and verification.

* Data binding with an external data source.

> You can download the sample project here: [Web Service Tests](https://github.com/katalon-studio-samples/web-service-tests).

## Create parameterized web service request objects

1. To create a web service request object, from the main menu, select **File > New > Web Service Request**. 

2. In the displayed **New** dialog, name your request object and specify the request type.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-web-service/KS-New-request-object.png" width=70% alt="New Web Service Request dialog">

    In our example, we need to create two RESTful requests.

    **POST request to register a new user**

    We need to specify the request method, the API endpoint, and the corresponding HTTP Body.

    The JSON-encoded HTTP Body in the POST request includes these parameterized values: `username`, `password`, `gender`, `age`, and `avatar`. This API request receives user information and returns the ID of the newly created user.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-web-service/KS-New-POST-request-object.png" width=70% alt="POST request configuration">

    **GET request to get a user by ID**

    This API request receives a user ID and returns the corresponding user information. The user ID (`id`) is parameterized in the API endpoint. 

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-web-service/KS-New-GET-request-object.png" width=70% alt="GET request configuration">

> To learn more about using parameters with Web Service Requests, refer to this document: [Parameterize a Web Service Object](https://docs.katalon.com/katalon-studio/docs/parameterize-a-web-service-object.html).

## Create a test case with parameterized web service requests

To demonstrate parameterized web service test design, we create a test case to send the POST request to create a new user. With the returned user id from the POST request, we verify user identity using the GET request.

Follow these steps to set up the test case:

1. Open a new test case, in the **Script** view, enter the following code snippet to set up the test case:

    ```groovy

    // Send a POST request to create a new user
    // The response contains the id of the newly created user
    post_response = WS.sendRequestAndVerify(findTestObject('POST a new user', [('username') : username, ('password') : password
                , ('gender') : gender, ('age') : age]))

    // Get the id value from the response
    user_id = WS.getElementPropertyValue(post_response, 'id')
    println("ID of user " + username + ": " + user_id.toString())

    // Send a GET request to retrieve user information by id
    get_response = WS.sendRequestAndVerify(findTestObject('GET user by id', ['id' : user_id]))
    println("The response is: " + get_response.getResponseText())

    // Verify that the returned values match the user information
    WS.verifyElementPropertyValue(get_response, 'username', username)

    ```

2. To run a test case with different inputs, you need to parameterize the test case. Switch to the **Variables** tab of the **Test Case Editor** and specify the parameterized values.

    Here we specify the variables in use (`username`, `password`, `gender`, `age`, and `avatar`), provide the type and the default values.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-web-service/KS-Variables-tab.png" width=70% alt="Test case variables">

3. Run the test case and verify the test message in the **Console** log:

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-web-service/KS-Console-log-test-case-result.png" width=70% alt="Test case run result">

## Apply data-driven testing with web service tests

We apply DDT to the web service test by binding a data file to a test suite.

Follow these steps to set up the test data, the test suite, and data binding:

1. To create a test data file, from the main menu, select **New > File > Test Data**. In the displayed dialog, name the test data file and specify the data type.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-web-service/KS-New-Test-Data-dialog.png" width=70% alt="New Test Data dialog">

    In our example, we use an Excel file that contains user information.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-web-service/KS-Test-Data-User-Information-Table.png" width=70% alt="Test Data table of user information">

    > To learn more about test data management, refer to this guide: [Manage Test Data](https://docs.katalon.com/katalon-studio/docs/manage-test-data.html).


2. Open a new test suite, click on the **Add** button and include the parameterized test case.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-web-service/KS-Test-Suite-add-test-case.png" width=70% alt="Test Data table of user information">

3. To open the **Data Binding** section, click on the **Show Data Binding** button.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-web-service/KS-Test-Suite-Show-Data-Binding.png" width=70% alt="Test Data table of user information">

4. You need to specify the test data file and configure the variable binding. Follow the steps in this guide to configure the binding: [Manage Data Binding](https://docs.katalon.com/katalon-studio/docs/run-test-case-external-data.html#manage-data-binding).

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-web-service/KS-Test-Suite-configure-data-binding.png" width=70% alt="Test Data table of user information">

5. Once configured, run the test suite and verify the result in the **Log Viewer**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-web-service/KS-DDT-Test-Result.png" width=70% alt="Test Data table of user information">

**See also**:

* [Data-driven Testing with Katalon Studio](https://docs.katalon.com/katalon-studio/docs/ddt.html)
