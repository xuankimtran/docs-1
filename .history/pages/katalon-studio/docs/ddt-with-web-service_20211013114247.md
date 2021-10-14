[Web Service Object Parameterization](https://docs.katalon.com/katalon-studio/docs/parameterize-a-web-service-object.html) in Katalon Studio allows you to perform data-driven testing (DDT) with web service.

This tutorial shows you how to set up a DDT test with web service. The test includes two requests to a web server and data binding with external source:

* A POST request to register user.

* A GET request to verify user identity.

* Data binding with a data sheet.

## Create a web service test

> You can download the sample project here: [Web Service Tests](https://github.com/katalon-studio-samples/web-service-tests).

### Set up a web service project

### Create web request objects 

1. In the **Test Explorer**, right-click on **Object Repository** and select **New > Web Service Request**. 

    [image]

2. In the displayed **New** dialog, name your request object and specify **Request Type**. Here you need to create two RESTful requests. 

    **POST request to register a new user**
   
    With this request, you need to configure the request method, the API endpoint, and the corresponding HTTP Body. 

    The JSON-encoded data includes: username, password, gender, age, and avatar.
    
    [image]

    **GET request to verify user identity**

    The user's id is parameterized in the endpoint.
