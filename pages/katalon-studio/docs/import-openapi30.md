---
title: "Import REST API with OpenAPI Specification 3.0" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/import-openapi30.html 
---

This manual shows you how to import RESTful APIs with [OpenAPI Specification version 3.0](https://swagger.io/specification/) to Katalon Studio. For OpenAPI 2.0 (Swagger), please see the following [document](https://docs.katalon.com/katalon-studio/docs/import-rest-requests-from-swagger-20.html).

**Requirements**

* Katalon Studio version 7.7+
* An active Katalon Studio Enterprise license

To import a service definition with OpenAPI 3.0, please do as follows:

1. Open or create a project then import the service definition in two ways:

* With a API/Web Service project type, click on the OpenAPI icon and select the **Import OpenAPI 3** option; or

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/import-openapi30/icon.png" width=351>

* In **Tests Explorer**, right-click on any folder of **Object Repository** and select **Import > From OpenAPI 3**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/import-openapi30/rightclick.png" width=541>

3. In the displayed dialog, browse your **OpenAPI 3.0** local file or enter an OpenAPI 3 URL, and click **OK**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/import-openapi30/browse.png" width=454>

   Katalon Studio loads the file and generates RESTful test requests accordingly.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/import-openapi30/imported.png" width=651>

**See also:**

* [Use test requests in a test case](https://docs.katalon.com/katalon-studio/docs/using-web-services-in-a-test-case.html)
* [Parameterize a Web Service Object](/display/KD/Parameterize+a+Web+Service+Object)
* [Verification Snippets](/display/KD/Verification+Snippets)