---
title: "BDD Testing Framework (Cucumber integration)" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/cucumber-features-file.html 
redirect_from:
    - "/display/KD/Cucumber+Features+File/"
    - "/display/KD/Cucumber%20Features%20File/"
    - "/x/OBLR/"
    - "/katalon-studio/docs/cucumber-features-file/"
    - "/katalon-studio/docs/running-cucumber-features-file.html"
    - "/display/KD/Running+Cucumber+Features+File/"
    - "/display/KD/Running%20Cucumber%20Features%20File/"
    - "/x/PhLR/"
    - "/katalon-studio/docs/running-cucumber-features-file/"
    - "/display/KD/Step+Definitions/"
    - "/display/KD/Step%20Definitions/"
    - "/x/OxLR/"
    - "/katalon-studio/docs/step-definitions/"
    - "/katalon-studio/docs/step-definitions.html"
description: 
---

## Add Feature Files

> For the best performance, please clean up the Katalon workspace frequently. Navigate to **File** \> **Clean up**.

Features File is located within **'Include/'features'** folder from your project folder and can be seen from _Tests Explorer_:

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/cucumber-features-file/Screenshot-at-Sep-04-11-17-22.png)

The content of _Features_ File will follow BDD conventions (_Given, When, The_n). When creating a new _Features_ File, there will be an option to '**Generate sample Feature template**' which will generate a sample template for your _Features_ File. This will ensure that the created _Features_ File matches with BDD convention so that you will reduce efforts in creating _Features_ File in the correct format. 

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/cucumber-features-file/Screen-Shot-2018-09-06-at-11.34.52-AM.png)

Let's look at an example of Katalon Demo Cura System ([http://demoaut.katalon.com).](http://demoaut.katalon.com%29./) We want to test the _Login_ feature with a valid and invalid credential so the content will be something like this:

> Tags are a great way to organize Features and Scenarios. [Read more...](https://docs.cucumber.io/cucumber/api/#tags)

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/cucumber-features-file/Screen-Shot-2018-09-06-at-9.00.58-AM.png)

**Sample Features File**

```gherkin
#Author: your.email@your.domain.com
#Keywords Summary :
#Feature: List of scenarios.
#Scenario: Business rule through list of steps with arguments.
#Given: Some precondition step
#When: Some key actions
#Then: To observe outcomes or validation
#And,But: To enumerate more Given,When,Then steps
#Scenario Outline: List of steps for data-driven as an Examples and <placeholder>
#Examples: Container for s table
#Background: List of steps run before each of the scenarios
#""" (Doc Strings)
#| (Data Tables)
#@ (Tags/Labels):To group Scenarios
#<> (placeholder)
#""
## (Comments)
#Sample Feature Definition Template
@Login
Feature: Login Feature
  
  As a user, I want to login to Cura System
  so that I can make an appointment.

  @Valid
  Scenario Outline: Login with a valid credential
    Given I navigate to Cura System homepage
    When I click Make Appointment button
    And I enter username <username> and password <password>
    And I click Log in button 
	Then I should be able to login successfully

    Examples: 
      | username | password           |
      | John Doe | ThisIsNotAPassword |

  @InValid
  Scenario Outline: Login with an invalid credential
    Given I navigate to Cura System homepage
    When I click Make Appointment button
    And I enter an invalid username <username> and password <password>
    And I click Log in button
	Then I should NOT be able to login successfully

    Examples: 
      | username | password           |
      | Jane Doe | ThisIsNotAPassword |
```

## Maintain Features File

> Katalon Studio code inspection will detect and highlight any missing _Step Definitions_ in _Features File_ to help the user create the required step definitions.

  
There will be cases the current _Features_ File meet one of the following maintenance difficulties:

*   The current format is not organized properly.
*   Figure out which _Step Definitions_ is mapped with current _Gherkin_ step.
*   Recalculate steps in the _Features_ file when there are changes in _Step Definitions_.

Above difficulties have been handled directly from the context menu of Feature File editor.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/cucumber-features-file/Screen-Shot-2018-09-06-at-9.04.08-AM.png)

**Pretty Format**

Re-do the format.

**Find Step**

Find relevant step of current Gherkin step in existing Step Definitions files.

**Recalculate steps**

Recalculate steps in the Feature file when there are changes in Step Definitions.

## Define Steps

Each Gherkin step in the _Features_ file needs to be defined as a set of programming code so that the machine can execute the actions of these steps. These _Step Definitions_ can be implemented in _Keyword_ folder by leveraging the **Script Mode**. Katalon Studio built-in keywords can also be re-used in step definition files as well. When Katalon Studio executes any _Features_ files in the test case, it will also look for the matching step definitions in the source folder.

> Step Definitions can be written in any Cucumber-supported programming languages including Groovy and Java.

  
For example, let's take the Gherkin scenarios from _Features_ File above and define the steps:

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/step-definitions/Screen-Shot-2018-08-30-at-2.11.31-PM.png)

**Step Definitions**

```groovy
class MyStepDefinition {

	/**
	 * The step definitions below match with Katalon sample Gherkin steps
	 */

	@Given("I navigate to Cura System homepage")
	def I_navigate_to_Cura_System_homepage() {

		WebUI.openBrowser("http://demoaut.katalon.com")
		//WebUI.waitForPageLoad(30)
	}

	@When("I click Make Appointment button")
	def I_click_makeAppointment_button() {

		WebUI.click(findTestObject('Page_CURA Healthcare Service/a_Make Appointment'))
	}
 
	@And("I enter username (.*) and password (.*)")
	def I_enter_valid_username_password(String username, String password) {

		WebUI.setText(findTestObject('Page_CURA Healthcare Service/input_userName'), username)
		WebUI.setText(findTestObject('Page_CURA Healthcare Service/input_password'), password)
	}
 
	@And("I click Log in button")
	def I_click_login_btn() {

		WebUI.click(findTestObject('Page_CURA Healthcare Service/button_Login'))
	}
 
	@Then("I should be able to login successfully")
	def I_login_successfully() {

		WebUI.click(findTestObject('Page_CURA Healthcare Service/button_Login'))
		WebUI.verifyTextPresent('Make Appointment', false)
		WebUI.closeBrowser()
	}

	@And("I enter an invalid username (.*) and password (.*)")
	def I_enter_invalid_username_password(String username, String password) {
		
		WebUI.setText(findTestObject('Page_CURA Healthcare Service/input_userName'), username)
		WebUI.setText(findTestObject('Page_CURA Healthcare Service/input_password'), password)
	}

 
	@Then("I should NOT be able to login successfully")
	def I_login_unsuccessfully() {

		WebUI.verifyTextPresent('Login failed! Please ensure the username and password are valid.', false)
		WebUI.closeBrowser()
	}

}

```

## From a Feature File

### From Toolbar

Katalon Studio allows you to run the feature file instantly by itself to make sure it works properly. Open the desired **Features** file, click the **Play** button on the main toolbar.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/running-cucumber-features-file/Screen-Shot-2018-09-06-at-10.11.40-AM.png)

### In Test Cases

Katalon Studio supports Cucumber keywords along with the original built-in keywords. The user doesn't have to import Cucumber libraries into Katalon Studio.

To include Cucumber _Feature_ file in Katalon Studio test case:

#### Execute a single Feature File (with or without tags)

* [runFeatureFile](https://docs.katalon.com/katalon-studio/docs/cucumber-kw-run-feature-file.html)
* [runFeatureFileWithTags](https://docs.katalon.com/katalon-studio/docs/cucumber-kw-run-feature-file-tag.html)

#### Execute multiple Feature Files (with or without tags)

* [runFeatureFolder](https://docs.katalon.com/katalon-studio/docs/cucumber-kw-run-feature-folder.html)
* [runFeatureFolderWithTags](https://docs.katalon.com/katalon-studio/docs/cucumber-kw-run-feature-folder-tag.html)

#### Execute using [Cucumber Runner](http://toolsqa.com/cucumber/junit-test-runner-class/)

* [runWithCucumberRunner](https://docs.katalon.com/katalon-studio/docs/cucumber-kw-run-cucumber-runner.html)

## Cucumber Reports

### In Katalon TestOps

Katalon TestOps has dedicated support for viewing BDD test results as well as advanced analytics and reports such as Traceability Matrix Report. Please follow [this tutorial](https://forum.katalon.com/t/better-bdd-support-in-katalon-studio-7-8-beta/47977/2) to configure.

### In Katalon Studio

There is **NO** custom report for executing Feature File. Katalon Studio uses only generated Cucumber **reports** for **Test Suite/Test Suite Collection** execution **level**, in which the test cases contain the Cucumber Features file.

The generated Cucumber report of Test Suite/Test Suite Collection will be located in the same folder of Katalon Studio report's folder. In Katalon Studio Tests Explorer, right-click at the desired **Report > Open Containing Folder**. Katalon Studio will redirect you to the local folder where Cucumber Reports are stored. 

Katalon Studio supports **three** formats for Cucumber reports: JSON, XML, HTML.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/running-cucumber-features-file/Screenshot-at-Sep-04-20-01-21.png)
