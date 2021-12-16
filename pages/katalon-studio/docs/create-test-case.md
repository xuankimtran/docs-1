---
title: "Create Test Case"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/create-test-case.html
redirect_from:
    - "/display/KD/Script+View/"
    - "/display/KD/Script%20View/"
    - "/x/Y4Iw/"
    - "/katalon-studio/docs/script-view/"
    - "/katalon-studio/docs/script-view.html"
    - "/display/KD/Manual+View/"
    - "/display/KD/Manual%20View/"
    - "/x/9YEw/"
    - "/katalon-studio/docs/manual-view/"
    - "/katalon-studio/docs/manual-view.html"
    - "/display/KD/Test+Case+Manual+View/"
    - "/katalon-studio/tutorials/create_test_case_using_manual_mode.html"
    - "/katalon-studio/docs/create_test_case_using_manual_mode.html"
    - "/katalon-studio/tutorials/create_test_case_using_script_mode.html"
    - "/katalon-studio/docs/create_test_case_using_script_mode.html"
description:
---

After you create your Katalon Project, it's time to generate your very first Test Case. Katalon Studio supports Keywords-Driven testing where Test Cases consist of keywords representing actions of users on the Applications Under Test (AUT).

The Manual view allows users with less experience in programming to generate automated tests. In addition to the Manual view, Katalon Studio allows users with Groovy/Java experience to programmatically write and modify automated tests in the Script view of Test Cases.

This tutorial will guide you through creating a new Test Case, then adding your test steps in Manual and Script view with usage examples.

## Create a new Test Case

To create a new Test Case, first, open your desired Katalon Project. You can learn more about how to create projects at [Project Settings](https://docs.katalon.com/katalon-studio/docs/execution-settings.html).

On the right side of Katalon Studio, you can see the **Test Explorer** section containing access to all folders of your projects. In the **Test Explorer**, do as follows:

1. Right-click on the **Test Cases** folder, select **New > Test Case**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-case/tc-new-tc.png" alt="new test case option" width="70%">

    > Notes:
    >
    > For better management, you can also create a new folder by selecting **Test Case > New > Folder**, then create new Test Cases inside that folder.

2. The **New Test Case** dialog appears. Enter your Test Case name, description, and tag. You can organize your project more efficiently by creating relevant Test Case names, tags, and providing detailed descriptions.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-case/tc-new-test-case.png" alt="new test case dialog" width="70%">

    After you are done, click **OK**. A new Test Case is created inside the **Test Cases** folder.

    > Tags can be useful for large project management. You can learn how to manipulate tag properties at [Test Case Management With Tags](https://docs.katalon.com/katalon-studio/docs/test-case-management-with-tags.html).

2. Once a new test case is created, it is opened in **Manual** view. This view allows users to create automated tests with little programming skills required. You can switch to the **Script** tab to edit in Script view.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-case/manual-view.png" alt="manual view" width="100%">
## Generate Test Steps in Manual View

The tutorial below will give you step-by-step instructions to create test steps in Manual view.

1. In the **Manual** tab of the **Test Case Editor**, click **Add**. A new line representing a test step is generated.

2. In the newly created test step, type a keyword, or click on the dropdown button to select a keyword. Add an **Object**, **Input**, **Output**, and **Description** for that test step, if any.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-case/tc-hover.png" alt="keyword description" width="100%">

    > Notes:
    >
    > To learn more about a keyword in Katalon Studio, hover over each keyword to see its description. You can also use the search bar on our Katalon Studio documentation page to find the detailed information and usage example of each keyword.

    You can also add a **Statement** or **Call Test Case** as a test step. To learn how Statement and Call Tese Case works, see: [Statements](https://docs.katalon.com/katalon-studio/docs/statements.html) and [Call Test Case](https://docs.katalon.com/katalon-studio/docs/call-test-case.html).

4. Continue adding your test steps. You can also **Move up**, **Move down**, or **Delete** a test step.

    When you are done, in the main toolbar, click **Run** to execute the test case.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-case/run.png" alt="run" width="30%">

<details><summary><strong>Usage Example: Create a sample Test Case in Manual view</strong></summary>

In our example, we use a sample test case with the steps as below:

* Open the browser.
* Navigate to a website.
* Click on a specific control.
* Validate if a control exists on the page.
* Close the browser.

1. **Open the browser**: Select the **[Open Browser](/display/KD/%5BWebUI%5D+Open+Browser)** keyword. This keyword opens a browser and navigates to the specified URL if provided. 

    > You can view the description of a keyword by hover your mouse over that keyword.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-case/open-browser-manual.png" alt="open browser" width="100%">

2. **Navigate to a website**: Add the **[Navigate To Url](/display/KD/%5BWebUI%5D+Navigate+to+Url)** keyword. This keyword will navigate to a specified URL. Double click on the **Input** cell to provide additional data (parameters) for the keyword.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-case/tc-navigate.png" alt="navigate to url" width="100%">

    The **Input** dialog displays.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-case/tc-input.png" alt="input dialog" width="100%">

    For now, enter the URL of Katalon demo AUT ([http://demoaut.katalon.com](http://demoaut.katalon.com)) into the **Value** column, then click **OK**.

<table>
	<thead>
		<tr>
			<th>Field</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>No</td>
			<td>The number of parameter for the selected keyword.</td>
		</tr>
		<tr>
			<td>Param Name</td>
			<td>The name of the parameter.</td>
		</tr>
		<tr>
			<td>Param Type</td>
			<td>The required data type for the parameter.</td>
		</tr>
		<tr>
			<td>Value Type</td>
			<td>The type of your input value (e.g. strings, <a href="/display/KD/Variable+Types" rel="nofollow">variables</a>, <a href="/display/KD/Manage+Test+Data" rel="nofollow">data sources</a>...)</td>
		</tr>
		<tr>
			<td>Value</td>
			<td>
				<p>The input value for this parameter.</p>
				<p>The input value can be varied based on&nbsp;<strong>Value Type</strong>. Refer to&nbsp;<a href="/display/KD/Value+Types" rel="nofollow">Value Types in Katalon</a>&nbsp;for more details.</p>
			</td>
		</tr>
	</tbody>
</table>

3. **Click on a specific control**: Add the **[Click](/display/KD/%5BWebUI%5D+Click)** keyword. This keyword represents the click action on a given object. Double click on the **Object** cell and provide the object for the keyword.
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-case/click-manual.png" alt="click" width="80%">

4. **Validate if a control exists on the page**: All captured objects in **Object Repository** are displayed in the **Test Object Input** dialog. Select your object then click **OK**. To learn how to capture objects, see [Spy Object](/display/KD/Record+and+Spy+Utilities).

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-case/test-object-input.png" alt="test object input" width="80%">

    Add the **[Verify Element Present](/display/KD/%5BWebUI%5D+Verify+Element+Present)** keyword. This keyword validates if a certain object is displayed on the executing browser. Similar to the previous step, you need to specify the object to be used with this keyword.  

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-case/verify-element-present-manual.png" alt="verify element" width="100%">

5. **Close the browser**: Add the **[Close Browser](/display/KD/%5BWebUI%5D+Close+Browser)** keyword and save your test case.  

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-case/close-browser-manual.png" alt="close browser" width="80%">

</details>

### Recent Keywords

**Recent keywords** allow users to quickly add any of the last 10 recently used keywords in the **Item** list. To reuse recent keywords, in the Test Case editor, click on **Recent keywords**.
### Recent Objects and Object Folders

Katalon Studio allows users to quickly select recently used objects or jump directly to the recently used **Object Folder** in the Object Repository.

In the Object column, double-click on any Test Object to open the **Test Object Output** dialog. Here, you can see the _Recent Object_ button on the top right corner.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-case/tc-recent-object.png" alt="recent objects" width="100%">

The recent list will have two sections: **Object Folder** and **Test Object**.

* **Test Object:** Displays the names of the last 5 selected objects.
* **Object Folder:** Displays the names of 5 folders that contains any recently used objects.

## Generate Test Steps in Script view

Once a new test case is created, you can switch to the **Script view** using the corresponding tab at the bottom of the test case editor. Test steps specified in the **Manual view** are translated into a Groovy script in **Script view**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-case/script-view.png" alt="script view" width="100%">

By using the import statement in a test script, you can reference to the classes you wish to use. Expand the **import** section to see all default imported classes by Katalon Studio. The name after 'as' in each import statement is an alias for the class. You can change the alias for each class. These classes are necessary for composing a test script.

### Use Built-in Keywords in Script view

Katalon Studio is an automation tool that supports keyword-driven testing. All keywords are grouped into **[WebUI](http://docs.katalon.com/display/KD/Web+UI)**, **[Mobile](http://docs.katalon.com/display/KD/Mobile)**, and **[WebService](http://docs.katalon.com/display/KD/Web+Service)** packages accordingly. Press **Ctrl + Space** to view these packages and functions from the imported classes.

The following API docs may prove useful when working in Script view:
    
| Class | Description |
| --- | --- |
| **[Builtin Keywords](http://api-docs.katalon.com/studio/v4.6.0.2/api/com/kms/katalon/core/keyword/BuiltinKeywords.html)** | List of common built-in keywords |
| **[WebUI Builtin Keywords](http://api-docs.katalon.com/studio/v4.6.0.2/api/com/kms/katalon/core/webui/keyword/WebUiBuiltInKeywords.html)** | List of Web UI built-in keywords |
| **[Web Service Builtin Keywords](http://api-docs.katalon.com/studio/v4.6.0.2/api/com/kms/katalon/core/webservice/keyword/WSBuiltInKeywords.html)** | List of Web Service built-in keywords |
| **[Mobile Builtin Keywords](http://api-docs.katalon.com/studio/v4.6.0.2/api/com/kms/katalon/core/mobile/keyword/MobileBuiltInKeywords.html)** | List of Mobile built-in keywords |

To use a built-in keyword, type the group keyword, for example, `WebUI.` for Web UI or `WS.` for Web Service.

The **Content Assist** function will be invoked after users enter the **dot** character. **Content Assist** provides users with a context-sensitive suggestion for code completion. Therefore, all the built-in keywords for WebUI testing will be displayed as below:

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-case/webUI.png" alt="content assist" width="100%">

### Refer to an Object in Script view
    
You can find any object ID from its Properties dialog. Go to **Test Explorer > Object Repository**. Right-click on an object and choose **Properties**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-case/find-properties.png" alt="find properties" width="50%">

To refer to an object in **Object Repository**, use `findTestObject('{Object ID}')`, in which **Object ID** is the ID of that object in Katalon Studio. You can also drag and drop the object into the Test Case editor to generate this syntax.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-case/object-properties.png" alt="object properties" width="70%">

<details><summary><strong>Usage Example: Generate Test Steps in Script view</strong></summary>

In our example, we use a sample test case with the steps as below:

* Open the browser.
* Navigate to a website.
* Click on a specific control.
* Validate if a control exists on the page.
* Close the browser.

In this scenario, you will create a Web application test script to make use of the **[Web UI](/x/VQAM) [built-in keywords](/x/VQAM)**. Follow these steps to automate the above test scenario in **Script view**:

1. **Open the browser**: Type `WebUI.` and select the **[Open Browser](/display/KD/%5BWebUI%5D+Open+Browser)** keyword. This keyword opens a browser and navigates to the specified URL if it is provided. Selected keywords will have their description displayed along for reference.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-case/open-browser.png" alt="open browser" width="100%">

2. **Navigate to a website**: Enter the **[Navigate To Url](/display/KD/%5BWebUI%5D+Navigate+to+Url)** keyword. This keyword navigates to a specified URL. For now, enter the URL of Katalon Studio ([katalon.com](http://katalon.com)) as the value of the parameter.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-case/navigate.png" alt="navigate keyword" width="100%">

3. **Click on a specific control**: Enter the **[Click](/display/KD/%5BWebUI%5D+Click)** keyword. This keyword represents the click action on a given object. You need to specify an object for this action.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-case/click.png" alt="click keywords" width="100%"> 
    
4. **Validate if a control exists on the page**: Enter the **[Verify Element Present](/display/KD/%5BWebUI%5D+Verify+Element+Present)** keyword. This keyword validates if a certain object is displayed on the executing browser. Similar to the previous step, you need to specify the object to be used with this keyword.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-case/verify-element-present.png" alt="verify element" width="100%">

5. **Close the browser**: Add the **[Close Browser](/display/KD/%5BWebUI%5D+Close+Browser)** keyword and save your test case.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-case/close-browser.png" alt="close browser" width="100%">

</details>

> Learn more with our Katalon Academy course: [Create and Execute Test Cases](https://academy.katalon.com/courses/create-execute-test-cases/?utm_source=kat_docs_create&utm_medium=bottom_link&utm_campaign=academy_promotion).
