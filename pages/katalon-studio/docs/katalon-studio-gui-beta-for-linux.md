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

Linux is an open-source operating system with many distributions. If you are a Linux user or you want to test your build in a Linux environment, you can still enjoy Katalon Studio with a GUI on your Linux. You can also use Katalon Runtime Engine for Linux to run your test in console mode.

Katalon Studio for Linux is compatible with any latest version of Linux distribution that supports Gnome, KDE, or Unity DE. You can find links to popular distribution download pages at [Linux.org](https://www.linux.org/pages/download/). Katalon Studio for Linux is tested by our Katalon team on Linux Ubuntu. To learn more about how to install Linux Ubuntu, see Ubuntu documentation: [Installation](https://help.ubuntu.com/community/Installation).

This guide covers setting up steps for running Katalon Studio GUI on Linux.

<details>
  <summary><strong>New to Linux? Here are some tips!</strong></summary>

You can install Linux with a LiveDVD, USB drive, or physical disk to a Virtual Machine. Before installing Linux, take a look at the [System Requirements](http://docs.katalon.com/display/KD/System+Requirements) to work with Katalon Studio.

Virtualization programs such as Parallels Desktop, Virtual Box, and VMWare Fusion run on the macOS allow you to create a Virtual Machine that mimics the hardware of a Linux operating system. For Windows, you can try Hyper-V by Microsoft. To learn more about these virtualization programs, see Parallels Desktop documentation [Parallels Desktop for Mac](https://www.parallels.com/products/desktop/resources/), Virtual Box documentation [About VirtualBox](https://www.virtualbox.org/wiki/VirtualBox), WMWare documentation [Creating a Linux Virtual Machine in Fusion](https://docs.vmware.com/en/VMware-Fusion/12/com.vmware.fusion.using.doc/GUID-4919245A-CD5D-4FC7-B5D0-4D90DFAFC7F7.html), or Microsoft documentation [Hyper-V on Windows Server](https://docs.microsoft.com/en-us/windows-server/virtualization/hyper-v/hyper-v-on-windows-server).
</details>

## Install Katalon Studio for Linux

### Environment Requirements

1. Verify whether your computer meets the System Requirements to work with Katalon Studio. You need to make sure that there is a minimum of 2 GB RAM (32-bit) or 4 GB RAM (64-bit) for the app to run normally. For more details, see [System Requirements](http://docs.katalon.com/display/KD/System+Requirements).

2. Install OpenJDK 8 on your Ubuntu (NOT Oracle JDK).

    > Katalon Studio for Linux currently supports OpenJDK 8 only.

    To install OpenJDK 8, open your Terminal. On the command line, type:

    ``` groovy
    sudo apt-get install openjdk-8-jre
    sudo update-alternatives --config java //then choose the openjdk-8-jre option
    java -version
    ```

    You can find more information about the installation steps at the OpenJDK document: [How to download and install prebuilt OpenJDK packages](http://openjdk.java.net/install/). Once you finish the installation, your `OpenJDK` information is displayed when you execute `java -version` command.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/katalon-studio-gui-beta-for-linux/Screen-Shot-2018-02-07-at-11.50.50.png" alt="linux" width=100%>

### Download Katalon Studio

Download [Katalon Studio for Linux](https://www.katalon.com/download/). Choose the Linux version of Katalon Studio, then click **Donwload**. A tar.gz file is downloading to your machine.

### Start Katalon Studio

1. Extract the tar.gz file. In the extracted folder, you can find the Katalon Studio app.

    Open Katalon Studio by double-clicking on Katalon Studio, or run `cd ./katalon` in your Terminal.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/katalon-studio-gui-beta-for-linux/katalon-ubuntu.png" alt="Katalon in extracted folder" width=100%>

2. The Katalon Studio app starts launching, then the **Katalon Studio Activation** dialog appears. You can click **Register** to sign up for a Katalon account and begin your 30 days trial or sign in to your existing account to activate your license. To learn more about license activation steps, see [Activate Katalon License](https://docs.katalon.com/katalon-studio/docs/activate-license.html).

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/katalon-studio-gui-beta-for-linux/activation-linux.png" alt="activate on linux" width=100%>

3. After you are done, click **Activate**. Now Katalon Studio is ready to use.

## Configure Katalon Studio on Linux

This section provides some additional setup for Mobile and Web Services.

### Mobile

1. Install Node.js. See Node.js documentation: [Node.js for Linux](https://nodejs.org/en/download/package-manager/#debian-and-ubuntu-based-linux-distributions).

2. Install Appium by typing this in the Terminal:

    ```groovy
    npm install -g appium
    ```

  * If you see an EACCES error with the Appium installation command, follow the instructions of npm documentation here: [Resolving EACCES permissions errors when installing packages globally](https://docs.npmjs.com/resolving-eacces-permissions-errors-when-installing-packages-globally).

  * If you encounter an error related to that Java `jar` file can't be found. You might need to add the environment variable: `KATALON_JAVA_HOME= <JRE_location>`.
  * Set the Appium directory manually in **Katalon Studio Preferences**. The default directory should be `/usr/lib/node_modules/appium/`.

### Web Services

To see the Web Service's response section and email template content, install `libwebkitgtk-3.0-0`. In the Terminal, type this:

```groovy
apt-get install libwebkitgtk-3.0-0
```

> Notes:
>
> There is no "On top" option in the Spy/Record dialog. To make it work, select and right-click the Spy/Record dialog, then choose **Always On Top** option.

### Troubleshoot configuration

You might encounter the `NoClassDefFoundError` error since Oracle JDK is being used. To resolve this error, do as follows:

1. Uninstall Oracle JDK.
2. Install [OpenJDK 8](http://openjdk.java.net/install/).

**See also**

* [Install Runtime Engine](https://docs.katalon.com/katalon-studio/docs/install-RE.html)
* [How to use Katalon TestOps plugin for Jenkins on Ubuntu](https://docs.katalon.com/katalon-studio/docs/jenkins-plugin-ubuntu.html)
* [Integrate Jenkins on Docker hosted in Ubuntu](https://docs.katalon.com/katalon-studio/docs/jenkins-docker-ubuntu.html)
