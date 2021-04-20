---
title: "Import RESTful requests with OpenAPI Specification 2.0 (Swagger)" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/import-rest-requests-from-swagger-20.html 
redirect_from:
    - "/display/KD/Import+REST+requests+from+Swagger+2.0/"
    - "/display/KD/Import%20REST%20requests%20from%20Swagger%202.0/"
    - "/x/8hXR/"
    - "/katalon-studio/docs/import-rest-requests-from-swagger-20/"
description: 
---
> [Read more about Swagger 2.0...](https://github.com/OAI/OpenAPI-Specification/blob/master/versions/2.0.md)

This topic shows you how to import Web Service objects from a **Swagger 2.0** File or URL, depending on the type of your Katalon Studio project.

**Requirements**

* Katalon Studio version 7.0+.
* An active Katalon Studio Enterprise license.

To conduct, do as follow:

1. Open or create a project > import the service definition in two ways:

* With an API or Web Service project type, click on the OpenAPI icon > select **Import OpenAPI 2 (Swagger)**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/import-rest-requests-from-swagger-20/import.png" width=56%>

* Or in the **Tests Explorer**, right-click on **Object Repository** > select **Import > From OpenAPI 2 (Swagger)**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/import-rest-requests-from-swagger-20/import-via-object.png" width=70%>

2. In the displayed dialog, browse your **Swagger** local file or enter an OpenAPI 2 (Swagger) URL > click **OK**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/import-rest-requests-from-swagger-20/browse.png" width=70%>

    Katalon Studio loads the file and generates RESTful test requests accordingly.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/import-rest-requests-from-swagger-20/result.png" width=70%>

> **Known Issues**:
> 
> *   No Raw text content in HTTP Body parsed from Swagger.
> *   No Authorization parsed from Swagger.
> *   Variables and Parameters should be adjusted manually.

**See also:**

* [Use test requests in a test case](https://docs.katalon.com/katalon-studio/docs/using-web-services-in-a-test-case.html)
* [Parameterize a Web Service Object](/display/KD/Parameterize+a+Web+Service+Object)
* [Verification Snippets](/display/KD/Verification+Snippets)
* [Import REST API with OpenAPI Specification 3.0](https://docs.katalon.com/katalon-studio/docs/import-openapi30.html)