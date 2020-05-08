---
title: "Windows Spy Tutorials"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/windows-spy-tutorials.html
---
> Starting in **Katalon Studio version 7.0**, you can spy objects on a Windows desktop application.

1. To start capturing test objects on a Desktop application, Click the **Spy Windows Object** icon on the main toolbar of Katalon Studio.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/introduction-desktop-app-testing/Spy_Windows_Object.png" width="549" height="61.5">

2. The Spy Windows Objects dialog box is displayed. Specify the information at the **CONFIGURATIONS** section.

* **Configuration**: where you can view and edit the `WinAppDriver URL` and `Desired Capabilities`.

* **Application File**: the absolute path to the `Windows Executable File (*.exe)` of the testing machine. For Windows users, click **Browse...** button to locate the application file.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/spy-windows-object/spy2.png" width="397" height="142">

    The **Start** button is enabled after the Application File text box is filled.

    Click **Start** when you're done with the settings.

4. The specified Windows application is deployed and opened on a testing machine.

5. The **Screen View** dialog box is displayed to show the current screenshot of your application on the testing machine.

    All the Windows objects in that screenshot are analyzed and organized in a tree at the **Screen Objects** section.

    Click on any object in that tree and it's highlighted in the Screen View accordingly.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/spy-windows-object/spy-highlight.png">

6. Select any objects in the tree by checking on the checkboxes on the left of an intended element to add it to the Object Repository. The selected object is displayed in the **Captured Objects** Section. You're recommended to rename objects in the **Object Properties** Section.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/spy-windows-object/highlight-spy.png" width="747" height="694">

    Here you can customize the locator of a captured object by modifying it in the Locator tab of **Object Properties** and clicking **Highlight** to verify if the new locator correctly identifies the intended object on **Screen View**.

7. All of the selected objects above are captured at the **Captured Objects** section.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/spy-windows-object/spy-step7.png" width="187" height="197">

8. You can stop the application or start another application if needed. To reload the Screen View as well as the details in Spy Desktop Utility, simply click on the **Refresh Screen** button.\
When you’re done with spying, click **Add to Object Repository** to save the captured objects in Katalon Studio.

9. You will be prompted to save the captured objects in the Object Repository of Katalon Studio. Select a preferred location, then click **OK** to continue.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/spy-windows-object/spy-objectrepo.png" width="393" height="392">

10. The captured objects are added to the preferred Object Repository Folder accordingly.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/spy-windows-object/saved-objects.png" width="332" height="167">

11. Click **OK** at the bottom of the dialog box to finish your spying session.

    >**Notes**:
    >
    > 1. Remember not to lock your screen while spying, spying or executing a test on a desktop application.
    > 2. You're recommended not to run multiple applications simultaneously.
    > 3. To start UWP application, the application's execute file should be:
    > 
    > * ApplicationID if your app is published on Microsoft store
    > * PackageFamilyName!Application ID if your app is still in development.
