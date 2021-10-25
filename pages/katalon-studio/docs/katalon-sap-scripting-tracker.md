---
title: "Combine Katalon Studio with SAP Scripting Tracker for Windows" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/katalon-sap-scripting-tracker.html 
redirect_from:
description: 
---

Scripting Tracker is a utility and a replacement to the SAP GUI Scripting Development Tools. It is an SAP GUI analyzer and recorder on the SAP GUI Scripting base. You can learn more about SAP Scripting Tracker in the SAP blog post here: [Scripting Tracker – Development Tool for SAP GUI Scripting](https://blogs.sap.com/2014/11/20/scripting-tracker-development-tool-for-sap-gui-scripting/).

This tutorial demonstrates how to combine Katalon Studio with SAP Scripting Tracker for Windows. 

> Requirements:
> * Katalon Studio version 7.0.0 onwards.
> * WinAppDriver version 1.1.0 onwards. To learn more about setting up WinAppDriver, you can refer to this document: [Set up WinAppDriver](https://docs.katalon.com/katalon-studio/docs/setup-winappdriver.html#set-up-windows-application-driver-on-a-local-windows-10-machine).
> * SAP Scripting Tracker version 3.15 onwards. You can download the SAP Scripting Tracker from the Scripting Tracker website: [Scripting Tracker](https://tracker.stschnell.de/#).

## Enable SAP GUI Scripting in SAP

To enable SAP scripting mode, you can refer to the SAP document here: [Enabling Scripting on the Server Side](https://help.sap.com/viewer/8ecea00c1f854fd0a433c4aef5da1ea2/Cloud/en-US/001675913cc54719930aa8197478dcde.html).

## Implement the Java code recording for SAP Scripting Tracker

Katalon can only read Java language generated from SAP Scripting Tracker. To use SAP GUI Scripting in the context of Java you need the Java COM Bridge (JACOB). You can download and install Java COM Bridge (JACOB) from the Github repository: [Java COM Bridge (JACOB)](https://sourceforge.net/projects/jacob-project/).

## Build your test case
### Download our sample Katalon SAP GUI project

This sample project provides you with code samples, custom keywords, and sample test cases that give you the necessary preparations to automate your test script with SAP Scripting Tracker.

You can download the sample project here at our Github repository: [Katalon SAP GUI sample project](https://github.com/katalon-studio-samples/kat-sap-gui-sample-test).
### Add your login account to the test case

1. After downloading our sample project, from the **Test Explorer** panel, open **Profiles > default**.     

2. Double-click the **Value** cell of the **username** and **password** variables.  
   
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/katalon-sap-scripting-tracker/KS-SAP-Open-the-default-file.png" width="70%" alt="Open the default file">

3. In the opened **Edit variables** dialog, change the sample value to your SAP account.
   
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/katalon-sap-scripting-tracker/KS-SAP-Fill-in-your-username.png" width="70%" alt="Fill in your username">

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/katalon-sap-scripting-tracker/KS-SAP-Fill-in-ur-password.png" width="70%" alt="Fill in your password">
### Create a new test case based on the sample project

1. Create a new test case. Go to **File > New > Test Case**.
2. From the **Test Explorer** panel of our sample project, go to **Test Cases > Common** folder. There are 3 sample test cases as follows:

    <table width="846">
    <tbody>
    <tr>
    <td><strong>StartSAPLogon</strong></td>
    <td>This sample test case starts SAP Logon, then goes to the sign-in section.</td>
    </tr>
    <tr>
    <td><strong>Login</strong></td>
    <td>This sample test case starts an SAP session then uses the <strong>username</strong> and <strong>password</strong> variables to login</td>
    </tr>
    <tr>
    <td><strong>TestCaseTemplate</strong></td>
    <td>This sample test case calls the <strong>StartSAPLogon</strong> and <strong>Login</strong> test cases, then enables Katalon to read the SAP Scripting Tracker script.</td>
    </tr>
    </tbody>
    </table>

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/katalon-sap-scripting-tracker/KS-SAP-3-sample-test-cases.png" width="70%" alt="3 sample test cases">

3. Open the **Script** tab of the **TestCaseTemplate** test case, copy the content and paste it into the **Script** tab of the new test case created from step 1.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/katalon-sap-scripting-tracker/KS-SAP-Copy-the-test-script-in-the-TestCaseTemplate-sample.png" width="70%" alt="Copy the test script in the TestCaseTemplate sample test">
    
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/katalon-sap-scripting-tracker/KS-SAP-Paste-the-test-script-into-the-new-test-case.png" width="70%" alt="Paste the test script into the new test case">
### Record test script using SAP Scripting Tracker

1. Start SAP Logon and sign in SAP GUI with your SAP account.
   
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/katalon-sap-scripting-tracker/KS-SAP-Start-SAPLogon.png" width="70%" alt="Start SAPLogon">

2. After signing in, open SAP Scripting Tracker. Click **Refresh**, then select the current SAP session.
   
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/katalon-sap-scripting-tracker/KS-SAP-select-SAP-session.png" width="70%" alt="Select the SAP session">

3. Choose Java language, then click **Record** to start recording your SAP GUI script. 
   
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/katalon-sap-scripting-tracker/KS-SAP-Choose-Java-language.png" width="70%" alt=" Choose Java ">
   
    Here, we record the following scenario:

    - In the opened SAP GUI session, go to **SAP Menu > Human Resources**. Double-click on **PPMDT - Manager's Desktop**. The **Manager's Desktop** interface opens.
    - Double-click on **Personal Data** to open the folder.
    - Navigate to **Reports > Employee data**, then click **Maternity**.

    We stop recording here.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/katalon-sap-scripting-tracker/ezgif.com-gif-maker.gif" width="70%" alt="Recording from Scripting Tracker">

4. After finishing your recording, copy and paste the content from Scripting Tracker into your Katalon test script.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/katalon-sap-scripting-tracker/KS-SAP-Copy-the-script-from-Scripting-Tracker.png" width="70%" alt="Copy the script from Scripting Tracker">

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/katalon-sap-scripting-tracker/KS-SAP-Paste-after-pasting-the-script-into-Katalon.png" width="70%" alt="Paste the script into the Katalon test script">

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/katalon-sap-scripting-tracker/KS-SAP-Final-results.png" width="70%" alt="Results after pasting the script into the Katalon test script">
### Run the test script

To run the recorded test script, on the main toolbar, select **Windows** in the dropdown list next to **Run**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/katalon-sap-scripting-tracker/KS-SAP-Run-the-test.png" width="30%" alt="Run the test">

Katalon will automatically sign in SAP GUI with your SAP account and playback the recorded steps from Scripting Tracker.