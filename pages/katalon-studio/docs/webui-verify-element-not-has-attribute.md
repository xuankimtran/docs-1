---
title: "[WebUI] Verify Element Not Has Attribute" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/webui-verify-element-not-has-attribute.html 
redirect_from:
    - "/display/KD/%5BWebUI%5D+Verify+Element+Not+Has+Attribute/"
    - "/display/KD/%5BWebUI%5D%20Verify%20Element%20Not%20Has%20Attribute/"
    - "/x/DooY/"
    - "/katalon-studio/docs/webui-verify-element-not-has-attribute/"
description: 
---
Description
-----------

Verify if the web element doesn't have an attribute with the specified name.

Parameters
----------

| Param | Param Type | Mandatory | Description |
| --- | --- | --- | --- |
| to | TestObject | Required | Represent a web element. |
| attributeName | String | Required | The name of the attribute to verify. |
| timeout | int | Required | System will wait at most timeout (seconds) to return result |
| flowControl | FailureHandling | Optional | Specify [failure handling](/x/qAAM) schema to determine whether the execution should be allowed to continue or sto |

Returns
-------

<table><thead><tr><th>Param Type</th><th>Description</th></tr></thead><tbody><tr><td>boolean</td><td><ul><li><strong>true:</strong> the element doesn't the attribute with the specified name.</li><li><strong>false: </strong>the element has the attribute with the specified name</li></ul></td></tr></tbody></table>

Example
-------

You want to verify 'Make Appointment'  button doesn't have attribute 'href' .

```groovy
import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject
import com.kms.katalon.core.webui.keyword.WebUiBuiltInKeywords as WebUI
import internal.GlobalVariable as GlobalVariable

'Open browser and navigate to demo AUT site.'
WebUI.openBrowser(GlobalVariable.G_SiteURL)

'Verify \'Make Appointment\' button doesn\'t have attribute \'href\''
WebUI.verifyElementNotHasAttribute(findTestObject('Page_CuraHomepage/btn_MakeAppointment'),'href', 20)

'Close browser'
WebUI.closeBrowser()
```
