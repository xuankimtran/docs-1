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

**Execution Profile** helps cover multiple and different environments to execute your automation test scripts with ease. You can configure the testing environment in terms of data and behaviors through **global variables**. A **global variable** is a variable defined in the execution profile and can be used in any test cases in the project.

### Create a profile

Just like other test artifacts, you can CRUD the **Execution Profile** in the **Tests Explorer**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-profile-v54/Untitled3.png" width=55%>
   
In a profile, you need to define its content via adding variables. Do as follows:

1. Select a profile > click **Add**.
2. In the **New Variable** dialog, specify details for the variable > click **OK**.
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/variable-types/image2017-1-24-153A413A17.png" sidth=45%>

3. The variable is added to the profile accordingly.
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/variable-types/default-profile.png" width=65%>

### Set default profile at project level

You may have multiple profiles for executing your tests, for instance, staging and production profiles with corresponding global variables. It would be convenient if you can set a profile as your default one in every execution of a project. Starting from **version 7.4.2**, you can configure a default profile at the project level.

Right-click on your desired execution profile and select **Set as default Execution Profile**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-profile-v54/set-default-profile.png" width=45%>

This profile becomes a default execution option for Test Case, Test Suite, and Test Suite Collection.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-profile-v54/tsc.png" width=65%>

It's also applied for the Executive Platform of the Command Generator in case you use Katalon Runtime Engine.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-profile-v54/cli.png" width=65%>

### Profile Inheritance

**Profile Inheritance** allows you to define a default profile that configures testing environments through global variables and to define derived (custom) profiles that either inherit or override those configurations. Here are two common use cases:

1. If a particular variable is not found in the selected running profile (any other but **default**), the test case will pick the value from the **default** to execute. 
2. If certain variables are shared across all profiles, but the values are not changing, you can define them in the **default** and remove them from the **custom profiles**.

The following example illustrates how the **Profile Inheritance** feature works:

1. Define a default profile and a derived profile

* Default profile with `profile`= default <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-profile-v54/default-profile.png" width=50%>

* Derived profile with `profile`= HelloMe <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-profile-v54/hello-me.png" width=50%>

1. In a test case, execute the test case with 

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-profile-v54/TC1.png" width=65%>

   - HelloMe: <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-profile-v54/run-with-hello-me.png" width=65%> 

2. When executing the test case with each profile (one at a time), the **Console** log shows:

- default: <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-profile-v54/run-with-default.png" width=65%>

- MyProfile: <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-profile-v54/run-with-custom.png" width=65%>

### View a profile 

Execution profile is provided with **Manual view** and **Script view** where an XML editor is available for adding variables via script. Depending on the project needs, you can create as many profiles as you want to.

In the **Script view**, profiles are in sync once a similar list of **Global Variables** is required for testing different environment types. To conduct, copy and paste the variables list from one profile to another.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-profile-v54/profile-script-view.png" width=50%>

### Use a profile and Usage Examples

By default, Katalon Studio uses the **default** profile for executing tests, as indicated on the top right corner of the screen. You can select any available execution profiles in the drop-down menu.

The following section shows you a usage example. Based on testing environments, there are three profiles: **local**, **staging**, and **production**.

- **For test cases or test suites**: Select your desired profile on the top right > **all Global Variables** within your current project automatically uses these values.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-profile-v54/Untitled2.png" width=65%>

- **For Test Suite Collection**: Select your desired profile to be executed with your Test Suite on the **Profile** column.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-profile-v54/4.png" width=65%>

- **For [Console Mode](/display/KD/Console+Mode+Execution) execution**: Select your desired profile on the **Profile** field.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-profile-v54/5.png" width=50%>

   The **Generated Command** has **executionProfile** parameter so that you can change it manually. For example:

   ```groovy
   katalonc -noSplash  -runMode=console -consoleLog -projectPath="C:\Users\Admin\Katalon Studio\yourProject.prj" -retry=0 -testSuitePath="Test Suites/TS_RegressionTest" -executionProfile="local" -browserType="Chrome (headless)
   ```

## Global Variables



### Use a Global Variable

Any test cases across a project can use global variables - for example, input data for keywords in [Manual View](/display/KD/Manual+View) or params when [binding Data for Test Execution](/display/KD/Design+a+Test+Suite#DesignaTestSuite-VariableBinding).

```groovy
import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject

import com.kms.katalon.core.webui.keyword.WebUiBuiltInKeywords as WebUI

import internal.GlobalVariable as GlobalVariable

WebUI.comment('Story: Login to CURA system')

WebUI.comment('Given that the user has the valid login information')

WebUI.openBrowser(GlobalVariable.G_SiteURL)

WebUI.click(findTestObject('Page_CuraHomepage/btn_MakeAppointment'))
%
WebUI.setText(findTestObject('Page_Login/txt_UserName'), Username)

WebUI.setText(findTestObject('Page_Login/txt_Password'), Password)

WebUI.comment('When he logins to CURA system')

WebUI.click(findTestObject('Page_Login/btn_Login'))

WebUI.comment('Then he should be able to login successfully')

landingPage = WebUI.verifyElementPresent(findTestObject('Page_CuraAppointment/div_Appointment'), GlobalVariable.G_Timeout)

WebUI.closeBrowser()
```

### Parameterize a Global Variable

Enter the syntax `${GlobalVariable.name}` in any supported locations. For example:

in HTTP Body of an API Test Object:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/variable-types/1-GlobalVariable.png" width=55%>

in Selected Locator of a WebUI Test Object:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/variable-types/2-GlobalVariable.png" width=55%>

### Use escaping, special characters

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

To create global variables during runtime, here is an approach provided by [Sergii Tyshchenko](https://forum.katalon.com/t/how-to-pass-user-defined-parameters-from-command-line/8771/22?u=jass).

You can define environment variable (with path to external configuration or properties file) in the session that is used to execute Katalon Studio. Then in the `TestListener`, read the variable's value (path to the file), load that file and override the project settings, or Global variables. Use the following metaprogramming:

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

It’s possible to add getter and/or setter as new methods to the `GlobalVariable` class or add a new field. Then in the script, you can use GlobalVariable.VarName where the VarName is your new variable.

```groovy
CustomKeywords.'helper.addGlobalVariable'('localURL', 'katalon.com')
println GlobalVariable.localURL
```

> Go to the [original discussion](https://forum.katalon.com/t/how-to-define-global-variables-within-scripts-i-e-on-the-fly/). 
