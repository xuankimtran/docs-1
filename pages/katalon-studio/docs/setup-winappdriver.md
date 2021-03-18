---
title: "Set up WinAppDriver" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/setup-winappdriver.html 
---
This document shows you how to install and run Windows Application Driver on a Windows 10 machine before performing automation test for Windows application. You need to install and run WinAppDriver on the test machine having the Application under test. While the machine where you install Katalon Studio (the test runner) and store test scripts can be either the same as the test machine (local connection) or another one (remote connection).

## Set up Windows Application Driver on a local Windows 10 machine

You can install WinAppDriver on a local Windows 10 machine in two ways:

* Refer to [Installing and Running Windows Application Driver](https://github.com/microsoft/WinAppDriver#installing-and-running-windows-application-driver) to install WinAppDriver. Open this folder `C:\Program Files (x86)\Windows Application Driver`, then double-click on **WinAppDriver.exe** file; or
* From the Katalon Studio toolbar, select **Tools > Windows > Install WinAppDrivers**. The **Windows Application Driver Setup** window will pop up. Follow the instructions to install the Windows Application Driver. Then run WinAppDriver.exe.

Enable **Developer Mode** on the test machine. Refer to the [official guide](https://docs.microsoft.com/en-us/windows/uwp/get-started/enable-your-device-for-development) from Microsoft for instructions.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/introduction-desktop-app-testing/dev-mode.png" width="305.5" height="">

## Set up Windows Application Driver on a remote Windows 10 machine

On the test machine:

1. Open **Task Manager** > Select **File** > Create a new task.
2. Select **Create this task with administrative privileges** and enter `cmd` in the **Open** text box, then click the **OK** button.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/introduction-desktop-app-testing/Set-up-1.png" width="476" height="171">

3. Run `cd` to folder `C:\Program Files (x86)\Windows Application Driver`.
4. Run `WinAppDriver.exe <IP_Adress> <Port>`.
    
    * *IP_Adress* is the public IP address of the test machine. Run `ipconfig.exe` to determine the IP address.
    * *Port* is the public port of the remote machine. By default, it should be 4723.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/introduction-desktop-app-testing/Set-up-2.png" width="690" height="146">
   
5. Enable **Developer Mode** on the test machine. Refer to the [official guide](https://docs.microsoft.com/en-us/windows/uwp/get-started/enable-your-device-for-development) from Microsoft for instructions.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/introduction-desktop-app-testing/dev-mode.png" width="305.5" height="">
