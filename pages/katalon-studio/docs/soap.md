---
title: "SOAP Request"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/soap.html
redirect_from:
    - "/display/KD/SOAP/"
    - "/x/LwLR/"
    - "/katalon-studio/docs/soap/"
    - "/x/0hNO/"
    - "/katalon-studio/docs/soap-pre-54/"
    - "/katalon-studio/docs/soap-pre-54.html"
description:
---
When sending a SOAP Request in Katalon Studio, you can receive a response from the API server for examination and troubleshooting. This section includes a tutorial of how to create a SOAP request object and an introduction to each field of a request service in its opened editor.

## Creating a SOAP-based Request

1. From the main menu, select **File > New > Web Service Request**.
2. In the **New Web Service Request** dialog, select **SOAP** in the **Request Type** list and click **OK** to create a new SOAP object.

   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/soap-request/image2018-9-5-143A213A46.png)

3. A **New** request object is created under the **Object Repository** of Katalon Studio.

## Adding SOAP Request Details

After you've created a request successfully, double-click on the request to open its editor for adding details. In the opened editor of the **New Request** object, you can see all the required information of a request object.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/soap-request/details.png">

### Request Method

The request method indicates the expected action to be executed on the specified resource. Katalon Studio supports the following SOAP methods: SOAP, SOAP 1.2, POST, GET. By default, Katalon selects SOAP as a method for a new SOAP request.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/soap-request/method.png">

### WSDL URL

This field is for a WSDL path from which Katalon Studio imports the content to this SOAP request.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/soap-request/wsdl-url.png">

### Service Function

The function that you want to use in this SOAP request. When clicking **Load Service Function**, you can retrieve a list of service functions available from the WSDL file.
Each Service Function carries its own content, including Service Endpoint, SOAPAction Header and Request message.

* **Service Endpoint**: You can specify another URL indicating the desired service endpoint of this request.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/soap-request/service-endpoint.png">

### Request Authentication

This part is used for authenticating and authorizing the request, which means to verify if the client is permitted to send the request and to perform the endpoint operation.

For more details on using each type of auth, please see:

* [Basic](https://docs.katalon.com/katalon-studio/docs/authorization-basic.html)
* [OAuth 1.0](https://docs.katalon.com/katalon-studio/docs/authorization-oauth1.html)
* [OAuth 2.0](https://docs.katalon.com/katalon-studio/docs/authorization-oauth2.html)

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/soap-request/image2018-9-5-143A213A10.png">

### Request Headers

The header information needs sending along with this SOAP request. You can select headers from the list of suggested options (by double-clicking on the **Name** cell) or enter another header of your interest. Refer to [Supported HTTP Headers](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers) for more details.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/soap-request/header.png">

### Request Message

The information that you want to transmit in this SOAP request. You can get it after clicking **Load New Content** of the selected service function.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/soap-request/request-message.png">

## Response

After sending the service request, Katalon Studio retrieves a message from the server and displays it in the **Response** view of the request. A service response comprises Status, Elapsed time, and Size fields; Body section, Header, and Verification Log.

* **Status**: The status code of the response
* **Elapsed**: The total time that starts from the request is sent until Katalon Studio receives the last byte of the response
* **Size**: Size of the response package

### Response Body

There are 2 viewing formats: **pretty** and **raw**. For example, the SOAP's response to `http://www.dneonline.com/calculator.asmx?WSDL` is shown below.

* Pretty format

  <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/soap-request/pretty.png">

* Raw Format

  <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/soap-request/response.png">

### Response Header

The response's header is displayed in the **Header** tab.

### Verification Log

This tab displays the verification results after the request is tested and verified. Refer to this document for [how to verify API responses in Katalon Studio](https://docs.katalon.com/katalon-studio/docs/verify-api-responses.html#verifying-rest-response-in-json-format).

**See also:**

* [Parameterize a Web Service Object](/display/KD/Parameterize+a+Web+Service+Object)
* [Verification Snippets](/display/KD/Verification+Snippets)
* [Using Web Services in a Test Case](/display/KD/Using+Web+Services+in+a+Test+Case)