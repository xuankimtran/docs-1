---
title: "REST Request"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/restful.html
redirect_from:
    - "/display/KD/RESTful/"
    - "/x/CQLR/"
    - "/katalon-studio/docs/restful/"

description:
---

Katalon Studio supports sending RESTful requests with parameters, body data and authorization details needed. When sending a Request, you can receive a response from the API server for examination adn troubleshooting. This section gives you detailed information of how to create and configure a RESTful request.

## Creating a RESTful request object

You can create a new RESTful request object in two ways. First, you can **add** a Web Service request to a _New_ or any _Existing_ test case directly in the object details view by a click on the **plus** icon.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/soap-request/Screen-Shot-2018-09-20-at-5.06.42-PM.png)

Or select **File > New > Web Service Request** from the main menu.

In the **New Web Service Request** dialog, specify a name for your request; select **RESTful** in the Request Type's drop-down list; and set request URLs. Then click OK to create a request.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/restful-web-services/image2018-4-1-183A113A47.png)

## Specifying request details

After you've created a request successfully, double-click on the request to open its editor for adding details.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/restful-web-services/Screen-Shot-2018-09-20-at-4.44.23-PM.png)

### Request Method

The request method indicates the expected action to be executed on the specified resource. For REST services, Katalon Studio supports the following methods: GET, POST, PUT, DELETE, PATCH, HEAD, CONNECT, OPTIONS, and TRACE. You can refer to [this document](https://restfulapi.net/http-methods/) for more details and specifications of each method.

For Katalon Studio Enterprise users, you can use custom methods added in  **Project Settings > Test Design > API/Web Service Method**. 

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-510/custAPI.png)

In Tests Explorer, there is a small **icon** next to the object that indicates its used method. By default, GET method is selected for new requests.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/restful-web-services/image2018-4-1-183A353A21.png)

### Request URL

You need to specify a URL indicating the service endpoint of each request. For example, the following URL `https://petstore.swagger.io/v2/pet/findByStatus?status=${status}` is registered for the RESTful request we've created. In URLs, you can use variables, `status=${status}` for instance, to update the Query Parameter dynamically. [More details](https://docs.katalon.com/katalon-studio/docs/parameterize-a-web-service-object.html).

### Parameters

This table displays any parameter to be passed along with the RESTful request object. These values are generated automatically based on the Request URL or can be manually added. [More details](https://docs.katalon.com/katalon-studio/docs/parameterize-a-web-service-object.html).

Starting from **version 7.0**, Katalon Studio encodes special characters in query parameters before sending requests.

### Request Body

You can add the body information needed to be sent along with a RESTful request object. Katalon Studio supports the following body data types: text, x-www-form-urlencoded, form-data, and file.

* **text**: With this type, the supported formats include Text, JSON, XML, HTML, and Javascript.
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/restful-web-services/image2018-9-5-143A263A6.png">

* **form-data**: This data type allows you to send data to APIs as multipart/form-data and attach files as well. From **version 7.5.0+**, you can specify the content type in form-data body.
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/restful-web-services/form-data.png">

### Request Authentication

This part is used for authenticating and authorizing the request, which means to verify if the client is permitted to send the request and to perform the endpoint operation.

For more details on using each type of auth, please see:

* [Basic](https://docs.katalon.com/katalon-studio/docs/authorization-basic.html)
* [OAuth 1.0](https://docs.katalon.com/katalon-studio/docs/authorization-oauth1.html)
* [OAuth 2.0](https://docs.katalon.com/katalon-studio/docs/authorization-oauth2.html)

### Request Headers

You can configure the header information needed for sending the RESTful request object. By default, the **Content-Type** value of **Header** is generated automatically based on the HTTP Body. You can also select headers from the list of suggested options (by double-clicking on the **Name** cell) or enter another header of your interest. Refer to [Supported HTTP Headers](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers) for more details.

Starting from version **7.2.5**, Katalon Studio supports disabling specifying the content type of HTTP Header based on HTTP Body automatically. This allows users to configure content types for HTTP Header and Body separately.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/restful/auto-update.png" width="" height="">

## Response

After you send a request, Katalon Studio supports reading its reponse in a separate **Response** view. A service reponse comprises Status, Eslapsed time, and Size fields; Body section, Header and Verification Log.

* **Status**: The status code of the response
* **Elapsed**: The total time that starts from the request is sent until Katalon Studio receives the last byte of the response
* **Size**: Size of the response package.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/restful-web-services/image2018-9-5-143A253A46.png)

### Response Body

Katalon can read a service response in JSON, XML, HTML, and JavaScript. The response body can be displayed in three formats: pretty, raw, and preview.

* **pretty**: Response is displayed in a pretty format which is easier to read
<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/restful-web-services/Screen-Shot-2018-04-10-at-17.23.21.png">

* **raw**: Response is displayed in the raw text without any format
<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/restful-web-services/image2018-9-5-143A253A6.png">

* **preview**: Response is displayed as visualized (e.g., If a Response is from loading a specific webpage, it is displayed as the screenshot below)
<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/restful-web-services/image2018-4-1-19_10_26.png">

### Response Header

The response's header is displayed in the **Header** tab:
![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/restful-web-services/image2018-9-5-143A243A48.png)

### Verification Log

This tab displays the verification results after the request is tested and verified. Refer to this document for [how to verify API responses in Katalon Studio](https://docs.katalon.com/katalon-studio/docs/verify-api-responses.html#verifying-rest-response-in-json-format).

**See also:**

* [Parameterize a Web Service Object](/display/KD/Parameterize+a+Web+Service+Object)
* [Verification Snippets](/display/KD/Verification+Snippets)
* [Using Web Services in a Test Case](/display/KD/Using+Web+Services+in+a+Test+Case)
