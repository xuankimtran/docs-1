---
title: "Introduction to Desktop App Testing" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/introduction-desktop-app-testing.html 
---

> Starting in **Katalon Studio version 7.0**, you can execute a test on a Windows desktop application.

### **Windows Execution Type**

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/introduction-desktop-app-testing/Windows_Execution_1.png" width="267" height="319">

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/introduction-desktop-app-testing/Windows_Execution_2.png" width="535" height="375">

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/introduction-desktop-app-testing/Windows_Execution_3.png" width="535" height="463">

### **Windows Keyword**

To add a Windows keyword in the manual view:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/introduction-desktop-app-testing/Windows_Keyword_1.png" width="481" height="364">

To add a Windows keyword in the script view, enter `Win`, then press `Ctrl+Space`:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/introduction-desktop-app-testing/Windows_Keyword_2.png" width="563" height="268">

To have a picture of Windows built-in keywords, navigate to **Keywords Browser** > **Built-in Keywords** > **Windows Keyword**:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/introduction-desktop-app-testing/Windows_Keyword_3.png" width="317" height="449">

### **Windows Object**

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/introduction-desktop-app-testing/Windows_Object.png" width="481" height="279">

### **Spy Windows Object**

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/introduction-desktop-app-testing/Spy_Windows_Object.png" width="549" height="61.5">

### **Record Windows Action**

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/introduction-desktop-app-testing/Windows_Record_Action.png" width="600.5" height="65">

## **Set-up**

First, you need to install WinAppDriver. Refer to [Installing and Running Windows Application Driver](https://github.com/microsoft/WinAppDriver#installing-and-running-windows-application-driver) to install a WinAppDriver.

>Remember to enable **Developer Mode** on the testing machine.  

### Set up Windows Application Driver on a local Windows 10 machine

There are two ways of installing the WinAppDriver on a local Windows 10 machine.

1. Open this folder `C:\Program Files (x86)\Windows Application Driver`, then double-click on **WinAppDriver.exe** file.

2. From the Katalon Studio toolbar, select **Tools > Windows > Install WinAppDrivers**. The **Windows Application Driver Setup** window will pop up. Follow the instructions to install the Windows Application Driver.

### Set up Windows Application Driver on a remote machine

* Open **Task Manager** -> Select **File** -> Create a new task
* Check `Create this task with administrative privileges` and enter `cmd` in the **Open** text box, then click the **OK** button.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/introduction-desktop-app-testing/Set-up-1.png" width="476" height="171">

* Enter `cd` to folder `C:\Program Files (x86)\Windows Application Driver`.
* Enter `WinAppDriver.exe IP_Adress Port` \
    where: \
    *IP_Adress* is the public IP address of the remote machine \
    *Port* is the public port of the remote machine. By default, it should be 4723.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/introduction-desktop-app-testing/Set-up-2.png" width="690" height="146">
