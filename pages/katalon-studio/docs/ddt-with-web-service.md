---
title: "Data-driven testing with RESTful Web Service requests" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/ddt-with-web-service.html 
redirect_from:
description: 
---

Web Service Object Parameterization in Katalon Studio allows you to perform data-driven testing (DDT) with Web Services.

This tutorial shows you how to apply DDT with RESTful Web Service requests. The tutorial includes:

* Creating RESTful Web Service requests and test cases with variables.

* Data binding the associated request objects and test cases with an external data source.

> You can download the sample project here: [Web Service Tests](https://github.com/katalon-studio-samples/web-service-tests).

In our example, we want to send the user information with dynamic data, including username, password, age, gender, and avatar to the server to create an account, then return a user ID as the response. After creating a new user, we will find that user by the user ID.

## Create Web Service request objects with variables

Here we need to create two RESTful requests with variables:

* A POST request with variables to register a new user.
* A GET request with variables to get a user by ID.

### Create a POST request with variables

We use the POST request to send the user information, including username, password, age, gender, and avatar to the server to create an account, then expect a user ID as the response.

Follow these steps to create and configure the POST request:

1. Create a Web Service request. From the main menu, select **File > New > Web Service Request**. In the displayed **New** dialog, name the request and specify the request type as **RESTful** request.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-web-service/KS-new-web-request-POST.png" width=70% alt="New Web request dialog">

2. Specify the API endpoint. In our example, the API endpoint is `https://sample-web-service-aut.herokuapp.com/api/users/json`.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-web-service/KS-New-POST-API-endpoint.png" width=70% alt="POST request API endpoint">

3. In the **Variables** tab, input `username`, `password`, `gender`, `age`, and `avatar` variables.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-web-service/KS-POST-request-variable-tab.png" width=70% alt="POST Variables tab">

4. To call a variable in a Web Service object, use the `${variable_name}` syntax as a place holder in any of the supported locations.

    Here we use the syntax to specify the variables in the **HTTP Body** tab.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-web-service/KS-POST-request-HTTP-body.png" width=70% alt="HTTP Body tab">

### Create a GET request with variables

Next, we use the GET request to find a user by ID. We expect the server to return the user information, including username, password, gender, age, and avatar in the response.

Follow these steps to configure the GET request:

1. Create a Web Service request. From the main menu, select **File > New > Web Service Request**. In the displayed **New** dialog, name the request and specify the request type as **RESTful** request.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-web-service/KS-new-web-request-GET.png" width=70% alt="New Web request dialog">

2. Specify the API endpoint. For the GET request, the API endpoint is `https://sample-web-service-aut.herokuapp.com/api/users/`.

3. To pass a variable to the GET API, add the `${variable_name}` place holder at the end of the API endpoint.

    Here we specify the `id` variable using the `${id}` syntax as follows:
    `https://sample-web-service-aut.herokuapp.com/api/users/${id}`. 

3. In the **Variables** tab, input the `id` variable.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-web-service/KS-GET-request-object-config.png" width=70% alt="GET request variables tab">

## Create a test case with associated Web Service requests

After creating two RESTful Web Service requests with variables, we create a test case to send the POST request to register a new user and extract the user ID from the response. With the returned user ID, we send the GET request to retrieve user information and verify it.

Follow these steps to set up the test case:

1. Open a new test case, in the **Script** tab, enter the following code snippet to set up the test case:

    ```groovy

    // Send a POST request to create a new user
    // The response contains the id of the newly created user
    post_response = WS.sendRequest(findTestObject('POST a new user', [('username') : username, ('password') : password
                , ('gender') : gender, ('age') : age]))

    // Extract the id value from the response
    user_id = WS.getElementPropertyValue(post_response, 'id')
    println("ID of user " + username + ": " + user_id.toString())

    // Send a GET request to retrieve user information by id
    get_response = WS.sendRequest(findTestObject('GET user by id', ['id' : user_id]))
    println("The response is: " + get_response.getResponseText())

    // Verify that the returned values match the user information
    WS.verifyElementPropertyValue(get_response, 'username', username)
    WS.verifyElementPropertyValue(get_response, 'password', password)

    ```

2. To input variables into the test case, switch to the **Variables** tab and pass the variables defined in the Web Service object to the variables in the test case.

    Here, we specify the `username`, `password`, `gender`, `age`, and `avatar` variables.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-web-service/KS-Variables-tab.png" width=70% alt="Test case variables">

3. Run the test case and verify the test message in the **Console** log:

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-web-service/KS-Console-log-test-case-result.png" width=70% alt="Test case run result">

## Apply data-driven testing with Web Service tests

We apply DDT to the Web Service test by binding a data file to a test suite.

Follow these steps to set up the test data, the test suite, and data binding:

1. To create a test data file, from the main menu, select **New > File > Test Data**. In the displayed dialog, name the test data file and specify the data type.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-web-service/KS-New-Test-Data-dialog.png" width=70% alt="New Test Data dialog">

    In our example, we use an Excel file that contains user information.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-web-service/KS-Test-Data-User-Information-Table.png" width=70% alt="Test Data table of user information">


2. Open a new test suite, click on the **Add** button and include the test case.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-web-service/KS-Test-Suite-add-test-case.png" width=70% alt="Test Data table of user information">

3. To open the **Data Binding** section, click on the **Show Data Binding** button.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-web-service/KS-Test-Suite-Show-Data-Binding.png" width=70% alt="Test Data table of user information">

4. You need to specify the test data file and configure the variable binding. Follow the steps in this guide to configure the binding: [Manage Data Binding](https://docs.katalon.com/katalon-studio/docs/run-test-case-external-data.html#manage-data-binding).

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-web-service/KS-Test-Suite-configure-data-binding.png" width=70% alt="Test Data table of user information">

5. Once configured, run the test suite and verify the result in the **Log Viewer**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-web-service/KS-DDT-Test-Result.png" width=70% alt="Test Data table of user information">

> **Notes**:
>
> For real-time monitoring and better reporting capabilities, consider integrating your project with Katalon TestOps. Learn more about test result reports here: [Upload Test Results to Katalon TestOps from Katalon Studio](https://docs.katalon.com/katalon-studio/docs/katalon-analytics-beta-integration.html).

**See also**:

* [Data-driven Testing with Katalon Studio](https://docs.katalon.com/katalon-studio/docs/ddt.html)
