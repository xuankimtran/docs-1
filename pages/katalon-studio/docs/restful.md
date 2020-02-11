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
> You can **add** a Web Service request to a _New_ or any _Existing_ test case directly in the object details view by a click on the **plus** icon.
>
>  ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/soap-request/Screen-Shot-2018-09-20-at-5.06.42-PM.png)

1. Select **File > New > Web Service Request** from the main menu. The **New Web Service Request** dialog is displayed where you can input your RESTful URL directly on this dialog.
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/restful-web-services/image2018-4-1-183A113A47.png)

2. After you've created a request successfully, there is a small **icon** next to the object on Tests Explorer to indicate its used method.
   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/restful-web-services/image2018-4-1-183A353A21.png)

3. In the editor of the new request, there are two separate sections, including **Request** and **Response**.

Please take a look at the **Request** section using the sample REST URL.

```groovy
https://petstore.swagger.io/v2/pet/findByStatus?status=${status}
```

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/restful-web-services/Screen-Shot-2018-09-20-at-4.44.23-PM.png)

* **Request method**: The request method indicates the expected action to be executed on the specified resource. Katalon Studio supports following methods for REST services: **GET, POST, PUT, DELETE, PATCH (Available from version 5.8)**. You can refer to more details and specifications of each method [here](https://restfulapi.net/http-methods/).
* **Request URL**: The URL registered for the RESTful web services
* **Parameters**: Any parameter to be passed along with the RESTful request object. These values are generated automatically based on the Request URL or can be manually added. Starting from version 7.0, Katalon Studio encodes special characters in query parameters before sending requests.
* **Authorization**: Credentials for HTTP authentication.\
   Type: **Basic**, **OAuth 1.0**, or **No Authorization**
* **HTTP Headers**: The header information to be included to transmit in the RESTful request object. By default, the **Content-Type** value is generated automatically based on the HTTP Body. You can also select headers from the list of suggested options (by double-clicking on the **Name** cell) or enter another header of your interest. Refer to [Supported HTTP Headers](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers) for more details.

   Starting from version 7.2.5, Katalon Studio supports disabling specifying content type of HTTP Header based on HTTP Body automatically. This allows users to configure content types for HTTP Header and Body separately.
   
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/restful/auto-update.png" width="" height="">

* **HTTP Body**: The body information to be included to transmit in the RESTful request object. Katalon Studio supports the following transmit types:

   * Text
   * x-www-form-urlencoded
   * form-data
   * file
   
   And the following format types:
   * Text
   * JSON
   * XML
   * HTML
   * Javascript

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/restful-web-services/image2018-9-5-143A263A6.png">

## RESTful Response

Since version 5.4, Katalon Studio provides Web Services Response in a separate window pane, which contains more details information of the Request as shown below.

### Body

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/restful-web-services/image2018-9-5-143A253A46.png)

There are 3 new information provided in the response's section:

* **Status**: The status code of the response
* **Elapsed**: The total time that starts from the request is sent until Katalon Studio receives the last byte of the response
* **Size**: Size of the response package

The **Response** can be displayed in **multiple ways**:

* **pretty**: Response is displayed in a pretty format which is easier to read
<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/restful-web-services/Screen-Shot-2018-04-10-at-17.23.21.png">

* **raw**: Response is displayed in the raw text without any format
<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/restful-web-services/image2018-9-5-143A253A6.png">

* **preview**: Response is displayed as visualized (e.g. If a Response is from loading a specific webpage, it is displayed as the screenshot below)
<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/restful-web-services/image2018-4-1-19_10_26.png">

At the bottom of the **Body** section, different types of Response format can be selected as desired:

* JSON
* XML
* HTML
* JavaScript

### Header

The response's header information is displayed in the **Header** tab

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/restful-web-services/image2018-9-5-143A243A48.png)

**See also:**

* [Parameterize a Web Service Object](/display/KD/Parameterize+a+Web+Service+Object)
* [Verification Snippets](/display/KD/Verification+Snippets)
* [Using Web Services in a Test Case](/display/KD/Using+Web+Services+in+a+Test+Case)