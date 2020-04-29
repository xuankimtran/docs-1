---
title: "SOAP Request"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/soap.html
redirect_from:
    - "/display/KD/SOAP/"
    - "/x/LwLR/"
    - "/katalon-studio/docs/soap/"
description:
---
This section includes a tutorial of how to create a SOAP request object and an introduction to each field of a request service in its opened editor.

## Create a SOAP-based Request Object

1. From the main menu, select **File > New > Web Service Request**.
2. In the **New Web Service Request** dialog, select **SOAP** in the **Request Type** list and click **OK** to create a new SOAP object.

    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/soap-request/image2018-9-5-143A213A46.png)

3. A **New** request object is created under the **Object Repository** of Katalon Studio.

## Design the SOAP Request Object

In the opened editor of the **New** request object, you can see all the required information of a request object.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/soap-request/opened-editor.png">

* **Request Method**: The request method indicates the expected action to be executed on the specified resource. Katalon Studio supports following SOAP methods: SOAP, SOAP 1.2, POST, GET.
* **WSDL URL**: The WSDL service definition registered for the SOAP web service.
* **Service Function**: The function/method of the SOAP web service that you want to use in this SOAP request. The list is retrieved after clicking **Load Service Function**.
* **Service Function's content** includes Service Endpoint, SOAPAction Header and Request message.
* **Service Endpoint**: 
* **Authorization**: Credentials for HTTP authentication
<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/soap-request/image2018-9-5-143A213A10.png">

* **HTTP Headers**: The header information that you want to transmit in this SOAP request object.
You can select headers from the list of suggested options (by double-clicking on the **Name** cell) or enter another header of your interest. Refer to [Supported HTTP Headers](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers) for more details.
<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/soap-request/http-headers.png">

* **Request Message**: The information that you want to transmit in this SOAP request object.You can enter directly or import content from external text files.
<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/soap-request/message.png">

When you have finished updating the request object, you need to save your changes. The defined request object can be used in test cases. Refer to [Use Web Service in Test Case](/display/KD/Using+Web+Services+in+a+Test+Case) for more details.

## Explore the Response View of an Object

When you click on the **Test Request** button, Katalon Studio retrieves a message from a web service server and display it in the Response view of an object. The response include the following details: **Status**, **Elapsed** Time, and **Size**.

* **Body**: There are 2 viewing formats: **pretty** and **raw**.

  Pretty format

  <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/soap-request/pretty.png">

  Raw Format

  <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/soap-request/raw.png">

* **Header**:
* **Verification Log**:

For example, the SOAP request and response of `http://www.dneonline.com/calculator.asmx?WSDL` are shown below.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/soap-request/Screen-Shot-2018-09-21-at-1.13.00-PM.png)

**See also:**

* [Parameterize a Web Service Object](/display/KD/Parameterize+a+Web+Service+Object)
* [Verification Snippets](/display/KD/Verification+Snippets)
* [Using Web Services in a Test Case](/display/KD/Using+Web+Services+in+a+Test+Case)