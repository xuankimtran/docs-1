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

Linus is a reliable computer ecosystems. You can still enjoy Katalon Studio with a GUI on your Linux. Katalon Studio for Linux (Ubuntu tested) supports both IDE and console mode versions.

If you have not used Linux before and need to test your build in Linux environment, here are some suggestions to install Linux on your desktop or laptop computer:

* Linux distribution: You can find links to popular distribution download pages at [Linux.org](https://www.linux.org/pages/download/).
* Linux installation: You can install Linux with a USB stick or a drive, see Ubuntu documentation:
* Use Linux on virtual machine: Virtualisation programs such as Parallels Desktop and VMWare Fusion run on the macOS, but allow you to create a Virtual Machine - or VM - that mimics the hardware of a Windows PC. For Windows, you can try Hyper-V by Microsoft.
* Another way to test your build in Linux environment without installing Linux is Docker. See Docker.

This guide covers setting-up steps for running Katalon Studio GUI on Linux.

## Installation

### Environment Requirements

1. Verify whether your computer meets the [System Requirements](http://docs.katalon.com/display/KD/System+Requirements) to work with Katalon Studio. This step is important if you run your Linux by creating a Virtual Machine or a USB stick. You need to make sure that there are minimum 2 GB RAM (32-bit) or 4 GB RAM (64-bit) for the app to run normally.

2. Install OpenJDK 8 on your Ubuntu (NOT Oracle JDK).

  > Katalon Studio for Linux currently supports OpenJDK 8 only.

  To install OpenJDK 8, open your Terminal. On the command line, type:

``` groovy
sudo apt-get install openjdk-8-jre
sudo update-alternatives --config java //then choose the openjdk-8-jre option
java -version
```

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/katalon-studio-gui-beta-for-linux/linux-config.png" alt="configure" width=100%>

  You can find more information about the installation steps at OpenJDK document: [How to download and install prebuilt OpenJDK packages](http://openjdk.java.net/install/). Once you finish the installation, your `OpenJDK` information is displayed when you execute `java -version` command.

  <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/katalon-studio-gui-beta-for-linux/Screen-Shot-2018-02-07-at-11.50.50.png" alt="linux" width=100%>

### Download Katalon Studio

* Download [Katalon Studio for Linux](https://www.katalon.com/download/). Choose Linux version of Katalon Studio, a tar.gz file is downloading to your machine.

* Do a quick check on [System Requirements](/display/KD/System+Requirements) before using Katalon Studio.

### Start Katalon Studio

Extract the tar.gz file. In the extracted folder, you can find the Katalon Studio app.
Open Katalon Studio by double-click on Katalon Studio, or run `cd ./katalon` in your terminal. 

The Katalon Studio start launching, then the ... dialog appears. You can sign up a Katalon account to start your 30 days trial, or sign in to your previous account to activate your license. To learn more about how to activate your license, see [Activate Katalon License](https://docs.katalon.com/katalon-studio/docs/activate-license.html).

  <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/katalon-studio-gui-beta-for-linux/activation-linux.png" alt="activate on linux" width=100%>

After you are done, click ... Now Katalon Studio is ready to run.

## Configure Katalon Studio on Linux

This section provide some additional set-up for Mobile and Web Services.

### Mobile

* Install [Node.js for Linux](https://nodejs.org/en/download/package-manager/#debian-and-ubuntu-based-linux-distributions)
* Install Appium:

  ```groovy
  npm install -g appium
  ```

  * If you see an EACCES error with the Appium installation command, follow the instructions [here](https://docs.npmjs.com/resolving-eacces-permissions-errors-when-installing-packages-globally).

  * You may need to [set JAVA_HOME](https://askubuntu.com/questions/175514/how-to-set-java-home-for-java?utm_medim=organic&utm_source=google_rich_qa&utm_campaign=google_rich_qa) if you encounter an error related to that Java `jar` file can't be found.
  * Set the Appium directory manually in **Windows > Katalon Studio Preferences**. The default directory should be **/usr/lib/node_modules/appium/**.

### Web Services

To see the Web Service's response section and email template content, install `libwebkitgtk-3.0-0`.

```groovy
apt-get install libwebkitgtk-3.0-0
```

> Notes:
>
> There is no "On top" option in the Spy/Record dialog. To make it work, please select the Spy/Record dialog > Right-click > choose **Always On Top** option.

### Troubleshoot configuration

You might encounter the `NoClassDefFoundError` error since Oracle JDK is being used. To resolve this error, do as follows:

1. Uninstall Oracle JDK.
2. Install [OpenJDK 8](http://openjdk.java.net/install/).
