---
title: "Set up WinAppDriver" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/setup-winappdriver.html 
---
This document shows you how to install and run Windows Application Driver (WindAppDriver) on a Windows 10 machine before performing automation test for Windows application. 

> What is the test machine?
>
> The test machine is where you have the Application Under Test installed and tested.

> What is the test runner machine?
> 
> * The test runner machine is where you install Katalon Studio and store the test scripts. 
> * The test runner machine and the test machine can be the same machine or different ones (remote connection).
## Install & Run WindAppDriver on Windows 10 machine
### Install WindAppDriver

> Notes:
> 
> Install and run WinAppDriver on the test machine. 

There are two ways to install WinAppDriver on a Windows 10 machine:

1. From the Katalon Studio toolbar, select **Tools > Windows > Install WinAppDrivers**. The **Windows Application Driver Setup** window opens. Follow the instructions to install the Windows Application Driver.

2. You can also refer to the WindAppDriver Github project document here: [Installing and Running Windows Application Driver](https://github.com/microsoft/WinAppDriver#installing-and-running-windows-application-driver) for the installation. 
### Run WindAppDriver

1. Enable **Developer Mode** on the test machine. You can refer to the Microsoft document here: [Enable your device for development](https://docs.microsoft.com/en-us/windows/uwp/get-started/enable-your-device-for-development) for instructions.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/introduction-desktop-app-testing/dev-mode.png" width="305.5" height="">
   
2. By default, WindAppDriver is installed at `C:\Program Files (x86)\Windows Application Driver`. To run WindAppDriver, double-click the `WinAppDriver.exe` file from the installation directory. 

## Set up WindAppDriver for the remote connection
### On the Windows 10 test machine

After installing WindAppDriver and enabling **Developer Mode**, to configure WindAppDriver for the remote connection, follow these steps:

1. Open **Task Manager** > Select **File** > Create a new task.
2. Select **Create this task with administrative privileges** and enter `cmd` in the **Open** text box, then click the **OK** button.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/introduction-desktop-app-testing/Set-up-1.png" width="476" height="171">

3. Run `cd` to your WindAppDriver installation folder. By default, it is at `C:\Program Files (x86)\Windows Application Driver`.
4. Run `WinAppDriver.exe <IP_Adress> <Port>`.
    
    * `IP_Adress`: is the public IP address of the test machine. Run `ipconfig.exe` to determine the IP address.
    * `Port`: is the public port of the remote machine. By default, it should be 4723.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/introduction-desktop-app-testing/Set-up-2.png" width="690" height="146">
### On the test runner machine

> Notes:
> 
> The test runner machine can be Windows, macOS or Linux.

While building your test script, make sure to have the `WinAppDriver URL` point to the IP address of the remote test machine. In the above example, it should be: `http://192.168.37.95:4723/`.

The application file path points the file path on the remote machine.


**Next step:**

After setting up WindAppDriver, you can begin creating your first Windows Desktop Apps tests. You can refer to the following document for further details: 
* [Create test cases using Windows Record Utility](https://docs.katalon.com/katalon-studio/docs/windows-recorder-tutorials.html#coordinate-based-recording)
* [Create test cases using Windows Spy Utility](https://docs.katalon.com/katalon-studio/docs/windows-spy-tutorials.html)