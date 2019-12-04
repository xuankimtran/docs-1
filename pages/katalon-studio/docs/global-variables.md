---
title: "Global Variables"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/global-variables.html
redirect_from:
  - "/katalon-studio/docs/global-variables/"
description:
---
> Starting from **Katalon Studio [version 6.3.0](https://docs.katalon.com/katalon-studio/new/version-630.html)**, Move up and Move down functions for Global Variables are available.

## Define a Global Variable

A Global Variable in Katalon Studio is a variable which is used globally in the project. For example, if you are going to 

define a variable as a Global Variable, you can use it in any test case in the project.

Global Variables can be managed in the **Default Profile** view.

> Starting from Katalon Studio version 5.4, the Global Variable view is no longer available.

Expand the **default profile** view, then click **Add**.

The **New Variable** dialog box is displayed. Specify details for the variable then click **OK**.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/variable-types/image2017-1-24-153A413A17.png)

The variable will be added to the **default profile** accordingly.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/variable-types/default-profile.png" width="784" height="395">

## Use a Global Variable

Global Variables can be utilized by any test case across a project. (e.g. input data for keywords in [Manual View](/display/KD/Manual+View) or params when [binding Data for Test Execution](/display/KD/Design+a+Test+Suite#DesignaTestSuite-VariableBinding)).

```groovy
import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject

import com.kms.katalon.core.webui.keyword.WebUiBuiltInKeywords as WebUI

import internal.GlobalVariable as GlobalVariable

WebUI.comment('Story: Login to CURA system')

WebUI.comment('Given that the user has the valid login information')

WebUI.openBrowser(GlobalVariable.G_SiteURL)

WebUI.click(findTestObject('Page_CuraHomepage/btn_MakeAppointment'))

WebUI.setText(findTestObject('Page_Login/txt_UserName'), Username)

WebUI.setText(findTestObject('Page_Login/txt_Password'), Password)

WebUI.comment('When he logins to CURA system')

WebUI.click(findTestObject('Page_Login/btn_Login'))

WebUI.comment('Then he should be able to login successfully')

landingPage = WebUI.verifyElementPresent(findTestObject('Page_CuraAppointment/div_Appointment'), GlobalVariable.G_Timeout)

WebUI.closeBrowser()
```

## Parameterize a Global Variable

Starting with **Katalon Studio version 6.3.0**, you can directly parameterize Global Variables in both WebUI and API Test Objects.

Enter the syntax `${GlobalVariable.name}` in any supported locations. For example: 

in HTTP Body of an API Test Object:

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/variable-types/1-GlobalVariable.png)

in Selected Locator of a WebUI Test Object:

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/variable-types/2-GlobalVariable.png)

### Escaping, special characters

To use a special character like `$` or `\` as a regular one in any place that calls parameterized global variables, prepend it with a backslash: `\` (the so-called escape character).

```groovy
{
 	"productName": ${GlobalVariable.productName},
  	"unit": "\\bottle\",
  	"quantity": 50,
  	"discount": ${ if (productName == "wine") { return 30 } else { return 0}}
	"note": "Currency unit of ${GlobalVariable.productName} is \$."

}
```

* Without `\`: *note: Currency unit of ${GlobalVariable.productName} is $*.

* With `\`: *note: Currency unit of wine is $*.
