---
title: "iOS sample project"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/iOS-sample-prj.html
---

This sample demonstrates fundamental iOS testing in Katalon Studio.

The Application Under Test (AUT) is the `Coffee Timer` application. You can learn more about mobile testing in this document: [Introduction to mobile testing](https://docs.katalon.com/katalon-studio/docs/katalon_mobile_recorder_introduction.html#mobile-recorder).

> Requirements:
> * iOS setup. To set up Xcode simulators/ real iOS devices, you can refer to this document: [[Mobile] iOS Setup](https://docs.katalon.com/katalon-studio/tutorials/mobile-ios-setup.html#part-1-setting-up-the-environment-for-ios-testing).

## Open the sample iOS test project

To open the iOS sample project, in Katalon Studio, go to **File > New Sample Project > Sample iOS Mobile Tests Project**. 

<img src="url" width="70%" alt="Open iOS sample project">

Alternatively, you can download the iOS sample project from our Github repository: [iOS sample](https://github.com/katalon-studio-samples/ios-mobile-tests).

## Prepare the iOS application file

The current `Coffee Timer` application located in the `App` folder of this sample project is pre-built and signed by the Katalon team to only run on our devices.
As part of the iOS development procedure, to execute the sample test cases with your iOS devices, you need to build the `Coffee Timer` application for your iOS devices. To build iOS application file for Xcode simulators and real iOS devices, you can refer to this document: [Prepare the iOS application file](https://docs.katalon.com/katalon-studio/tutorials/mobile-ios-setup.html#part-5-prepare-the-ios-application-file).

After finishing building `Coffee Timer` application, put the file into the `App` folder of the sample project. Katalon will use this file to start the `Coffee Time` application.

## iOS sample project components

### Custom keywords

You can use custom keywords in the test case. To learn more about custom keywords, you can refer to this document: [Introduction to custom keywords](https://docs.katalon.com/katalon-studio/docs/introduction-to-custom-keywords.html).

Katalon creates the `startAppliucation` custom keyword to define the absolute path for starting the iOS application. To see the custom keyword, in the **Test Explorer** panel, go to **Keywords > sample > Common.groovy**.

<img src="url" width="70%" alt="Custom keywords in the iOS project">

<table>
<thead>
  <tr>
    <th>Parameter</th>
    <th>Type</th>
    <th>Mandatory</th>
    <th>Description</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>appPath</td>
    <td>String</td>
    <td>Yes</td>
    <td>The absolute path of the application installation file.</td>
  </tr>
  <tr>
    <td>uninstallAfterCloseApp</td>
    <td>boolean</td>
    <td>Yes</td>
    <td>true if uninstalling the application automatically after run.</td>
  </tr>
</tbody>
</table>

```groovy
public class Common {
	@Keyword
	def startAppliucation() {
		String appPath = RunConfiguration.getProjectDir() + '/App/Coffee Timer.ipa'
		Mobile.startApplication(appPath, false)
	}
}
```

> Notes:
> * If you change the name of the `Coffee Timer` application while building it, make sure to change the absolute path to the correct file accordingly.
> * If you are running test cases with Xcode simulators. The path should lead to the `Coffee Timer.app` file instead.

### Test cases


