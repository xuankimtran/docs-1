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

**Execution Profile** helps cover multiple and different environments to execute your automation test scripts with ease. You can configure the testing environment in terms of data and behaviors through **Global variables**. 

### Create a profile

Just like other test artifacts, you can CRUD the **Execution Profile** in the **Tests Explorer**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-profile-v54/Untitled3.png" width=55%>
   
In a profile, you need to define its content via adding [Global variables](https://docs.katalon.com/katalon-studio/docs/execution-profile-v54.html#global-variables). Do as follows:

1. Select a profile > click **Add**.
2. In the **New Variable** dialog, specify details for the variable > click **OK**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/variable-types/image2017-1-24-153A413A17.png" sidth=60%>

3. The variable is added to the profile accordingly.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/variable-types/default-profile.png" width=70%>

### View a profile 

Execution profile is provided with **Manual view** and **Script view** where an XML editor is available for adding variables via script. Depending on the project needs, you can create as many profiles as you want to.

In the **Script view**, profiles are in sync once a similar list of **Global Variables** is required for testing different environment types. To conduct, copy and paste the variables list from one profile to another.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-profile-v54/profile-script-view.png" width=65%>

### Set default profile at project level

You may have multiple profiles for executing your tests, for instance, staging and production profiles with corresponding global variables. It would be convenient if you can set a profile as your default one in every execution of a project. Starting from **version 7.4.2**, you can configure a default profile at the project level.

Right-click on your desired execution profile and select **Set as default Execution Profile**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-profile-v54/set-default-profile.png" width=45%>

This profile becomes a default execution option for Test Case, Test Suite, and Test Suite Collection.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-profile-v54/tsc.png" width=70%>

It's also applied for the Executive Platform of the Command Generator in case you use Katalon Runtime Engine.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-profile-v54/cli.png" width=70%>

### Profile Inheritance

Profile Inheritance allows you to define a default profile that configures testing environments through global variables and to define derived (custom) profiles that either inherit or override those configurations.

During the execution, if global variables are not defined in the profile being executed with, then Katalon 

During the execution, if Katalon does not find a variable that is used in the test within the designated profile, it’ll look into Default Profile.

**How to utilize Profile Inheritance**

Commonly used global variables should be stored in the **default** profile and other sets of global variables should be stored in the **derived** (custom) profiles to avoid the code from duplicating and for an easy code management.

**Running the examples**

The following examples illustrate how the **Profile Inheritance** feature works.

- Given test case:

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-profile-v54/inherit-sample.png" width=70%>

- Execute default profile with given test case:

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-profile-v54/inherit-default-profile.png" width=70%>

   The result is shown as below:

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-profile-v54/inherit-console-default.png" width=70%>

- Execute stagging and production profile with given test case:
   
   When executing the stagging and production profiles, the **name**, **serveURL** and **credential** variables are overriden (highlighted in blue) while the **usage** and **reference** variables are inherited (highlighted in red) from the global variables in default profile. 

   - Stagging profile:

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-profile-v54/inherit-stagging-profile.png" width=70%>

      The result is shown as below:

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-profile-v54/inherit-console-stagging.png" width=70%>

   - Production profile:

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-profile-v54/inherit-production-profile.png" width=70%>

      The result is shown as below:
   
      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-profile-v54/inherit-console-production.png" width=70%>

### Use a profile

By default, Katalon Studio uses the **default** profile for executing tests, as indicated on the top right corner of the screen. You can select any available execution profiles in the drop-down menu.

The following section shows you a usage example. Based on testing environments, there are three profiles: **local**, **staging**, and **production**.

- **For test cases or test suites**: Select your desired profile on the top right > **all Global Variables** within your current project automatically uses these values.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-profile-v54/Untitled2.png" width=70%>

- **For Test Suite Collection**: Select your desired profile to be executed with your Test Suite on the **Profile** column.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-profile-v54/4.png" width=70%>

- **For [Console Mode](/display/KD/Console+Mode+Execution) execution**: Select your desired profile on the **Profile** field.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-profile-v54/5.png" width=70%>

   The **Generated Command** has **executionProfile** parameter so that you can change it manually. For example:

   ```groovy
   katalonc -noSplash  -runMode=console -consoleLog -projectPath="C:\Users\Admin\Katalon Studio\yourProject.prj" -retry=0 -testSuitePath="Test Suites/TS_RegressionTest" -executionProfile="local" -browserType="Chrome (headless)
   ```

## Global Variables

A **global variable** is a variable defined in the execution profile and can be used in test cases, test object, web service object and email configuration in the project.

### Scope of Global Variables

**Global Variables** are visible in the scope of a **Test Case** or a **Test Suite**, **NOT** in a Test Suite Collection. In other words, a profile that contains a set of global variables can be executed by a Test Case or a Test Suite only. In other words:

- **A Profile is Test Case scoped** implies that you can choose to execute a Test Case with any available Profiles (as in the following screenshot).

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-profile-v54/test-case-scoped.png" width=70%>

- In a Test Suite Collection, you can list a single Test Suite more than once with different Profiles applied. In the following screenshot, you can find “Test Suites/New Test Suite (1)” is listed twice. The first one has “default" Profile, and the second one has “stagging”. This association proves that **a Profile is Test Suite scoped**. Otherwise, the association can not be logically valid.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-profile-v54/test-suite-scoped.png" width=70%>

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

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/variable-types/1-GlobalVariable.png" width=70%>

in Selected Locator of a WebUI Test Object:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/variable-types/2-GlobalVariable.png" width=70%>

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

- Without `\`: *note: Currency unit of ${GlobalVariable.productName} is $*.
- With `\`: *note: Currency unit of wine is $*.

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
