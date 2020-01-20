---
title: "Version 4.x"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/new/version-48.html
redirect_from:
    - "/display/KD/Version+4.8/"
    - "/display/KD/Version%204.8/"
    - "/x/yRBO/"
    - "/katalon-studio/new/version-48/"
    - "/katalon-studio/new/version-472.html"
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
    - "/katalon-studio/new/version-46.html"
    - "/display/KD/Version+4.6/"
    - "/display/KD/Version%204.6/"
    - "/x/1gxO/"
    - "/katalon-studio/new/version-46/"
    - "/katalon-studio/new/version-45.html"
    - "/display/KD/Version+4.5/"
    - "/display/KD/Version%204.5/"
    - "/x/LgNO/"
    - "/katalon-studio/new/version-45/"
    - "/katalon-studio/new/version-44.html"
    - "/display/KD/Version+4.4/"
    - "/display/KD/Version%204.4/"
    - "/x/-ocw/"
    - "/katalon-studio/new/version-44/"
    - "/katalon-studio/new/version-43.html"
    - "/display/KD/Version+4.3/"
    - "/display/KD/Version%204.3/"
    - "/x/nIUw/"
    - "/katalon-studio/new/version-43/"
    - "/katalon-studio/new/version-42.html"
    - "/display/KD/Version+4.2/"
    - "/display/KD/Version%204.2/"
    - "/x/rYIw/"
    - "/katalon-studio/new/version-42/"
    - "/katalon-studio/new/version-41.html"
    - "/display/KD/Version+4.1/"
    - "/display/KD/Version%204.1/"
    - "/x/HoEr/"
    - "/katalon-studio/new/version-41/"
    - "/katalon-studio/new/version-400.html"
    - "/display/KD/Version+4.0.0/"
    - "/display/KD/Version%204.0.0/"
    - "/x/CYMi/"
    - "/katalon-studio/new/version-400/"
description:
---

## Version 4.8.0

### General Improvement

**Enhanced Katalon Help**

Introducing brand new Katalon Help page for Katalon Studio application. Users can access Katalon Studio resources all in one place such as Tutorials, FAQs, Sample Projects, or User Guides.

**![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-48/image2017-9-1-173A83A59.png)**

**[Support Shadow DOM](/display/KD/Working+with+Shadow+DOM+Objects)**

Katalon Studio Version 4.8 supports objects with Shadow DOM in Web Testing. Users can identify Shadow DOM objects by specifying the Shadow Root Parent in the Object settings tab.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-48/image2017-8-15-113A323A52.png)

### Test Suite

[**Video Capturing**](/display/KD/Video+Capturing)

> [K-Lite Codec](https://www.codecguide.com/download_kl.htm) is recommended to play Katalon Studio test execution video.

Introducing Katalon Studio **new** feature **video capturing** for Test Suite reports. Users will be able to video capture test suite execution and replay to review how each test case was executed. Description of test steps will be added as subtitle for users convenience. **Video capturing** feature can be enable in **Project Settings**.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-48/image2017-8-25-143A93A49.png)

[**Variable Binding**](/display/KD/Execute+a+test+suite#Executeatestsuite-VariableBinding)

Variable Binding has been improved to allow users to set or update **Type** and **Test Data **column of multiple rows at once.This improvement aims to save testing time and to eliminate several repetitive procedures.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-48/image2017-8-17-143A273A14.png)

### JIRA Integration

[Katalon Studio add-on for JIRA:](/display/KD/Install+and+Use+Katalon%27s+JIRA+add-on) An add-on for JIRA so that business users can involve with development team. Project Manager or Business Analyst can compose requirements on JIRA under the BDD's format. These requirements will be synced with Katalon Studio so that test script can be generated and associated accordingly.

*   Basic functions and features of this JIRA add-on are as following:

    *   Katalon BDD - JIRA custom Gherkin field
    *   Sync JIRA Issues back and forth
    *   Sync Katalon Studio test execution via attachment


    ![Design test cases in Gherkin](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-48/17c5dea4-e386-499a-95e4-d2934f75fa70.png)

    The add-on is listed at [Atlassian Marketplace](https://marketplace.atlassian.com/plugins/com.katalon.katalon-jira-plugin). Currently, we only suport JIRA server. To install the add-on, please follow [Atlassian's instruction](https://marketplace.atlassian.com/plugins/com.katalon.katalon-jira-plugin/server/installation).


### Mobile Testing

[Record](/display/KD/Recording+Mobile+Test) and [Spy](/display/KD/Mobile+Object+Spy) Mobile is improved to support Kobiton devices, a cloud-based devices platform. Testing team can run test automation on hundreds of Kobiton devices.

*   Users can choose 2 options in **Device Types**:
    *   Local devices: This will list out all local devices and simulators.
    *   Kobiton device: This will list out Kobiton's devices that integrated with Katalon Studio
*   **Device Name**: display all devices name accordingly based on selected type in **Device Types**

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-48/image2017-8-15-163A403A14.png)

### Test Case

Introducing **Recent Keywords** and **Recent Objects** features in **Manual** mode when writing a test case. This will optimize time and reduce repetitive tasks for users.

**[Recent Keywords](/display/KD/Test+Case+Manual+View#TestCaseManualView-RecentKeywords)** feature allows users to select and add any of the 10 last used **keywords** to Item list.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-48/image2017-8-18-173A193A14.png)

**[Recent objects](/display/KD/Test+Case+Manual+View#TestCaseManualView-RecentObjectsandObjectFolders)** feature in _Test Object Input_ dialog allows users to select and add any of the 10 last used **Test Objects.** Users can also quickly jump to **Recent Object Folder** that has recent used objects accordingly.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-48/image2017-8-25-173A293A39.png)

### Web Services

**[Support OAuth 1.0 authorization](/display/KD/RESTful)
**

Katalon Studio now supports OAuth 1.0 authorization for Web Services Testing.  OAuth (Open Standard for Authorization) is an open token-based protocol authentication and authorization that allows application to capture protected information without exposing end user credentials. Testing teams can leverage this support to test any Web Services project that required OAuth 1.0 authorization with Katalon Studio.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-48/image2017-8-23-123A93A38.png)

### Project Settings

**[Email](/display/KD/Emails+Settings)**

This version of Katalon Studio improved **Email** configuration in Project setting. Users able to customize Mail Server, send to multiple recipients, editable subject field.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-48/image2017-8-15-143A523A25.png)

New **Template** under Email section allows users to customize test execution reports and add extra fields to the report.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-48/image2017-8-15-143A493A1.png)

### Katalon Studio Console Mode for Linux OS

Katalon Studio for Linux is now available. Users can execute test automation in Linux environment by using command line mode. Refer to this guide for [Console Mode Execution](/display/KD/Console+Mode+Execution).

> *   Tested on Ubuntu, other OSes might have its own problem.
> *   Only Chrome, Firefox and Remote options are supported for console mode execution using Linux version.

**Linux OS:** [http://download.katalon.com/4.8.0/Katalon\_Studio\_Linux_64-4.8.tar.gz](http://download.katalon.com/4.8.0/Katalon_Studio_Linux_64-4.8.tar.gz)

### Keywords

New built-in keywords to help users check for broken links or images.

| Keywords | Description |
| --- | --- |
| [Get All Links On Current Page](/display/KD/%5BWebUI%5D+Get+All+Links+On+Current+Page) | Get all links on current page |
| [Verify Response Status Code](/display/KD/%5BWS%5D+Verify+Response+Status+Code) | Verify status code in the returned data from a web service call |
| [Verify Response Status Code In Range](/display/KD/%5BWS%5D+Verify+Response+Status+Code+In+Range) | Verify status code valid in a range of status codes in the returned data from a web service call |
| [Verify Links Accessible](/display/KD/%5BWebUI%5D+Verify+Links+Accessible) | Verify a list of links (URLs) are accessible |
| [Verify All Links On Current Page Accessible](/display/KD/%5BWebUI%5D+Verify+All+Links+On+Current+Page+Accessible) | Verify all links (URLs) on the current page are accessible |

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

## Version 4.6.0

### General Improvement

**Download Size Reduced **

| Platform | Katalon Studio 4.5 | Katalon Studio 4.6 |
| --- | --- | --- |
| Windows 32 bits | 430 MB | 329 MB |
| Windows 64 bits | 414 MB | 333 MB |
| macOS | 414 MB | 348 MB |

### Mobile Testing

**[Record & Playback for Mobile ](/display/KD/Recording+Mobile+Test)**

Katalon preferred Recording utility is enhanced to support both iOS and Android to cover mobile platforms. Test objects and actions will be stored and generated as test cases that can be edited using manual/scripting interfaces. The function UI is identical to web recording to help users get started quickly.  

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-46/record_mobile.png)

### Test Object

**[Parameterizing Test Objects](/display/KD/Manage+Test+Object#ManageTestObject-ParameterizingTestObject)**

This version provides the capability to handle dynamic objects (objects with particular properties changed due to certain business rules). Users can leverage Katalon Studio parameterization capability to control these objects easily.
For example, the desired properties for the test object can be declared in the manual mode even without recording & spying the AUT. These properties will be used by Katalon to identify the test object during execution dynamically.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-46/1.declare-dynamic-object.png)

Users can leverage the declared properties further by using Katalon scripting mode and adjust how the value of the properties to be perceived. (Typically, users will want to pass property value as variable or make reference to datafiles according to their situation - Refer to [Parameterizing Test Object](/display/KD/Manage+Test+Object#ManageTestObject-ParameterizingTestObject) for more details).

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-46/image2017-5-18-113A493A17.png)

### Network Configuration

**Certificate Settings**

Version 4.6 introduces the capability to bypass certificate validation supporting users with restricted network policy to work with Katalon Studio as usual. This setting can be found at: **Project > Settings > Network** and it affects both WebUI and WebService testings.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-46/image2017-5-21-203A343A16.png)

**Proxy Settings**

Proxy setup can be configured at: **Preferences > Proxy**. The setting affects both WebUI and WebService testings. 

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-46/image2017-5-18-113A523A43.png)

### Object Spy

**Hotkeys Settings**

This version supports customizable hotkeys for Object Spy function for users to choose the preferred combination or avoid confliction with UAT hotkeys. 

> This ability to change hotkeys for Object Spy only affect Chrome browser. Other browsers will be considered for future releases.


![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-46/image2017-5-28-93A383A40.png)

### Keywords

**Wait time for Angular/jQuery pages**

New built-in keywords are introduced in this version to help users with the popular JS technologies such as Angular or jQuery loading issue. Click on each keyword for more details and examples. 

| Keyword | Description |
| --- | --- |
| [Wait for Angular Load](/display/KD/%5BWebUI%5D+Wait+For+Angular+Load) | Wait for Angular/AJAX to load within the given time in second unit. |
| [Wait for jQuery Load](/display/KD/%5BWebUI%5D+Wait+for+jQuery+Load) | Wait for jQuery to load within the given time in second unit. |

**Location for screenshots**

Similar to the [\[Mobile\] Take Screenshot](/x/WpQY) keywords, this improvement allows users to specify location for screenshots taken by [\[WebUI\] Take Screenshot](/display/KD/%5BWebUI%5D+Take+Screenshot) keywords.

| Keyword | Improvement |
| --- | --- |
| [\[WebUI\] Take Screenshot](/display/KD/%5BWebUI%5D+Take+Screenshot) | Captured screenshot saved to user-defined path. The default location will be used without user-defined value. |

**Start installed Kobiton application from Katalon Studio**

Katalon Studio no longer requires the mobile UAT to be deployed on the local machine, users can start their tests with application ID generated by Kobiton. 

<table><thead><tr><th>Keyword</th><th>Improvement</th></tr></thead><tbody><tr><td><a class="external-link" href="/display/KD/%5BMobile%5D+Start+Application" rel="nofollow">[Mobile] Start Application</a></td><td><p>'Start Application' keyword will start your installed <a class="external-link" href="http://docs.kobiton.com/display/DOC/App+repository" rel="nofollow">Kobiton application</a> directly by passing generated application ID from <a class="external-link" href="http://docs.kobiton.com/display/DOC/App+repository" rel="nofollow">Kobiton application repository</a>.</p><p><strong>Example:</strong></p><pre><code class="language-groovy">Mobile.startApplication('kobiton-store:136', false)</code></pre></td></tr></tbody></table>

## Version 4.5.0

### General Improvement

**Help links to documentation **

Users are provided with context help links to quickly navigate to documentation from corresponding UIs. The quick links are available at multiple locations which includes the following major interfaces:

*   Test Case Editor
*   Test Suite Editor
*   Test Object Editor
*   Test Data Editor
*   Reports
*   Record Dialog
*   Object Spy Dialog

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-45/image2017-2-21-133A273A16.png)

**Command Palette**

This special context menu, triggered by the **Ctrl + Alt + C **key combination, displays all useful links so that users can refer to whenever needed.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-45/image2017-2-21-153A323A13.png)

**Submit Issues**

This feature saves users the trouble of going to support channels or forum whenever they want to report bugs. Now you can send issues directly from Katalon Studio.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-45/image2017-2-21-153A293A54.png)

**Close Project**

Added option to let users close the current project.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-45/image2017-2-21-133A463A40.png)

### Script Mode

**Improved Content Assist when scripting**

Autocomplete now support more suggestion during typing for **Keywords Libraries**, **API Class Names** and **Variable Names** to help speeding up your scripting routines. 

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-45/image2017-2-21-113A93A19.png)

### Manual Mode

**Improve usability**

Use **TAB** (or **Shift+TAB**) to navigate to next/previous cells. 

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-45/image2017-2-21-113A343A17.png)

### Execution

**Parallel Execution**

You can now manually start multiple web automation tests on different connected iPhone devices for parallel execution.

### Test Suite

**Reorganizing Test Suite UI **

Added option to expand/collapse **Data Binding section** to simplify layout and improve content readability. 

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-45/image2017-2-21-133A183A28.png)

### Report

****Reorganizing Report UI** **

Added option to expand/collapse **Log Details section** to simplify layout and improve content readability.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-45/image2017-2-21-133A213A35.png)

**Renaming Reports**

Reports of Katalon Studio now can be changed to different name.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-45/image2017-2-21-133A233A47.png)

## Version 4.4.0

### Object Spy / Record

**Katalon Utility**

This [extension](https://chrome.google.com/webstore/detail/katalon-utility/ljdobmomdgdljniojadhoplhkpialdid) provides the ability to capture web elements displayed in Chrome browser. Captured objects will then be loaded to Katalon Studio for post processing.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-44/image2017-1-5-93A583A58.png)

After installing this Chrome extension, Katalon users can start spying objects (or recording test cases) on the current open Chrome browser by selecting the **Active Browsers** option in **Spy** (or **Record**) dialog of Katalon Studio.   

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-44/image2017-1-5-103A373A23.png)

This is particularly helpful in case when the user needs to capture things on his current browser quickly. With the support of Katalon Utility, the user does not have to open a new browser from Katalon Studio and go thru all the steps just to reach his targeted website.

**Start session at defined URL**

From this release, users can specify the initial web address of new browsers with **Starting URL** field.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-44/image2017-1-4-103A173A26.png)

### Web Services Testing

**Improved Editor**

Completely new and overhauled SOAP/REST object editor that could be utilized as a viable option for your Web Services testing.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-44/image2017-1-4-103A213A11.png)

### Mobile Testing

**Update mobile testing engine**

Mobile Testing Core is updated to be compatible with the new Appium 1.6 and Xcode 8 on macOS Sierra (10.12). You can now perform your test on latest Android 7 and iOS 10. The setup for mobile has been updated for this upgrade. Please refer to this [guide](http://docs.katalon.com/display/KD/Mobile+on+macOS) for more details.

### Activation

Users with proxy network had been troubled activating Katalon Studio. Katalon Studio now provide an option so that users can setup proxy for online activation.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-44/image2017-1-4-103A43A21.png)

### Console Mode

**Support Test Suite Collection execution**

Katalon Studio now extends [console mode execution](http://docs.katalon.com/display/KD/Console+Mode+Execution) capabilites to support test suite collection. Users can also generate commands for Test Suite Collection execution using **Command Builder**.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-44/image2017-1-4-103A293A29.png)

### General Improvement

**Performance Improvement**

Optimize performance of Katalon Studio when working under heavy duty. System memory will be released accordingly in case of running automation test with many processing activities such as capturing screenshots, writing log...constantly.

**New Welcome page & Sample Projects**

Welcome page now have links to help new users access useful resources quickly. The simplified Sample Projects will be good references for those who seek to get a quick experience with Katalon Studio.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-44/image2017-1-4-113A313A40.png)

**Git menu relocating**

Git options are relocated from Katalon menu to main toolbar so that user could access the functions quickly.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-44/image2017-1-4-143A273A0.png)

## Version 4.3.0

### Object Spy

**Highlight Object**

Katalon Studio extends Object Spy capabilities to help users in detecting whether test objects exist on the application under test just by a simply press on Highlight Object button.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-43/image2016-11-29-183A33A28.png)

### Execution

**Control all generated browsers**

Ability to continue executing your test scripts on any browser or mobile session launched by Katalon Studio, allow users to run automation test on existing environment.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-43/image2016-11-29-173A593A48.png)

> Limitations
>
> *   Does not support Safari
> *   Only support 1 session for Microsoft Edge

**Select any test step for execution**

Tired of seeing test scripts be executed from the beginning before reaching to a certain step? This feature will save users hours of debugging.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-43/image2016-11-29-183A03A25.png)

### Test Case

**Drag and drop Test Objects**

By dragging any of your test objects into current scripting editor, the test object's path will be generated automatically. Thus, saving users alot of time in manually typing its references.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-43/image2016-11-29-183A43A57.png)

### User Interface

**Flat Icons**

Completely reworked all icons.

**Menu Reordering**

Main menu items are reordered. **Project > Properties** is renamed as **Project > Project Information** and located as a sub-item within **Project > Settings** menu.

**Properties view**

This version adds Properties view to help users accessing information of test artifacts quickly. 

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-43/image2016-11-29-173A493A37.png)

**Revise Browser selector in Object Spy/ Record**

Browsers are grouped under respective categories. Selected browser will also be indicated by corresponding icons.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-43/image2016-11-29-173A503A57.png)

**New web service's object interface**

Revised web service object interface provide users a much simpler and straightforward form to define new webservice objects.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-43/image2016-11-29-173A533A20.png)

### Performance Improvement

**Reduce time to open large project or lengthy test cases** 

Open test case and project is much faster. The performance when opening test case and project are improved dramatically.

**Reduce memory usage**

Katalon Studio now consumes less memory during operation.

### Katalon Agent

[Non-UI version of Katalon Studio is now available! It serves best as a standalone console mode execution. It's available in following versions: Mac OSX](http://download.katalon.com/4.3.0/Katalon_Agent-4.3.dmg), [Windows 64](http://download.katalon.com/4.3.0/Katalon_Agent_Windows_64-v4.3.zip) and [Windows 32](http://download.katalon.com/4.3.0/Katalon_Agent_Windows_32-v4.3.zip).

### Console Mode Generator

**Remember last selection**

Our console mode generator will now remember the last selected options. Saving users the trouble of re-selecting some general options again.

### New Keyword 

**getCSSValue**

This keyword helps retrieving CSS value of an element.

```groovy
Get CSS value of a web element
Returns:
           the current, computed value of the property
Parameters:
           to - represent the web element
           css - represent the css property name of the element
```

### qTest Integration

**Separate execution's log**

Katalon Studio will only upload logs for selected test cases instead of the whole test suite as in previous version.

## Version 4.2.0

### New Features

#### JIRA Integration

Bugs can be submitted directly fromKatalonStudio failed test results using embedded native JIRA interface. Teststeps,captured screenshots and logs will be attached automatically to the JIRA ticket. Failed execution results can also be created as sub-task or associated with an existing JIRA ID. Ticket status' synced back toKatalonStudio providing necessary information for validation.  

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-42/image2016-11-1-183A93A57.png)

#### Undo Actions

Support Undo/Redo actions (within 20 steps) for following objects:

1.  Global Variables
2.  Test Case
3.  Test Data
4.  Checkpoint

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-42/image2016-11-1-183A103A53.png)


#### Headless execution

This new option is available for web automation execution without launching the browser interface which increases execution performance and time.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-42/image2016-11-2-163A113A37.png)

> The following keywords are not supported with headless execution
>
> <table><thead><tr><th>Keyword</th><th>Known Issues</th><th>Impact</th></tr></thead><tbody><tr><td><a class="external-link" href="http://docs.katalon.com/display/KD/%5BWebUI%5D+Accept+Alert" rel="nofollow">Accept Alert</a></td><td><p>Alert is not recognizable in headless execution</p><p>(<a class="external-link" href="https://github.com/MachinePublishers/jBrowserDriver/issues/147" rel="nofollow">https://github.com/MachinePublishers/jBrowserDriver/issues/147</a>)</p></td><td>Alert keywords can't be used for verification</td></tr><tr><td><a class="external-link" href="http://docs.katalon.com/display/KD/%5BWebUI%5D+Dismiss+Alert" rel="nofollow">Dismiss Alert</a></td></tr><tr><td><a class="external-link" href="http://docs.katalon.com/display/KD/%5BWebUI%5D+Get+Alert+Text" rel="nofollow">Get Alert Text</a></td></tr><tr><td><a class="external-link" href="http://docs.katalon.com/display/KD/%5BWebUI%5D+Set+Alert+Text" rel="nofollow">Set Alert Text</a></td></tr><tr><td><a class="external-link" href="http://docs.katalon.com/display/KD/%5BWebUI%5D+Verify+Alert+Not+Present" rel="nofollow">Verify Alert Not Present</a></td></tr><tr><td><a class="external-link" href="http://docs.katalon.com/display/KD/%5BWebUI%5D+Verify+Alert+Present" rel="nofollow">Verify Alert Present</a></td></tr><tr><td><a class="external-link" href="http://docs.katalon.com/display/KD/%5BWebUI%5D+Wait+For+Alert" rel="nofollow">Wait For Alert</a></td></tr><tr><td><a class="external-link" href="http://docs.katalon.com/display/KD/%5BWebUI%5D+Select+Option+By+Value" rel="nofollow">Select Option By Value</a></td><td><p>Wrong option is selected</p><p>(<a class="external-link" href="https://github.com/MachinePublishers/jBrowserDriver/issues/148" rel="nofollow">https://github.com/MachinePublishers/jBrowserDriver/issues/148</a>)</p></td><td>Options could not be selected as expected</td></tr><tr><td><a class="external-link" href="http://docs.katalon.com/display/KD/%5BWebUI%5D+Select+Option+By+Label" rel="nofollow">Select Option By Label</a></td></tr><tr><td><a class="external-link" href="http://docs.katalon.com/display/KD/%5BWebUI%5D+Select+All+Option" rel="nofollow">Select All Options</a></td></tr><tr><td><a class="external-link" href="http://docs.katalon.com/display/KD/%5BWebUI%5D+Select+Option+By+Index" rel="nofollow">Select Option By Index</a></td></tr></tbody></table>

### Improvements

#### General

1.  Address keywords incompatible issues with Firefox 47+ (as mentioned in [Version 3.5](/display/KD/Version+3.5)).
2.  Update ChromeDriver's version to 2.25 to resolve execution issue with Chrome 54.
3.  Fix compatible issue with macOS 10 Sierra. 
4.  Several minor UX enhancements and bug fixes. 

#### Test Project

1.  Include 'JRE' settings on Preferences. Users can change to other JRE version if needed.
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-42/image2016-11-1-183A153A42.png)
2.  Add option in context menu of editors (Test Case, Test Suite, Test Suite Collection) to quickly navigate to selected test artifacts.
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-42/image2016-11-1-183A193A24.png)

#### Test Case

1.  Support defining [closure](http://groovy-lang.org/closures.html) syntax of Groovy in test case's manual.
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-42/image2016-11-1-183A243A9.png)


2.   Links to Javadoc for keywords in manual editing mode. 
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-42/image2016-11-1-183A243A45.png)


3.  Support drag and drop test objects to 'Object' field of test case
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-42/image2016-11-4-143A233A23.png)


#### Test Suite Collection

1.  Add 'Run Configuration' column to setup required information for the following execution modes:

    1.  Android
    2.  iOS
    3.  Remote Web Server

    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-42/image2016-11-1-183A323A35.png)


2.  Add 'Custom' configuration list on 'Select Environment' dialog to execute using defined custom configuration.
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-42/image2016-11-1-183A343A38.png)


3.  Support drag and drop Test Suite to Test Suite Collection
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-42/image2016-11-1-183A363A24.png)

### Known Issues

> Appium 1.6 is not supported. Besides of that, Appium has problem running tests on the latest iOS as reported at: 
>
> [https://github.com/appium/appium/issues/6857](https://github.com/appium/appium/issues/6857).
>
> This problem also affects Katalon Studio execution function on the latest iOS devices. We are working on this limitation. Meanwhile, we recommend users to use Katalon Studio on the previous version of iOS and not use Appium 1.6 for execution

## Version 4.1.0

### New Features

#### Kobiton Integration

Katalon Studio now provides Kobiton users with option to leverage their devices in Kobiton Favorited List for mobile execution. Kobiton is a clould based service for mobile testing. You can register new account for free [here](https://portal-test.kobiton.com/login).

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-41/image2016-10-3-153A483A30.png)

#### New Version Notification

Users will be informed about any **new version** when opening Katalon Studio. You can change this notification settings in **Settings -> Preferences -> Katalon.**

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-41/image2016-10-3-153A393A56.png)

### Improvements

#### General

1.  Replace test artifacts and toolbar icons.

    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-41/image2016-10-3-153A553A41.png)


2.  Update Dialog icons.

    | Infomation |  |
    | --- | --- |
    | Error | ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-41/image2016-10-3-153A593A52.png) |
    | Warning | ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-41/image2016-10-3-163A03A53.png) |

3.  Rename 'Mobile Object Inspector' into 'Mobile Object Spy' Dialog
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-41/image2016-10-3-113A353A10.png)


4.  Auto wraps text in 'Message' field of Log Viewer under Tree View
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-41/image2016-10-3-143A133A26.png)


5.  Automatically detect and install SafariDriver on macOS if it's not installed

#### Console mode

1.  Allow user to input project folder path into -projectPath argument
2.  Add –email and –password in [Console Mode Execution](/display/KD/Console+Mode+Execution) for Katalon Studio activation
3.  'Generate Command Lines for Console Mode' will create appropriated command in macOS now.

#### Test Case

1.  Add hotkey for context menu in test case's editor

*   Delete: Del
*   Copy: Ctrl-C
*   Cut: Ctrl-X
*   Paste: Ctrl-V
*   Disable: Ctrl-D
*   Enable: Ctrl-E

    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-41/image2016-10-3-123A403A8.png)

2\. Change default scripting font to be '**Courier New**' for both Windows and macOS

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-41/image2016-10-2-163A453A23.png)

#### Test Suite Collection

1.  Add context menu and hotkey for test suite collection

*   Add: Ctrl + N
*   Delete: Del
*   Move up: Ctrl + Up Arrow
*   Move down: Ctrl + Down Arrow
*   Execute: Ctrl + E
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-41/image2016-10-3-123A403A34.png)

    2\. Display warning message when executing an empty Test Suite Collection

    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-41/image2016-10-3-173A83A45.png)

    3\. Support option for parallel execution in test suite collection. Default option for execution settings will be 'Sequential' where Test Suites will be run in order.

    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-41/image2016-10-3-143A143A23.png)

#### Record/Spy

1.  Automatically select all captured objects in 'Add Element to Object Repository' dialog

    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-41/image2016-10-3-133A133A38.png)


2.  Display details regarding XPath of focused elements when recording Test Case

    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-41/image2016-10-3-123A423A55.png)

### Customer Support

1.  \[macOS\] Texts are cut off in menu tree in Preferences and Project Settings
2.  \[macOS\] Fix blurry icons and intro images on Retina display
3.  Fix NullPointerException in qTest integration

## Version 4.0.0

### New Features

#### Product Activation

Katalon now requires users to activate the application before using it.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-400/image2016-9-7-173A543A17.png)

#### Welcome Page

Add **'Welcome'** page which will be displayed everytime Katalon is started

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-400/image2016-9-7-113A373A5.png)

#### Function Introduction

Add **'Functions Introduction'** dialog which will be displayed first time after activation of Katalon

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-400/image2016-9-7-113A383A13.png)

#### Sample Projects

You now have the option to select testing type on **'New Project**' dialog. Project template with pre-defined test artifacts will be created based on which testing type you have chosen.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-400/image2016-8-28-103A63A4.png)![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-400/image2016-8-28-103A63A14.png)

#### External Libraries settings

External Libraries can now be added to Katalon through **Project -> Settings -> External Libraries**

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-400/image2016-8-28-93A503A44.png)

#### GIT Integration

Katalon Studio now support [GIT Integration](/pages/viewpage.action?pageId=2261849)

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-400/image2016-9-7-123A443A51.png)

#### Checkpoint

Add new test artifact: [Checkpoint](/pages/viewpage.action?pageId=2261817)

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-400/image2016-9-7-123A433A24.png)

### Improvements

#### General

1.  Update ChromeDriver's version to 2.23
2.  Include JRE8 into Katalon's application. You don't need to setup Java environment anymore
3.  Improve performance when opening test case
4.  Add dialog message to warn users about NodeJS and Appium if they haven't set it up properly

#### Test Explorers

Display test artifact's information when hovering mouse on it:

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-400/image2016-9-7-203A503A5.png)

#### Test Case

1.  Add **'Keyword Description'** link in Javadoc dialog. It will open [keyword's description](http://docs.katalon.com/display/KD/Keyword+Index) page with more details of how to use that keyword
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-400/image2016-8-28-93A523A28.png)
2.  Reduce code complexity in scripting mode. 

#### Settings

** 1. **Add option on 'Execution' settings to let Katalon terminate all running drivers after execution or not. Default option will be UNCHECKED

 ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-400/image2016-9-7-203A533A29.png)

2. Add default page load timeout settings in **Projects > Settings > Execution > Default > Web UI**

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-400/image2016-8-28-103A593A43.png)

#### Record/Spy

1.  **'Add'** and **'Delete'** button is added on Record dialog
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-400/image2016-8-28-93A553A52.png)


2.  **Improve Web Object Spy**
    1.  'HTML DOM' will not automatically loaded anymore.
    2.  Add hotkey **Ctrl + Alt + ~ **(default) to let you load DOM map upon pressing
    3.  Improve the display of spy's instruction
    4.  Xpath value is now displayed when you mouse hover on an object
        ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-400/image2016-8-28-103A13A47.png)



#### Mobile Object Spy

Improve 'Mobile Object Spy':

1.  1.  Objects from 'Object Repository' can now be added to 'Mobile Object Spy' through context menu: 'Add to Mobile Object Spy'. Upon adding, the object will be automatically inspected on current screen
        ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-400/image2016-8-28-123A23A5.png)
    2.  Improve the display of 'Mobile Object Spy' form
    3.  'All Objects' panel is added to display all objects of current spied mobile application's screen
    4.  Selected objects from 'All Objects' panel will be automatically added to 'Captured Objects' panel
    5.  'Device View' form is now interactable. Click on an object in 'Device View' will highlight the object back to 'All Objects' panel
    6.  Captured objects and All objects will now have indication about object's status. 
        ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-400/image2016-8-28-113A593A48.png)

### Fixed Bugs

*   \[Test Case\] Can't edit Object and Input value on manual mode when input value's type is not matched with current built-in keyword
*   \[Test Case\] 'Item' field is not highlighted with gray color as disabled step
*   \[Test Data\] After renaming an opening test data, its name on Tab pane is not changed
*   \[Test Project\] Tests Explorer tree is empty when restore Debug mode session
*   \[Keywords\] Fix execution logs of 'Select Option By Value' keyword
*   \[RunConfiguration\] Fix built-in  functions "getExecutionSource", "getExecutionSourceName", "getExecutionSourceId", "getExecutionSourceDescription" to not return null when executing test case
*   \[Test Explorers\] Test Suite Collection Reports are in ascending order in Test Explorer
*   \[Test Explorers\] Cannot copy & paste a test suite collection in a same directory
*   \[Test Execution\[Unable to execute test script using 'Remote' option
*   \[Test Execution\] Cannot execute test case using custom settings from Project -> Settings -> Execution -> Custom
*   \[Manual View\] NullPointerException when defining variable without value in Script mode
*   \[TS Collection\] Browser label and icon are overlapped when selecting browser
*   \[Mac OS\] Test case is automatically changed to display in Integration mode when users switch between 2 (or more) test cases
*   \[Manual View\] Test step description with quotation marks (" or ') or backslash (\\) is not displayed properly
*   User cannot Open/Rename/Copy/Cut/Paste/Delete/Refresh any test artifacts after open a test suite collection
*   \[Record\] Duplicate keywords in Validation Point and Synchronization Point list
*   \[Keywords\] KeywordUtil.markFailedAndStop step is displayed as FAILED step on report
*   \[Mac OS\] Black dialog while loading project
*   \[Mac OS\] Not focus on the keyword in Manual View
*   \[Web API\] Cannot use RESTful Request Parameter with POST method
*   \[Test Project\] Test object's tab is automatically closed when it's moved to another location
*   \[Object Spy\] Object spy is not working on Firefox 48+

### Other Changes

Replace** <type>SCRIPT<type>** to **<type>SCRIPT_VARIABLE</type>** in test suite (.ts) file.