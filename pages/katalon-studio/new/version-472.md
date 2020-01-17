---
title: "Version 4.7.x"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/new/version-472.html
redirect_from:
    - "/display/KD/Version+4.7.2/"
    - "/display/KD/Version%204.7.2/"
    - "/x/IxJO/"
    - "/katalon-studio/new/version-472/"
    - "/katalon-studio/new/version-471.html"
    - "/display/KD/Version+4.7.1/"
    - "/display/KD/Version%204.7.1/"
    - "/x/GRFO/"
    - "/katalon-studio/new/version-471/"
    - "/katalon-studio/new/version-470.html"
    - "/display/KD/Version+4.7.0/"
    - "/display/KD/Version%204.7.0/"
    - "/x/Tw5O/"
    - "/katalon-studio/new/version-470/"
description:
---

## Version 4.7.2

### JIRA Integration

*   New icon on main toolbar to indicate status of JIRA integration and help users quickly access relevant function as needed.
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-472/image2017-8-10-163A363A58.png)


*   [Import Test Cases from JIRA via JQL:](/display/KD/Working+with+JIRA) This feature allows users to specify JIRA Tickets to be synced to Katalon Studio using JQL query syntax of JIRA
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-472/image2017-8-2-113A253A3.png)


*   [Katalon Studio add-on for JIRA:](/display/KD/Install+and+Use+Katalon%27s+JIRA+add-on) An add-on for JIRA so that business users can involve with development team. Project Managers or Business Analyst can compose requirements on JIRA under the BDD's format. These requirements will be synced with Katalon Studio so that test script can be generated and associated accordingly.

    Basic functions and features of this JIRA add-on are as following:



    *   Katalon BDD - JIRA custom Gherkin field
    *   Sync JIRA Issues back and forth
    *   Sync Katalon Studio test execution via attachment


    ![Design test cases in Gherkin](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-472/17c5dea4-e386-499a-95e4-d2934f75fa70.png)

    The add-on is listed at [Atlassian Marketplace](https://marketplace.atlassian.com/plugins/com.katalon.katalon-jira-plugin). Currently, we only suport JIRA server. To install the add-on, please follow [Atlassian's instruction](https://marketplace.atlassian.com/plugins/com.katalon.katalon-jira-plugin/server/installation).

## Version 4.7.1

### General Improvement

KatalonStudio [Test Case Script View](/display/KD/Test+Case+Script+View) is updated with new font:

*   Windows: Consolas 12
*   Mac OS: Menlo 14

### qTest Integration

 Improve overall UI of qTestintegration:

*   The user interfaces when setting up qTest integration are optimized for better user experiences and fixed bugs.  For more details, please refer to [qTest Integration](/display/KD/qTest+Integration).

    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-471/image2017-8-1-183A263A14.png)


*   Integrated test artifacts will have dedicated icon as shown below:
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-471/image2017-8-4-173A63A56.png)

## Version 4.7.0

### General Improvement

The **Katalon Help** page is updated to provide new users with three basic steps regarding how to get start with Katalon Studio quickly. Users can also specify location to create their new sample projects as appropriated.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-470/image2017-7-10-173A133A44.png)

### Test Case

Introduce **Properties** tab for Test Case. The read-only **Comment** field, whose value is extracted from [Comment](/display/KD/%5BCommon%5D+Comment) keywords, allows users to annotate their automation script for reviewing purpose. The below screenshot showcases how BDD and its Gherkin syntax is leverage to give description for the test case. Thus, allow business stakeholders such as BA or PM to involve in development process. 

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-470/image2017-6-23-153A413A54.png)

### Log Viewer

When viewing execution log in **Log Viewer**, users can now navigate to the respective step by selecting from the context menu. 

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-470/image2017-6-23-153A553A57.png)

### Report

Allow execution of Test Suites to be generated as JUnit report in XML format.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-470/image2017-6-23-163A23A2.png)

Execution of Test Suite Collection can now be exported to HTML format.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-470/image2017-6-23-163A123A5.png)

### Test Suite

Add **Map All** button to Variables Binding section so that users can quickly match test variables of test case with respective column of test data.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-470/image2017-6-23-163A83A7.png)

### Execution

Execution speed between actions can be specified based on the preference defined in **Project > Settings > WebUI**. This option provides the possibility for users to slow down test execution to a suitable level for their specific needs (e.g. observing the execution or doing demo...)

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-470/image2017-6-23-163A153A42.png)

### Keywords

| Keyword | Description |
| --- | --- |
| [\[WebUI\] Verify Element Text](/display/KD/%5BWebUI%5D+Verify+Element+Text) | Verify text of an element. |
| [\[WebUI\] Verify Options Present](/display/KD/%5BWebUI%5D+Verify+Options+Present) | Verify if all expected options are present within the given test object. |
| [\[WebUI\] Click Offset](/display/KD/%5BWebUI%5D+Click+Offset) | Click on the given element with the relative position (x, y) from the top-left corner of that element |
| [\[WebUI\] Right Click Offset](/display/KD/%5BWebUI%5D+Right+Click+Offset) | Right click on the given element with the relative position (x, y) from the top-left corner of that element |
| [\[WebUI\] Mouse Over Offset](/display/KD/%5BWebUI%5D+Mouse+Over+Offset) | Simulate users hovering a mouse over the given element with the relative position (x, y) from the top-left corner of that element. |
| [\[Mobile\] Send Keys](/display/KD/%5BMobile%5D+Send+Keys) | Simulates keystroke events on the specified element, as though you typed the value key-by-key.  |
| [\[Mobile\] Verify Element Text](/display/KD/%5BMobile%5D+Verify+Element+Text) | Verify text of an element. |