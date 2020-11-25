---
title: "Global Variables and Execution Profile"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/execution-profile-v54.html
redirect_from:
    - "/x/xAHR/"
    - "/katalon-studio/docs/execution-profile-v54/"
    - "/katalon-studio/docs/global-variables/"
    - "/katalon-studio/docs/global-variables.html"
    - "/display/KD/Create+Global+Variables+on+the+fly/"
    - "/display/KD/Create%20Global%20Variables%20on%20the%20fly/"
    - "/x/EAjR/"
    - "/katalon-studio/docs/create-global-variables-on-the-fly/"
    - "/katalon-studio/docs/create-global-variables-on-the-fly.html"
description:
---

## Execution Profile

**Execution Profile** helps cover multiple and different environments to execute your automation test scripts with ease.

* The **Default Profile** stores Global Variables and you can create new ones here. There is **NO** 'Global Variables' interface.
* By default, Katalon Studio uses a **default profile**, as indicated on the top right of Katalon Studio's interface. There is also a drop-down menu that allows you to select any available execution profile.

Execution Profile interfaces are provided with Manual and Script Views where an XML editor is available for adding variables via script. You can create as many profiles as you want to, depending on the needs of the project. In Script View, Profiles can be easily synced with each other when there is a similar list of Global Variables required for testing different environment types. Just copy and paste the variables list from one Profile to another.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-profile-v54/profile-script-view.png)

Just like any other test artifacts, you can quickly _create_, _rename_, _copy_, _cut_ **Execution Profile** directly from _Tests Explorer_.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-profile-v54/Untitled3.png)

There are many ways to use your profile. In the example below, there are 3 profiles: **local**, **staging**, **production** based on testing environments:

**For test cases/ test suites**: Select your desired profile from the top right. After your profile is changed, **all Global Variables** within your current project **uses** these **values**
![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-profile-v54/Untitled2.png)

**For Test Suite Collection**: Select your desired profile to be executed with your Test Suite on the '**Profile**' column.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-profile-v54/4.png)

**For [Console Mode](/display/KD/Console+Mode+Execution) execution**: Select your desired profile on the Profile field.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-profile-v54/5.png)

The generated command has '**executionProfile**' parameter so that you can change it manually, e.g

```groovy
katalon -noSplash  -runMode=console -consoleLog -projectPath="C:\Users\Admin\Katalon Studio\yourProject.prj" -retry=0 -testSuitePath="Test Suites/TS_RegressionTest" -executionProfile="local" -browserType="Chrome (headless)"

```

## Global Variables

> Starting in Katalon Studio version 6.3.0, Move up and Move down functions for Global Variables are available.

### Define a Global Variable

A Global Variable in Katalon Studio is a variable which is used globally in the project. For example, if you are going to define a variable as a Global Variable, you can use it in any test case in the project. Global Variables can be managed in the **Default Profile** view.

1. Expand the **default profile** view, then click **Add**.
2. In the **New Variable** dialog box, specify details for the variable then click **OK**.

   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/variable-types/image2017-1-24-153A413A17.png)

3. The variable are added to the **default profile** accordingly.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/variable-types/default-profile.png" width="784" height="395">

### Use a Global Variable

Any test case across a project can use global Variables (e.g., input data for keywords in [Manual View](/display/KD/Manual+View) or params when [binding Data for Test Execution](/display/KD/Design+a+Test+Suite#DesignaTestSuite-VariableBinding)).

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

### Parameterize a Global Variable

> Starting in **Katalon Studio version 6.3.0**, you can directly parameterize Global Variables in both WebUI and API Test Objects.

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

### Create Global Variables during runtime

To create Global Variables during runtime using Katalon scripts, there are many approaches as discussed [here](https://forum.katalon.com/discussion/6822/how-to-define-global-variables-within-scripts-ie-on-the-fly). One of the approaches below comes from [Sergii Tyshchenko](https://forum.katalon.com/profile/4921/Sergii%20Tyshchenko):

You can also define environment variable (with path to external configuration or properties file) in the session that is used to execute Katalon studio and then in the TestListener read the value of variable (path to the file), load that file and override settings for project, Global variables etc. To create new GlobalVariable I used metaprogramming:

```groovy
 @Keyword
 void addGlobalVariable(String name, def value) {
  GroovyShell shell1 = new GroovyShell()
  MetaClass mc = shell1.evaluate("internal.GlobalVariable").metaClass
  String getterName = "get" + name.capitalize()
  mc.'static'."$getterName" = { -> return value }
  mc.'static'."$name" = value
}
```

It's possible to add getter/setter as new methods toGlobalVariableclass or add a new field (commented in this example)

Then in the script code, you can use GlobalVariable.VarName

```groovy
CustomKeywords.'helper.addGlobalVariable'('localURL', 'katalon.com')
println GlobalVariable.localURL
```

## Set default profile at project level

You may have multiple profiles for executing your tests, for instance, staging and production profiles with corresponding global variables. It would be convenient if you can set a profile as your default one in every execution of a project. Starting from **version 7.4.2**, you can configure a default profile at project level.

Right-click on your desired execution profile and select **Set as default Execution Profile**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-profile-v54/set-default-profile.png" width="" height="">

This profile becomes a default execution option for Test Case, Test Suite, and Test Suite Collection.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-profile-v54/tsc.png" width="" height="">

It's also applied for the Executive Platform of the Command Generator in case you use Katalon Runtime Engine.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-profile-v54/cli.png" width="" height="">