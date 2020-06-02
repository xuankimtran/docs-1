---
title: "Parameterize a Web Service Object" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/parameterize-a-web-service-object.html 
redirect_from:
    - "/display/KD/Parameterize+a+Web+Service+Object/"
    - "/display/KD/Parameterize%20a%20Web%20Service%20Object/"
    - "/x/egLR/"
    - "/katalon-studio/docs/parameterize-a-web-service-object/"
    - "/display/KD/Parameterize+a+Web+Service+object/"
    - "/display/KD/Parameterize%20a%20Web%20Service%20object/"
description: 
---

## Query Parameters

> Only available for **RESTful** Web Service requests

Query parameters can be added to a REST request's URL to tailor and filter the response output. When you input a URL, Katalon Studio detects the query parameters (after the question mark `?`) and list them in the table for better management.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/updated-parameterize-a-web-service-object/Screen-Shot-2018-09-18-at-5.04.18-PM.png)

## Variables and Parameterizing Request Objects

> Available for both **RESTful** and **SOAP** Web Service requests

Katalon Studio provides the **Variables** section with both manual and scripting editors. By using variables in a request object, you can hanlde dynamic values of an object's properties and have more control over them. You can add a new variable and declare its properties in the **Variables** tab. In order to call a variable in a Web Service object, use the **${variable_name}** syntax as a place holder in any of the supported locations. The values of the pre-defined variables are passed to their place holders respectively during runtime. This whole utility is called parameterization and the approach is the same as [parameterizing a WebUI object](https://docs.katalon.com/katalon-studio/docs/manage-web-test-object.html#parameterize-web-test-objects).

In the manual view of a test case, when you add a request object, the pre-defined variables are added **automatically**; hence, you don't need to define them again.

### For RESTful request

Katalon Studio supports calling the declared variables in the following places of a RESTful Web Service object.

* URL
* Query Parameters
* HTTP Header
* HTTP Body
* Verification

The screenshot below illustrates an example of using the '**status**' variable in a URL.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/updated-parameterize-a-web-service-object/Screen-Shot-2018-09-18-at-5.10.01-PM.png)

### For SOAP-based request

The following locations are where you can use the pre-defined variables:

* WSDL URL
* Service Endpoint (available from version 7.5.5)
* HTTP Header
* Request Message
* Verification

Below is an example of parameterizing the domain URL in a SOAP request's service endpoint.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/parameterize-a-web-service-object/soap-endpoint.png">