---
title: "[WS] Verify Element Text" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/ws-verify-element-text.html 
redirect_from:
    - "/display/KD/%5BWS%5D+Verify+Element+Text/"
    - "/display/KD/%5BWS%5D%20Verify%20Element%20Text/"
    - "/x/kZQY/"
    - "/katalon-studio/docs/ws-verify-element-text/"
description: 
---
## Description


Verify that there is an element with expected text appeared in the returned data from a web service call.

## Parameters 


| Parameter | Parameter Type | Mandatory | Description |
| --- | --- | --- | --- |
| response  | ResponseObject  | Required | Represent an HTTP Response, the user can get responded content type, data, header properties (sometimes the user may want to get cookies from response header) |
| locator  | String  | Required | The element locator that Katalon uses to look for the expected data. To learn more about element locator, you can refer to this document: [Handle Response messages](https://docs.katalon.com/katalon-studio/docs/handle-response-messages.html). |
| text  | String  | Required | The expected text of element you want to verify in the responded data (usually is JSON/XML) |
| flowControl  | FailureHandling  | Optional | Specify failure handling schema to determine whether the execution should be allowed to continue or stop. To learn more about failure handling settings, you can refer to this document: [Failure handling](https://docs.katalon.com/katalon-studio/docs/failure-handling.html#default-failure-handlingbehavior). |
## Returns

*   **true**, if your element text is found, otherwise; **false**.
## Example

Given the following sample **SOAP_TransactionResult** SOAP object: 

``` groovy
<?xml version="1.0" encoding="UTF-8"?>
<env:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:env="http://schemas.xmlsoap.org/soap/envelope/">
  <env:Body>
    <ns:PreAuthorizeResponse xmlns:ns="beep" xmlns:ns2="bop" xmlns:ns1="foo" >
      <ns:Receipt>
        <ns1:DataKey>123</ns1:DataKey>
        <ns1:CustomerId>12345</ns1:CustomerId>
        <ns1:PaymentId>123456</ns1:PaymentId>
        <ns1:TransactionResult>Approved</ns1:TransactionResult>

```

We want to verify the **TransactionResult** object in XML format after sending the request. You can use the `verifyElementText` web service keyword as below:

```groovy
import static com.kms.katalon.core.testcase.TestCaseFactory.findTestCase
import static com.kms.katalon.core.testdata.TestDataFactory.findTestData
import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject
import internal.GlobalVariable as GlobalVariable
import com.kms.katalon.core.testobject.ConditionType as ConditionType
import com.kms.katalon.core.testobject.RequestObject as RequestObject
import com.kms.katalon.core.testobject.TestObjectProperty as TestObjectProperty
import com.kms.katalon.core.webservice.keyword.WSBuiltInKeywords as WebAPI
import com.kms.katalon.core.webui.keyword.WebUiBuiltInKeywords as WebUI
import com.kms.katalon.core.mobile.keyword.MobileBuiltInKeywords as Mobile
import com.kms.katalon.core.webservice.keyword.WSBuiltInKeywords as WS
import static com.kms.katalon.core.checkpoint.CheckpointFactory.findCheckpoint
import com.kms.katalon.core.model.FailureHandling as FailureHandling
import com.kms.katalon.core.testcase.TestCase as TestCase
import com.kms.katalon.core.testdata.TestData as TestData
import com.kms.katalon.core.testobject.TestObject as TestObject
import com.kms.katalon.core.checkpoint.Checkpoint as Checkpoint

'Send a SOAP request and returns its response'
def response = WS.sendRequest(findTestObject('SOAP_TransactionResult'))

'Verify converted weight after sending request is correct or not'
WS.verifyElementText(response, 'PreAuthorizeResponse.Receipt.TransactionResult', 'Approved')
```
> Notices:
> 
> Katalon checks if the XML element content text is strictly equal to the expected value. For example, if the **Approved** value have a whitespace, then you should add a whitespace when using the `verifyElementText` keyword.
> 
> ``` groovy
> WS.verifyElementText(response, 'PreAuthorizeResponse.Receipt.TransactionResult', '''Approved
>        ''')
>  ```