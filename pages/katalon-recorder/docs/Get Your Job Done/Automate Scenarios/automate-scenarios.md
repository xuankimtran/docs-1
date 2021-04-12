---
title: "Basics of automating scenarios"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-recorder/docs/automate-scenarios.html
description:
---

Automating a scenario in KR is essentially adding actions, either through recording or manually.

## Automate your first scenario

### 1/ Start recording

Once the extension is opened, open https://www.airbnb.com/ to automate booking a place to stay. Minimize and position the window in a way that allows you to see what's going on with KR. Click on the button with the red circle to start a recording session.

![](https://raw.githubusercontent.com/katalon-studio/docs-images/master/katalon-recorder/docs/jtbd/automate-scenarios/image1.png)

Start interacting with the website. Perform any activity like you would normally do. The interactions will be recorded in KR.

![](https://raw.githubusercontent.com/katalon-studio/docs-images/master/katalon-recorder/docs/jtbd/automate-scenarios/image2.png)

### 2/ Use context menu to add actions

Right-clicking on any element, select _Katalon Recorder (Selenium tests generator) \> waitForElementPresent_. This adds the step _waitForElementPresent_ with the value being the locator of the selected element.

![](https://raw.githubusercontent.com/katalon-studio/docs-images/master/katalon-recorder/docs/jtbd/automate-scenarios/image3.png)

### 3/ Rename your test for better readability

Click on the _Stop_ button.Rename your test case by right clicking on the test case and choose _Rename Test Case._

![](https://raw.githubusercontent.com/katalon-studio/docs-images/master/katalon-recorder/docs/jtbd/automate-scenarios/image4.png)

### 4/ Save your test case/test suite

Right click on the Test Suite and choose _Save Test Suite as_, KR will save your test suite, along with the test cases, into a HTML file.

---

## Add actions to a scenario

After recording a scenario, you may choose to extend it by adding actions manually.

### 1/ Add a new step

Click on the button with the _Plus icon._

![](https://raw.githubusercontent.com/katalon-studio/docs-images/master/katalon-recorder/docs/jtbd/automate-scenarios/image5.png)

### 2/ Specify an action

Click on the _down arrow_ next to the command input and choose a desired action.

![](https://raw.githubusercontent.com/katalon-studio/docs-images/master/katalon-recorder/docs/jtbd/automate-scenarios/image6.png)

### 3/ Read how to use the action & parameters

Click on _Reference_ tab at the bottom panel. Then click on each action to see the documentation.

![](https://raw.githubusercontent.com/katalon-studio/docs-images/master/katalon-recorder/docs/jtbd/automate-scenarios/image7.png)

---
## Save data
From 5.3.31, users can quickly save changes made to test cases via shortcuts `ctrl + s` or right-click on a test case and choose **Save Test Case**.

## Remove data
### Delete operations

![](https://raw.githubusercontent.com/katalon-studio/docs-images/master/katalon-recorder/docs/jtbd/automate-scenarios/image8.png)

From 5.3.31, KR implement some UX enhancements to help users more aware before removing data.

Specifically, the following operations are changed from:
- **Remove test case** to **Remove Test Case from Workspace**.
- **Close Test Suite** to **Remove Test Suite from Workspace**.
- **Close All Test Suites to** to **Remove all Test Suites from Workspace**.
- **Save Test Suite as** to **Save Test Suite to Computer**.

### Remove test suite
![](https://raw.githubusercontent.com/katalon-studio/docs-images/master/katalon-recorder/docs/jtbd/automate-scenarios/image9.png)

![](https://raw.githubusercontent.com/katalon-studio/docs-images/master/katalon-recorder/docs/jtbd/automate-scenarios/image11.png)

### Remove test case
![](https://raw.githubusercontent.com/katalon-studio/docs-images/master/katalon-recorder/docs/jtbd/automate-scenarios/image10.png)

![](https://raw.githubusercontent.com/katalon-studio/docs-images/master/katalon-recorder/docs/jtbd/automate-scenarios/image12.png)