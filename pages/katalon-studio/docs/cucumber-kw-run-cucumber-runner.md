---
title: "[Cucumber] Run with Cucumber Runner"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/cucumber-kw-run-cucumber-runner.html
---
* **Description**: Execute a Feature File with a set of options using [Cucumber Runner](http://toolsqa.com/cucumber/junit-test-runner-class/). Example you've created a Step Definitions called **MyCucumberRunner** within scripts folder ("Include/scripts/groovy" folder).
* **Keyword name**: runWithCucumberRunner
* **Keyword syntax**: runWithCucumberRunner(cucumberRunnerClass, flowControl)
* **Parameters**:
  * Name: cucumberRunnerClass
    * Description: a class that is annotated with Cucumber runner
    * Parameter Type: Class
    * Mandatory: Required
  * Name: flowControl
    * Description: an instance com.kms.katalon.core.model.FailureHandling that controls the running flow
    * Parameter Type: FailureHandling
    * Mandatory: Optional
* **Returns**: an instance of CucumberRunnerResult that includes status of keyword and JUnit Runner result.
* **Example**:

```groovy
CucumberKW.runWithCucumberRunner(MyCucumberRunner.class)
```

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/running-cucumber-features-file/Screen-Shot-2018-09-06-at-17.13.04.png)

* **Example #1**: Run all Feature files in **Include/features** Folder

```groovy
    import org.junit.runner.RunWith;
    import cucumber.api.CucumberOptions;
    import cucumber.api.junit.Cucumber;
    
    @RunWith(Cucumber.class)
    @CucumberOptions(features = "Include/features", glue = "")
    public class MyCucumberRunner {}

```

* **Example #2**: Run all Feature files in a specified file/folder

```groovy
    import org.junit.runner.RunWith;
    import cucumber.api.CucumberOptions;
    import cucumber.api.junit.Cucumber;
    
    @RunWith(Cucumber.class)
    @CucumberOptions(features = "Your_Folder_Or_File_Path", glue = "")
    public class MyCucumberRunner {}

```

* **Example #3**: Run all Feature files in a specified file/folder, generate JUnit Cucumber report with XML pretty format, and copy to a specified folder

```groovy
    import org.junit.runner.RunWith;
    import cucumber.api.CucumberOptions;
    import cucumber.api.junit.Cucumber;
    @RunWith(Cucumber.class)
    @CucumberOptions(features="Your_Folder_Path", glue="", plugin = ["pretty",
                        "junit:Folder_Name/cucumber.xml"])
    public class MyCucumberRunner {
    }

```

* **Example #4**: Run all Feature files in a specified file/folder, generate multi Cucumber reports with XML, JSON, HTML pretty format, and copy to a specified folder

```groovy
    import org.junit.runner.RunWith;
    import cucumber.api.CucumberOptions;
    import cucumber.api.junit.Cucumber;
    @RunWith(Cucumber.class)
    @CucumberOptions(features="Your_Folder_Path", glue="", plugin = ["pretty",
                        "junit:Folder_Name/cucumber.xml",
                        "html:Folder_Name",
                        "json:Folder_Name/cucumber.json"])
    public class MyCucumberRunner {
    }
```
