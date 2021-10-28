---
title: "Katalon Studio for Linux (GUI)" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/katalon-studio-gui-beta-for-linux.html 
redirect_from:
    - "/display/KD/Katalon+Studio+GUI+%28beta%29+for+Linux/"
    - "/display/KD/Katalon%20Studio%20GUI%20%28beta%29%20for%20Linux/"
    - "/x/fwTR/"
    - "/katalon-studio/docs/katalon-studio-gui-beta-for-linux/"
    - "/display/KD/Linux+Support/"
    - "/display/KD/Linux-Support/"
    - "/display/KD/Linux%20Support/"
    - "/display/KD/Linux+Support/index.html"
description: 
---

Linux is an open-source operating system with many distributions. If you are a Linux user or you want to test your build in a Linux environment, you can still enjoy Katalon Studio with a GUI on your Linux. You can also run your test in console mode with Katalon Runtime Engine for Linux.

Katalon Studio for Linux is compatible with any latest version of Linux distribution that supports Gnome, KDE, or Unity Desktop Environment. You can find links to popular distribution download pages at [Linux.org](https://www.linux.org/pages/download/). Our Katalon team has tested Katalon Studio for Linux on Ubuntu Linux. See the Ubuntu manual for additional information on how to install Linux Ubuntu: [Installation](https://help.ubuntu.com/community/Installation).

This guide covers setting up steps for running Katalon Studio GUI on Linux.

<details>
  <summary><strong>New to Linux? Here are some tips!</strong></summary>

You can install Linux with a LiveDVD, USB drive, or physical disk to a Virtual Machine. Before installing Linux, take a look at the [System Requirements](http://docs.katalon.com/display/KD/System+Requirements) to operate with Katalon Studio.

On macOS, virtualization programs like Parallels Desktop, Virtual Box, and VMWare Fusion allow you to construct a Virtual Machine that emulates the hardware of a Linux operating system. Microsoft's Hyper-V is a good option for Windows. To learn more about these virtualization programs, see Parallels Desktop documentation [Parallels Desktop for Mac](https://www.parallels.com/products/desktop/resources/), Virtual Box documentation [About VirtualBox](https://www.virtualbox.org/wiki/VirtualBox), WMWare documentation [Creating a Linux Virtual Machine in Fusion](https://docs.vmware.com/en/VMware-Fusion/12/com.vmware.fusion.using.doc/GUID-4919245A-CD5D-4FC7-B5D0-4D90DFAFC7F7.html), or Microsoft documentation [Hyper-V on Windows Server](https://docs.microsoft.com/en-us/windows-server/virtualization/hyper-v/hyper-v-on-windows-server).
</details>

## Install Katalon Studio for Linux

### Environment Requirements

> From Katalon Studio version 7.9.1 onwards, we only support 64-bit Windows, macOS, and Linux.

1. Verify whether your computer meets the System Requirements to work with Katalon Studio. You need to make sure that there is a minimum of 2 GB RAM (32-bit) or 4 GB RAM (64-bit) for the app to run normally. For more details, see [System Requirements](http://docs.katalon.com/display/KD/System+Requirements).

2. Install OpenJDK 8 (NOT Oracle JDK).

    > Katalon Studio for Linux currently supports OpenJDK 8 only.

    To install OpenJDK 8 on your Ubuntu, open your Terminal. On the command line, type:

    ``` groovy
    sudo apt-get install openjdk-8-jre
    ```

    Once you finish the installation, your `OpenJDK` information is displayed when you execute `java -version` command.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/katalon-studio-gui-beta-for-linux/Screen-Shot-2018-02-07-at-11.50.50.png" alt="linux" width=100%>

    If you have multiple versions of OpenJDK installed on your Ubuntu and the correct version is not being used, use the alternatives command to switch between them:
    
    ``` groovy
    
    sudo update-alternatives --config java //then choose the openjdk-8-jre option
    ```

    Verify the version of the JDK again using `java -version` command.

    > After you have finished configuring the system, restart for your changes to take effect.

    You can find more information about the installation steps for other Linux distributions at the OpenJDK document: [How to download and install prebuilt OpenJDK packages](http://openjdk.java.net/install/).

### Download Katalon Studio

Download [Katalon Studio for Linux](https://www.katalon.com/download/). Choose the Linux version of Katalon Studio, then click **Download**. A tar.gz file is being downloaded to your machine.

### Start Katalon Studio

1. Extract the tar.gz file. In the extracted folder, you can find the Katalon Studio app.

    Open Katalon Studio by double-clicking on Katalon Studio, or run `cd ./katalon` in your Terminal.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/katalon-studio-gui-beta-for-linux/katalon-ubuntu.png" alt="Katalon in extracted folder" width=100%>

2. The Katalon Studio app launches, then the **Katalon Studio Activation** dialog appears. Sign in to your Katalon account to activate your license, or click **Register** to sign up. To learn more about license activation steps, see [Activate Katalon License](https://docs.katalon.com/katalon-studio/docs/activate-license.html).

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/katalon-studio-gui-beta-for-linux/activation-linux.png" alt="activate on linux" width=100%>

3. After you are done, click **Activate**. Now Katalon Studio is ready to use.

## Configure Katalon Studio on Linux

This section provides some additional setup for Web Services.

## Mobile

You can only test an **iOS** application using **macOS**. To set up Android tests on Linux machine, see [Set up Android tests on Linux](https://docs.katalon.com/katalon-studio/tutorials/mobile-android-setup.html#on-linux-machine)

### Web Services

To see the Web Service's response section and email template content, install `libwebkitgtk-3.0-0`. In the Terminal, type this:

```groovy
apt-get install libwebkitgtk-3.0-0
```

> Notes:
>
> There is no "On top" option in the Spy/Record dialog. To make it work, select and right-click the Spy/Record dialog, then choose the **Always On Top** option.

### Troubleshoot configuration

You might encounter the `NoClassDefFoundError` error since Oracle JDK is being used. To resolve this error, do as follows:

1. Uninstall Oracle JDK.
2. Install [OpenJDK 8](http://openjdk.java.net/install/).

**See also**

* [Install Runtime Engine](https://docs.katalon.com/katalon-studio/docs/install-RE.html)
* [How to use Katalon TestOps plugin for Jenkins on Ubuntu](https://docs.katalon.com/katalon-studio/docs/jenkins-plugin-ubuntu.html)
* [Integrate Jenkins on Docker hosted in Ubuntu](https://docs.katalon.com/katalon-studio/docs/jenkins-docker-ubuntu.html)
