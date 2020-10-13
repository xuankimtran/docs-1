---
title: "Import RESTful requests from WADLs" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/import-wadl.html 
---

From **version 7.7+**, Katalon Studio supports importing [WADL](https://www.w3.org/Submission/2009/03/) files to create RESTful requests. This manual shows you how to import a WADL file into a Katalon project. You can use an example WADL Description provided [here](https://www.w3.org/Submission/wadl/#x3-40001.3).

1. Open or create a project then import the service definition in two ways:

* With a API/Web Service project type, click on the **Import WADL** icon; or

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/import-wadl/icon.png" width=302>

* In **Tests Explorer**, right-click on any folder of **Object Repository** and select **Import > From WADL**

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/import-wadl/rightclick.png" width=589>

2. In the displayed dialog, browse your **WADL** local file and click **OK**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/import-wadl/browse.png" width=399>

   Katalon Studio loads the file and generates RESTful request objects accordingly.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/import-wadl/imported.png" width=345>

**See also:**

* [Use test requests in a test case](https://docs.katalon.com/katalon-studio/docs/using-web-services-in-a-test-case.html)
* [Parameterize a Web Service Object](/display/KD/Parameterize+a+Web+Service+Object)
* [Verification Snippets](/display/KD/Verification+Snippets)
