---
title: "Import SOAP requests from WSDLs" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/import-soap-requests-from-wsdl.html 
redirect_from:
    - "/display/KD/Import+SOAP+requests+from+WSDL/"
    - "/display/KD/Import%20SOAP%20requests%20from%20WSDL/"
    - "/x/BhbR/"
    - "/katalon-studio/docs/import-soap-requests-from-wsdl/"
description: 
---

[WSDL](https://www.w3.org/TR/wsdl/) is used for specifying a SOAP web service's functionality. It's critical to SOAP Web Service testing when you can create web service requests based on a WSDL file. This section shows you how to import a WSDL file into a Katalon project and help you explore a WSDL.

From **version 7.5.0+**, Katalon Studio improves the WSDL importing feature with more intuitive UI and newly supported utility. Particularly, you are able to add the desired endpoint to your SOAP request, which takes precedence over the imported endpoint.

## Importing WSDLs into Katalon Studio

To import a WSDL file to your project, please do as follows:

1. In **Tests Explorer**, right-click on any folder of **Object Repository**
2. Select **Import > From WSDL**
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/import-soap-requests-from-wsdl/import-wsdl-rightclick.png" width=512 >

3. In the **URL** field of the **Import WSDL** dialog, specify either a remote WSDL URL or a path of a local WSDL file (e.g., [http://www.dneonline.com/calculator.asmx?WSDL](http://www.dneonline.com/calculator.asmx?WSDL)).
4. Click **OK**. Katalon Studio loads the file and generates SOAP request objects.

If you have created an **API/Web Service** project, click on the **Import WSDL** icon on the main toolbar to display the **Import WSDL** dialog in step 3.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/import-soap-requests-from-wsdl/import-wsdl-icon.png" width=412 >

## Working with the imported WSDLs

A WSDL may contain multiple services. For each service, Katalon Studio creates a SOAP request with a specific Service Function and parses its content from the specified WSDL into their corresponding fields in the request object such as Service Endpoint, SOAPAction and Request message. For example, Katalon Studio creates multiple request objects with [http://www.dneonline.com/calculator.asmx?WSDL]([http://www.dneonline.com/calculator.asmx?WSDL]).

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/import-soap-requests-from-wsdl/parsed-objects.png">

From version 7.5.0, you can always manually change the content of those fields. When you override any fields of the imported request object with new values, you need to **save** your modifications for it to take effect.

* **Service Endpoint**: this tab stores the service endpoint parsed from the WSDL file. You can also specify another endpoint for the interface as your wish. This request object receives any value given in this field.
* **SOAPAction**: the SOAPAction is parsed in the HTTP Header of the request if the request method is SOAP.

## Troubleshooting

After sending the SOAP request, you may encounter the "System.Web.Services.Protocols.SoapException: Server did not recognize the value of HTTP Header SOAPAction.." exception (1) in the response.

One of the possible causes is because you have enabled **Use the endpoint and SOAPAction header parsed from WSDL** (2) and specified the SOAPAction in the request header (3) simultaneously.

*(1),(2),(3): please see the image below for more information.*

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/import-soap-requests-from-wsdl/exception.png">

**Proposed solution**

Remove the SOAPAction header from the HTTP Header if you decide to use the endpoint and SOAPAction header parsed from WSDL.

See also:

* [SOAP Request](https://docs.katalon.com/katalon-studio/docs/soap.html)