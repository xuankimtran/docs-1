
[Web Service Object Parameterization](https://docs.katalon.com/katalon-studio/docs/parameterize-a-web-service-object.html) in Katalon Studio allows you to perform data-driven testing (DDT) with web service. 

In this tutorial, you will learn to design and execute a DDT with web service. The test includes:

* A request to create a new user (username, password, age, and gender).

* A request to retrieve the user by ID.

> You can download the sample project here: [Web Service Testing Samples](https://github.com/katalon-studio-samples/web-service-tests)

## Create data-driven test for web service

### Create test request objects

1. Right click on **Object Repository** and select **New > Web Service Request**.

    [image]

2. In the displayed **New** dialog, name your test request and specify the **Request Type**. Here we want to create two Restful requests.

    [image]

3. Configure the request objects: 

    **POST request for user registration**
   
    You need to provide a request method (POST), a URL, and an HTTP Body. For this particular API endpoint, the HTTP body must include these parameters: username, password, gender, age, and avatar.

    [image]

    **GET request to query user by id**

    A GET request method does not require an HTTP body.

    [image]

### Create a test case from a test request object

