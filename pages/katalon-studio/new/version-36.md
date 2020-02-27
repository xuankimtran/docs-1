---
title: "Version 3.x"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/new/version-36.html
redirect_from:
    - "/display/KD/Version+3.6/"
    - "/display/KD/Version%203.6/"
    - "/x/LIcY/"
    - "/katalon-studio/new/version-36/"
    - "/katalon-studio/new/version-35.html"
    - "/display/KD/Version+3.5/"
    - "/display/KD/Version%203.5/"
    - "/x/nIYY/"
    - "/katalon-studio/new/version-35/"
    - "/katalon-studio/new/version-33.html"
    - "/display/KD/Version+3.3/"
    - "/display/KD/Version%203.3/"
    - "/x/DoUY/"
    - "/katalon-studio/new/version-33/"
    - "/katalon-studio/new/version-320.html"
    - "/display/KD/Version+3.2.0/"
    - "/display/KD/Version%203.2.0/"
    - "/x/XoIY/"
    - "/katalon-studio/new/version-320/"
    - "/katalon-studio/new/version-31.html"
    - "/display/KD/Version+3.1/"
    - "/display/KD/Version%203.1/"
    - "/x/aYEY/"
    - "/katalon-studio/new/version-31/"
description:
---

## Version 3.6.0

### Improvements

#### General

*   Add hotkeys on context menu of test artifacts in Test Explorers
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-36/image2016-7-26-143A373A39.png)


*   Allow users to cancel progressing tasks on 'Loading Logs' dialog
*   \[Preference\] Expose more options of Native Eclipse Preference in Settings -> Preferences
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-36/image2016-7-26-143A383A10.png)

#### New MOBILE  built-in keywords

| No. | Name | Description |
| --- | --- | --- |
| 1 | Select Item in List by Index | Select item of list view control by its index. Have not implemented for Android because its list view is async loaded |
| 2 | Select Item in List by Label | Select item of list view control by its label. |
| 3 | Pinch to Zoom In by Position | Pinch to zoom in at a specific position on the screen of the mobile device |
| 4 | Pinch to Zoom Out by Position | Pinch to zoom out at a specific position on the screen of the mobile device |
| 5 | Tap At Position | Tap at a specific position on the screen of the mobile device |
| 6 | Get Element Top Position | Get the top position of mobile element |
|  7 | Get Element Left Position | Get the left position of mobile element |
| 8  | Get Element Width | Get the width of mobile element |
| 9 | Get Element Height | Get the height of mobile element |
| 10 | Long Press | Tap and hold at a specific position on the screen of the mobile device |
| 11 | Set Slider Value | Set the value for Slider control (android.widget.SeekBar for Android, UIASlider for iOS) at specific percentage |
| 12 | Unlock Screen | Unlock device scree |

#### Object Spy

*   Users can now do object spy on Firefox which is already being opened through [Katalon Object Spy](https://addons.mozilla.org/en-US/firefox/addon/katalon-object-spy/?src=api) add-on
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-36/image2016-7-26-143A403A42.png)
*   Improve mobile object spy
    *   Correct highlight on captured object
    *   Generate Xpath value
        ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-36/image2016-7-26-143A443A31.png)

#### Test Data

*   Improve UX of Internal Data:
    *   Select will now focus on single cell instead of full row
    *   Press 'Enter' key will enter or exit edit mode
    *   Press 'Tab' key will move to next cell, 'Shift Tab' will move to previous cell

#### Mobility

*   Add loading progress bar when 'Mobile Object Spy' dialog is loading
*   Add ability to specify log level for appium execution in Preference setting
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-36/image2016-7-26-153A383A41.png)
*   Support execution on mobile emulator
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-36/image2016-7-26-153A393A21.png)

### Fixed Bugs

*   \[Studio - Record\] Stop button is cut-off and disappeared when user drag mouse on it and maximize Record window
*   Fix 'Resume' icon on 'Record' window which its layout is broken
*   \[Manual View\] ELSE IF Statement icon and statement number are overlapped
*   \[Test Case\] 'Test Object' input is not shown in 'Input' form in case keyword used 'test object' input
*   A part of tab bar is cut off after opening and closing Job Progress
*   \[Test Data\] Excel data grid does not display data properly when checking "Use first row as header"
*   \[Explorer\] Some object names are cut off when opening Katalon
*   Fix test case's status counting in 'Log Viewer' for test suite collection execution
*   \[Log Viewer\] Incorrect test suite collection execution logs when executing test suite with no test cases are run
*   \[Test Data\] Excel data grid does not display properly

## Version 3.5.0

### Notes

Selenium 2.53.0 is not compatible with Firefox 47+ (more info [here](https://github.com/SeleniumHQ/selenium/issues/2110) and [here](https://github.com/SeleniumHQ/selenium/issues/1862) ). This release adds [Marionette driver](https://developer.mozilla.org/en-US/docs/Mozilla/QA/Marionette/WebDriver) to Katalon to fix issues when using Firefox 47+ and Selenium 2.53.0 for execution. However, we suggest Firefox 45 or 46 for stable execution.

### Improvements

#### General

*   Add settings to enable/disable 'Screen Capture' when executed steps failed. You can access this settings at _**Project > Settings > Report**_
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-35/image2016-6-16-143A553A39.png)


*   Display 'Splash Screen' and 'Loading Progress Bar' when starting Katalon
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-35/image2016-6-16-143A553A9.png)



#### Data Files

*   Support 'Database Data' as a new test data type. You can set default database settings through **_Project > Settings > Database_**
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-35/image2016-6-16-143A593A37.png)



#### New mobile keywords

| No. | Keyword's name | Description |
| --- | --- | --- |
| 1 | Tap And Hold | Tap and hold on a mobile element for a duration |
| 2 | Check Element | Check a check-box mobile element (android.widget.checkbox for Android, UIASwitch for iOS) |
| 3 | Uncheck Element | Unheck a check-box mobile element (android.widget.checkbox for Android, UIASwitch for iOS) |
| 4 | Hide Keyboard | Hide a keyboard if it is showing |
| 5 | Verify Element Checked | Verify if a mobile element is checked |
| 6 | Verify Element Not Checked | Verify of a mobile element is not checked |
| 7 | Drag and Drop | Drag and drop an element into another element |

#### Record/Playback

*   Record and Object Spy now can be used on current opened Chrome browsers. Users need to install Katalon's [Record](https://chrome.google.com/webstore/detail/katalon-recorder/bnaalgpdhfjepeanejkicnidgbpbmkhh?hl=en-US) and [Object Spy](https://chrome.google.com/webstore/detail/katalon-object-spy/gblkfilmbkbkjgpcoihaeghdindcanom?hl=en-US) extension on Chrome first in order to utilize this feature.![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-35/image2016-6-17-173A183A24.png)



#### Mobility

*   Improve UX by relocating 'Device View' window to be next to 'Mobile Object Inspector' window (instead of displaying one on top of the other in previous versions)
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-35/image2016-6-16-143A573A11.png)



#### Test Case

*   Hide FailureHandling value when users add new test step using built-in keyword. You can configure it through _**Project > Settings > Test Case > Default FailureHandling for Test Step**_
    _**![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-35/image2016-6-16-143A573A45.png)**_


#### Test Suite

*   Support the ability to execute multiple test suites using 'Test Suites Collection'
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-35/image2016-6-16-143A593A3.png)



#### Execution

Execution on IE will now generate IEDriverServer logs


### Fixed Bugs

*   KAT-845 Fix bug with using statement without surrounding code with brackets in Script Mode

*   KAT-870 Tests Explorer tree is not expanded after reopening Katalon with a saved session

*   KAT-874 Keyword's description is not displayed when hovered on in Keyword Browser

*   KAT-877 \[Mobile Keyword\] Application is closed unexpectedly when user runs Mobile keyword (Start Application, Set Text...

*   KAT-912 'Number' option is not shown for 'Object' param type in Input form

*   KAT-918 \[Generate Command\] Lack of "reportFolder" option when user saves report in default folder and don't use relative path

*   KAT-920 \[Command Line\] Cannot execute test suite when user indicates a different report folder using absolute path to the project

*   KAT-926 Can't get specific attribute's value using 'getAttribute' keyword

*   KAT-949 'Device Name' settings is not stored after changed on 'Project Settings' form

*   KAT-915 Remove redundant tooltips in 'Global Variable' view and 'Test Case' Manual view

*   KAT-847 Generated scripts from recording sessions will automatically import all default packages in Script mode


### Customer Requests

 \[CoreInformatics\] Fix issue with executing test scripts using enum in console mode

## Version 3.3.0

### Improvements

#### General

*   Add the ability to debug a test script
*   Update test artifacts by using properties dialog (Right Click -> Properties)

#### Mobility

*   Simplified mobile testing setup
*   Add settings for config external APPIUM libraries

#### Test Case

*   Ability to mark steps as disabled in Manual View

#### Execution

*   Add 'chrome' executable driver to Katalon's MAC version
*   Support external libraries in Console mode

#### Reports/ Logs

*   Add Katalon's version in execution logs and reports
*   Add step number for child steps in setUp and tearDown methods

### Fixed Bugs

*   Fixed an issue when users switching between running jobs will make the execution logs can't be loaded
*   Fixed test case's status under specific case
*   Fixed test steps' count on execution logs when running setUp and tearDown methods

### Customer Requests

*   \[Core Informatics\] Support the ability to update browser's preferences directly in test script
*   \[Nexidia\]  - 'import static' script will be kept when users save edited changes on manual mode
*   \[Nexidia\] - 'Progress Information' is struck when users rename test entities using rename dialog

## Version 3.2.0

### Improvements

#### General

*   The Default Browser for execution will be displayed with an indication
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-320/image2016-4-6-123A153A58.png)
*   Have options to let users open the previous working session when opening Katalon
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-320/image2016-4-6-123A103A5.png)
*   Automatically generate destination project's folder in case it's not existed yet when creating new Katalon Projects
*   Support loading **.app** file on Mobile Object Spy (for iOS platform)
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-320/image2016-4-6-123A293A14.png)
*   Automatically focus into first field of some UI components:
    *   In Global Variables, focus on Name field of Add/Edit Variable Dialogs
        ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-320/image2016-4-6-123A143A15.png)
    *   In Variable tab of Test Case editor, focus on Name field when adding new Variables 
        ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-320/image2016-4-6-123A143A47.png)

#### Console mode

*   Allow users to generate command to run in console mode
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-320/image2016-4-6-123A223A48.png)
*   Support the ability to auto send mail function parameters
*   Revamp argument processing for console mode: [Console Mode Execution](/display/KD/Console+Mode+Execution)

#### Execution

*   \[Infrastructure\] Revamp execution engine
*   Change mechanism to support executing test script upon current active Chrome & Firefox browsers


#### Report

*   Display 'Warning' filter in Katalon's generated report
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-320/image2016-4-6-123A353A1.png)

#### Object Spy

*   \[Mobile Object Spy\] Support "Object Name" field in MOI
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-320/object_name.png)

#### Test Case

*   Refactor getTestCaseBindingString method

#### Record/Playback

*   \[Record\] Add tooltip for recorded actions
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-320/image2016-4-6-123A383A25.png)

#### qTest Integration

*   \[Console Mode\] 'qTest' logs will not be displayed if the test project has no integration with qTest

### Fixed Bugs

*   \[Mobile\] MOI gets "Not Response" when started without application file
*   \[MOI\] MOI got frozen when users select captured objects on the view
*   System can't execute test scripts if executed browser is Firefox 45.0.1
*   System can't record steps if recorded objects are refreshed
*   Error when 'Take Screenshot' keyword is used
*   \[Test Suite\] Can't execute test suite if selected platform's preferences value used machine's path
*   Correct default generated value to use proper value based on input's value type
*   Global Variable value is kept as original when users changed value in custom keyword script

### Customer Requests

*   \[Core Informatics\] Change default values for 'Send attachment' settings & memory size of katalon.ini file
*   \[Core Informatics\] Improve performance on 'select Option By ' keyword without using regular expression
*   \[Core Informatics\] Create HTMLTableData based on TestData to support reading HTML content-based file
*   \[Core Informatics\] Add new 'Warning' filter level in 'Log Viewer' panel

## Version 3.1.0

### Improvements

#### General

*   Use natural naming convention for objects
*   Remember last opened session 
*   Automatically focus on first field in Search popup

#### New built-in keywords

*   "verifyElementClickable"

#### Execution

*   \[Console Mode\] - Support the option to '-retryFailedTestCases=<true, false>' 

#### Object Spy

*   Improve 'Add Element to Object Repository' form 
*   Display relevant message when there is no searched result in 'HTML DOM' field

#### Test Case

*   Display javadoc when user select a keyword in combo box in manual mode
*   Empty description is removed automatically when users switch to 'Script' view
*   Improve performance on test case's editor

#### Record/Playback

*   Abilities to edit/remove action during Recording
*   Abilities to edit/remove captured objects during Recording

#### qTest Integration

*   Add option to allow uploading test runs to latest approved test case's version of qTest

### Fixed Bugs

*   \[Test Suite\] System didn't allow users to save modified test suite in case different test suite's types are saved in test project
*   \[Test Project\] Users can create new folder under 'Reports' section
*   \[Log Viewer\] System didn't display correct test step's status counts in case teardown method is used
*   \[Console mode\] Auto disable dialog shown in case execution's status is different with passed
*   \[Test Case\] Users can't drag and drop a test step to replace FIRST test step
*   \[Test Case\] Object's value is displayed as null when users select defined variable as an object
*   \[Test Case\] Users can't edit fields on 'Input' form in case number value is left as blank value
*   \[Keyword\] Correct 'Take Screen Shot' keyword's name
*   \[Keyword\] Add Javadoc for 'Verify Match' keyword on manual mode and keywords browser form
*   \[Test Case\] System display error message when a test step is drag and dropped into blank areas
*   \[Test Suite\] 'Variable Binding' settings is reset to default binding when a new variable is defined for current test case
*   \[Test Execution\] Can't start execution on Firefox if Firefox profile settings are used
*   \[Test Case\] 'Modify Object Property' javadoc's keyword can't be displayed using combo box in manual mode
*   \[Test Project\] System displayed error message when drag and drop root folder to its location
*   \[Record/Playback\] System can't generate test steps in case element's field is blank for validation/sync action
*   \[Record/Playback\] Error message is displayed when 'property' value's type is selected on action without element

### Customer Requests

*   \[CoreInformatics\] Adjust qTest Integrate API to update to latest version
*   \[Care Logistics\] Investigate issue of crashed execution with lengthy suites