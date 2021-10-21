---
title: "Use Test Hooks for Cucumber Framework" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/cucumber-test-hook.html
redirect_from:
description: 
---

The integration of the Cucumber framework in Katalon Studio allows you to include Cucumber test hooks, which work at the start and the end of a scenario in a behavior-driven development (BDD) test. To learn more about test hooks in the Cucumber framework, you can refer to this document: [Cucumber Hooks reference](https://cucumber.io/docs/cucumber/api/#hooks).

This guide shows you how to create and use Cucumber hooks in Katalon Studio.

> You can download the sample project here on our Github repository: [Katalon BDD Cucumber Tests](https://github.com/katalon-studio-samples/katalon-bdd-cucumber-tests).

## Set up Cucumber Hooks

### Create Cucumber Feature file
To apply hooks in the Cucumber BDD test, first you need to create a Cucumber Feature file and its corresponding step definitions.

1. To create a Cucumber Feature file, go to **File > New > BDD Feature File**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/cucumber-test-hooks/KS-Create-new-feature-file.png" width=70% alt="New Feature File dialog">

    You can tick the **Generate sample feature** option for a sample feature file.

    For example:

    ```groovy
    #Sample Feature Definition Template
    @tag
    Feature: Title of your feature
    I want to use this template for my feature file

    @tag1
    Scenario Outline: Title of your scenario outline
        Given I want to write a step with <name>
        When I check for the <value> in step
        Then I verify the <status> in step

        Examples: 
        | name  | value | status  |
        | name1 |     5 | success |
        | name2 |     7 | Fail    |
    ```

2. To create step definitions, go to **File > New > Groovy Script**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/cucumber-test-hooks/KS-Generate-sample-step-defintions.png" width=70% alt="Create Keyword Dialog">

    You can tick the **Generate sample @Given, @When, @Then steps** for sample step definitions.

    For example:
    ```groovy
    class Sample {

        /**
        * The step definitions below match with Katalon sample Gherkin steps
        */
        @Given("I want to write a step with (.*)")
        def I_want_to_write_a_step_with_name(String name) {
            println name
        }

        @When("I check for the (\\d+) in step")
        def I_check_for_the_value_in_step(int value) {
            println value
        }

        @Then("I verify the (.*) in step")
        def I_verify_the_status_in_step(String status) {
            println status
        }
    }

    ```

### Add Cucumber Hooks

1. Create another step definition or a custom keyword that includes the Cucumber hooks. Here, we create a step definition.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/cucumber-test-hooks/KS-New-Cucumber-hooks-script.png" width=70% alt="New Cucumber hook script">

2. Enter Cucumber hooks into the new step definition. For example, to add ```@Before``` and ```@After``` scenario hooks, copy and paste the following script:

    ```groovy
    class SampleTestHook {
        @Before
        public void beforeScenario(Scenario scenario) {
            println 'This is a before scenario method: ' + scenario.getName()
        }

        @After
        public void afterScenario(Scenario scenario) {
            println 'This is a after scenario method: ' + scenario.getName()
        }
    }
    ```

## Create a test case with Cucumber hooks

1. In the **Manual** view of the new test case, click on the **Add** dropdown button and select **Cucumber Keywords**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/cucumber-test-hooks/KS-Add-Cucumber-keyword.png" width=70% alt="Add Cucumber Keywords">

2. Select the **Run Feature File** keyword. 

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/cucumber-test-hooks/KS-select-run-feature-file-keyword.png" width=70% alt="Select Run Feature File keyword">


3. To get the relative path, right-click on the Feature file and select **Copy ID**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/cucumber-test-hooks/KS-Copy-ID-feature-file.png" width=70% alt="Copy ID of Feature file">

4. Double-click on the **Input** cell of the **Run Feature File** keyword. In the displayed **Input** dialog, paste the copied relative path from step 3 as the input value.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/cucumber-test-hooks/KS-Feature-file-input-value.png" width=70% alt="Paste keyword input value">

5. Run the test and verify the message of the Cucumber hooks in the **Console** log:

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/cucumber-test-hooks/KS-Cucumber-hooks-message.png" width=70% alt="Cucumber hooks message">

**See also**: 

* [Cucumber Integration in Katalon Studio](https://docs.katalon.com/katalon-studio/docs/cucumber-features-file.html)
