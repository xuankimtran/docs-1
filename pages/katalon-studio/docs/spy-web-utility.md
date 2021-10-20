---
title: "Spy Web Utility" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/spy-web-utility.html 
redirect_from:
    - "/display/KD/Spy+Web+Utility/"
    - "/display/KD/Spy%20Web%20Utility/"
    - "/x/5BZO/"
    - "/katalon-studio/docs/spy-web-utility/"
    - "/x/jwBO/"
    - "/katalon-studio/docs/spy-web-utility-version-48-and-below/"
    - "/katalon-studio/docs/spy-web-utility-version-48-and-below.html"
description: 
---

Spy Web Utility offers an intelligent object capturing capability in web testing. With the utility, you can flexibly capture test objects by specifying several properties and locating methods.

This guide shows you how to use Spy Web Utility to capture and manually define test objects.

## Capture objects using Spy Web Utility

1. To open the Spy Web Utility, from the main toolbar, click on the **Spy Web** button.  

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/spy-web-utility/KS-Spy-Web-Utility-toolbar.png" width=70% alt="Spy Web Utility on toolbar">

2. In the displayed **Object Spy** dialog, specify the URL of the AUT and the web browser. Click on the **Start** button to start capturing.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/spy-web-utility/KS-Object-Spy-dialog.png" width=70% alt="New Object Spy dialog">

      Here you have two options for web browsers: **New Browsers** and **Active Browsers**.

   <table>
  <thead>
    <tr>
      <th>Type</th>
      <th>Description</th>
      <th>Note</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>New Browsers</td>
      <td>
        Start a new browser and start spying web objects from that browser.
      </td>
      <td>
        <strong>Supported browsers:</strong><br />- Firefox<br />- Chrome<br />-
        Internet Explorer (only on Windows)
      </td>
    </tr>
    <tr>
      <td>Active Browsers</td>
      <td>
        Focus on <strong>the current active Chrome browser</strong> and start
        spying web objects from it.
      </td>
      <td>
        Katalon Studio will install
        <a
          class="external-link"
          href="https://chrome.google.com/webstore/detail/katalon-recorder-selenium/ljdobmomdgdljniojadhoplhkpialdid"
          rel="nofollow"
          >Katalon Recorder</a
        >
        as an add-on to help with recording for this type of browser<br /><br /><strong
          >Supported browsers:</strong
        ><br />- Chrome<br />- Firefox (coming soon)
        <p>You will be asked for installation of <em>Katalon Utility</em>:</p>
        <p>
          <img
            src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/spy-web-utility/KS-Object-Spy-Active-browsers-extension.png"
            width="70%"
            alt="Add extension dialog"
          />
        </p>
        <p>
          Refer to
          <a href="https://docs.katalon.com/katalon-studio/docs/katalon-addon-for-chrome.html"
            >Katalon Addon for Chrome</a
          >
          for more details.
        </p>
      </td>
    </tr>
   </tbody>
   </table>
    
3. Katalon Studio launches the selected browser. Hover the mouse cursor over the web element to be captured.  

    Spy Web Utility highlights the web object with a red border. An overlay pane is also displayed at the top edge of the screen to show relevant **XPath** info.  
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/spy-web-utility/KS-Web-Spy-highlighted-element.png" width=70% alt="Web Spy highlights element"> 
      
    
4.  Press the combination of **\<Alt + \`\>** keys on the keyboard to capture the object. For macOS users, right-click on the element and select **Capture Object**. 

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/spy-web-utility/KS-Web-Spy-Capture-Object.png" width=70% alt="Capture element"> 
      
    
5.  Captured objects appear in the **Object Spy** dialog.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/spy-web-utility/KS-Object-Spy-captured-object.png" width=70% alt="Captured object">  

    
6.  Select the object in the **Captured Objects** tree; the utility displays its details in the **Object Properties** section.

      <table>
  <thead>
    <tr>
      <th>Type</th>
      <th colspan="2">Descriptions</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="5"><strong>Selection Method</strong></td>
      <td colspan="2">The method which Katalon Studio will be using to detect web elements.</td>
    </tr>
    <tr>
      <td><strong>Options</strong></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>Attributes</strong></td>
      <td>Katalon Studio automatically generate an XPath combine with objects' properties.</td>
    </tr>
    <tr>
      <td><strong>XPath</strong></td>
      <td>Katalon Studio <strong>Relative XPath</strong>. If an element cannot be consistently located using its direct attributes, Katalon Studio will identify by using its more robust neighbors.</td>
    </tr>
    <tr>
      <td><strong>XPath</strong></td>
      <td>Users are allowed to input CSS selector manually into Object Detect Editor.</td>
    </tr>
    <tr>
      <td><strong>Properties Grid</strong></td>
      <td colspan="2">All the captured properties of the selected object. You can edit the value of any property.</td>
    </tr>  
    <tr>
      <td rowspan="4"><strong>Selector Editor</strong></td>
      <td colspan="2">Display object locator based on selected method</td>
    </tr>
    <tr>
      <td><strong>Options</strong></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>Basic or XPath</strong></td>
      <td>Katalon Studio generated XPath will be displayed.</td>
    </tr>
    <tr>
      <td><strong>CSS</strong></td>
      <td>Editable text field allows users to manually input object's locator.</td>
    </tr>
  </tbody>
</table>

> To learn more about object selection methods, refer to this document: [Selection Method](https://docs.katalon.com/katalon-studio/docs/working-with-objects-selection-method-for-spyrecord-web.html).
 
7. Click on the **Save** button to add captured objects to **Object Repository**.

8. Check on those captured objects in the left pane that you would like to save into Katalon Studio.   

    The structure of your **Object Repository** is displayed on the right pane. Select the folder to add the captured objects. Click **OK** when done.  

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/spy-web-utility/KS-Add-element-to-object-repository.png" width=70% alt="Add Element to object repository">   
      
    
9. The captured objects are added to **Object Repository** accordingly.

## Define additional objects manually

1. **Add a Page element**: Web objects need a web page to hold them. Click on the **New page** button from the toolbar to add a new Page element manually.  

2. **Add a Frame element**: If the new object is a nested object, a frame is needed to locate the element. Frames are web elements that usually contain many other web objects.
    
    
3.  **Add an Object element**: Click on the **New object** button from the toolbar to manually add a web object. Click **Delete** to remove any unwanted element.
    
4.  In **Object Properties** section, provide **Object Name** for the recently added object, choose **Selection Method** options and specify **properties** for the new web object.

      Here we define a button element using the **Attributes** selection method. The chosen properties are **tag** and **id**.

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/spy-web-utility/KS-Object-Spy-New-Object.png" width=70% alt="Add Element to object repository">  
    
5.  Click **Verify and Highlight** to ensure Katalon Studio can locate the object.

    If there is a web object with matched **Selector Editor** value, it is highlighted **red** in the opened browser, and the message **" Found X element using XPath Selector"** is displayed.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/spy-web-utility/KS-Object-Spy-verify-object.png" width=70% alt="Verify object"> 
    
6.  Once finished, click **Save** to add the object to **Object Repository** as normal.
    

## Get web object XPath or CSS locator

1.  In the open spying browser, right-click on the target web element and select **Inspect**.


    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/spy-web-utility/KS-Web-element-right-click.png" width=70% alt="Right-click on web element"> 


2.  In the inspector window, the selected element is highlighted, indicating the target element's location in the HTML DOM. Right-click on the highlighted line and select **Copy > Copy XPath** or **Copy Selector**.


    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/spy-web-utility/KS-Web-element-copy-XPath.png" width=70% alt="Copy XPath">   
      
    
3. Navigate to the **Object Spy** window and paste into **Selected Locator** or **Object Properties** section.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/spy-web-utility/KS-Object-Spy-paste-XPath.png" width=70% alt="Paste XPath into Selected Locator section">  
    
4. Click the **Verify and Highlight** button to check if Katalon Studio can locate the object.  

5. Once finished, click **Save** to add the object to **Object Repository** as normal.

**See also**:

* [Working with Object Properties](https://docs.katalon.com/katalon-studio/docs/manage-web-test-object.html)
* [Object Identification Best Practices](https://docs.katalon.com/katalon-studio/docs/optimizing-object-identification-and-tools.html)
* [Configure Web Object Locators Settings](https://docs.katalon.com/katalon-studio/docs/web-locators-settings-since-v571.html)