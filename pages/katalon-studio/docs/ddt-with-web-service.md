---
title: "Data-driven testing with web service" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/ddt-with-web-service.html 
redirect_from:
description: 
---

[Web Service Object Parameterization](https://docs.katalon.com/katalon-studio/docs/parameterize-a-web-service-object.html) in Katalon Studio allows you to perform data-driven testing (DDT) with web service.

This tutorial shows you how to apply DDT to web service test. The test includes:

* Requests to web service for user registration and verification.

* Data binding with an external data source.

> You can download the sample project here: [Web Service Tests](https://github.com/katalon-studio-samples/web-service-tests).

## Create a web service test

### Create web service request objects

1. In **Tests Explorer**, right-click on **Object Repository** and select **New > Web Service Request**. 

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-with-web-service/New-Web-Request-Object.png" width=70% alt="New web request object">

2. In the displayed **New** dialog, name your request object and specify the **Request Type**. Here you need to create two RESTful requests. 

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-with-web-service/POST-request-object-dialog.png" width=70% alt="New request object dialog">

    **POST request to register a new user**

    You need to specify the request method, the API endpoint, and the corresponding HTTP Body. 

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-with-web-service/POST-request-config.png" width=70% alt="POST request config">

    The JSON-encoded HTTP Body includes these parameterized values: username, password, gender, age, and avatar.

    **GET request to get user by ID**

    With this request's endpoint, the user ID is parameterized in the URL.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-with-web-service/GET-request-config.png" width=70% alt="GET request config">

### Create a test case with request objects

To demonstrate web service test design, here we create a test case using the POST request object and specify its variables.

**User registration test case**

1. Open the test case in **Manual** view, click **Add  Web Service Keyword** button from command toobar.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-with-web-service/Add-web-service-keyword.png" width=70% alt="Add web service keyword">

2. To send a user registration request to web service, select the **Send Request And Verify** keyword.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-with-web-service/Double-click-on-object-cell.png" width=70% alt="Send request and verify keyword result">

3. Double click on object cell and select a test object (POST request object in this case) with the required variables.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-with-web-service/Test-object-input.png" width=70% alt="Test Object input dialog">

4. Run the test case and verify the result in **Log Viewer**:

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-with-web-service/Run-test-case-and-view-result.png" width=70% alt="Test case result">

## Apply data-driven testing with parameterized test requests

To combine user registration and verfication into one test case, you can define custom keywords from the two request objects. 

### Define custom keywords with web service requests

1. In **Tests Explorer**, right-click on the default package and select **New > Keyword** to create a new custom keyword class.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-with-web-service/KS-create-new-keyword.png" width=70% alt="Create new keyword">

2. Enter the following code snippet to define custom keywords and associate them with the two requests: 

```groovy
import groovy.json.JsonSlurper

import java.math.BigDecimal
public class Common {

	public static JsonSlurper jsonSlurper = new JsonSlurper()

	@Keyword
	def int createNewUser(BigDecimal age, String username, String password, String gender, int expectedStatus) {
		def response = WS.sendRequestAndVerify(findTestObject("Object Repository/POST a new user",
				["age": age, "username": username, "password": password, "gender": gender]))

		def jsonResponse = jsonSlurper.parseText(response.getResponseText())
		return jsonResponse.id
	}

	@Keyword
	def static void findUserById(int id, BigDecimal age, String username, String password, String gender, int expectedStatus) {
		def response = WS.sendRequestAndVerify(findTestObject('Object Repository/GET user by id', [('id') : id]))
		WS.verifyElementPropertyValue(response, "age", (age.intValue()).toString())
		WS.verifyElementPropertyValue(response, "username", username)
		WS.verifyElementPropertyValue(response, "password", password)
		WS.verifyElementPropertyValue(response, "gender", gender)
	}
}
```

### Create a test case with custom keywords

1. Open the new test case in **Manual** view. Click the **Add** dropdown button and select **Custom Keyword**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-with-web-service/add-cutom-keyword-web-service.png" width=70% alt="Add a custom keyword">

2. Add the two custom keywords to the test case (```createNewUser``` and ```findUserById```).

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-with-web-service/Select-two-custom-keywords.png" width=70% alt="Select two keywords">

3. Configure each custom keyword with its input and output parameters.

    ***createNewUser***

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-with-web-service/Create-user-input-variables.png" width=70% alt="Input variables">

    ***findUserById***

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-with-web-service/Find-user-by-id-input-variables.png" width=70% alt="Input variables">

    The ***CreateNewUser*** keyword requires an ouput parameter called **id**.

    [image]

### Bind external data to a test suite

1. In a new Test Suite, click on the **Add** button from the command toolbar to add the test case.

