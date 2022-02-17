---
title: "Supported Environments"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/supported-environments.html
redirect_from:
    - "/display/KD/Supported+Environments/"
    - "/display/KD/Supported%20Environments/"
    - "/x/dAAM/"
    - "/katalon-studio/docs/supported-environments/"
    - "/display/KD/System+Requirements/"
    - "/display/KD/System%20Requirements/"
    - "/x/cgAM/"
    - "/katalon-studio/docs/system-requirements/"
    - "/katalon-studio/docs/system-requirements.html"
description:
---


> * Katalon Studio (KS) provides free, basic tools suitable for the testing needs of individuals. For an advanced business solution, you can purchase Katalon Studio Enterprise (KSE) licenses. To compare features between KS and KSE, you can refer to this document: [Katalon Studio vs Katalon Studio Enterprise Features](https://docs.katalon.com/katalon-studio/docs/katalon-studio-vs-katalon-studio-enterprise.html). 
> * Katalon Runtime Engine (KRE) is the test execution add-on of Katalon Studio. KRE allows you to execute tests in a command-line interface (CLI).

> Notes:
> * We recommend using the latest version of Katalon Studio. Download the latest version from the Katalon website: [Katalon products](https://www.katalon.com/download/).
> * From Katalon Studio version 7.9.0 onwards, we do not support 32-bit Windows systems.

## System requirements

<table>
<thead>
  <tr>
    <th> </th>
    <th></th>
    <th>Katalon Studio/Katalon Studio Enterprise</th>
    <th>Katalon Runtime Engine (KRE)</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td rowspan="3">Operating System</td>
    <td>Windows</td>
    <td colspan="2">Windows 7, Windows 8, Windows 10, Windows 11<br>Windows Server 2012</td>
  </tr>
  <tr>
    <td>macOS</td>
    <td colspan="2">macOS 10.11 or later</td>
  </tr>
  <tr>
    <td>Linux</td>
    <td>- Make sure you install OpenJDK 8.0. For further details, you can refer to this document: <a href="https://docs.katalon.com/katalon-studio/docs/katalon-studio-gui-beta-for-linux.html#install-katalon-studio-for-linux" target="_blank" rel="noopener noreferrer">Install Katalon Studio for Linux</a>.<br>- The latest version of Linux distribution that supports Gnome, KDE, or Unity DE. <br>- Tested on Ubuntu.<br></td>
    <td>- Make sure you install OpenJDK 8.0.<br>For further details, you can refer to this document: <a href="https://docs.katalon.com/katalon-studio/docs/katalon-studio-gui-beta-for-linux.html#install-katalon-studio-for-linux" target="_blank" rel="noopener noreferrer">Install Katalon Runtime Engine for Linux</a>.<br>- Debian, Ubuntu, RHEL, Fedora, and CentOS-based distribution. <br>- Tested on Ubuntu.<br></td>
  </tr>
  <tr>
    <td colspan="2">GUI components</td>
    <td>Required for all operating systems.</td>
    <td>KRE doesn't have GUI components. For further information about executing with KRE, you can refer to this document: <a href="https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#command-builder" target="_blank" rel="noopener noreferrer">Execution on KRE</a>.</td>
  </tr>
  <tr>
    <td colspan="2">CPU</td>
    <td colspan="2">Minimum: 2 GHz or faster 32-bit (x86) or 64-bit (x64) processor</td>
  </tr>
  <tr>
    <td colspan="2">Memory</td>
    <td>Minimum: 2 GB RAM (32-bit) or 4 GB RAM (64-bit)<br>Recommended: 4 GB RAM (32-bit) or 8 GB RAM (64-bit).</td>
    <td>Minimum: 2 GB RAM (32-bit) or 4 GB RAM (64-bit)<br>Recommendation for concurrent executions (and execution with Docker): the number of concurrent sessions x 2GB.<br>For example: Recommended RAM for 3 concurrent execution sessions is 6GB (3 x 2GB).</td>
  </tr>
  <tr>
    <td colspan="2">Hard Drive</td>
    <td colspan="2">At least 1 GB available hard disk space. Extra disk space is required depending on project source codes and generated execution reports.</td>
  </tr>
</tbody>
</table>

## Browsers

<table>
<thead>
  <tr>
    <th>Desktop Browsers</th>
    <th>Version on Windows</th>
    <th>Version on macOS</th>
    <th>Version on Linux</th>
    <th>Note</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>Internet Explorer (IE)</td>
    <td>9, 10, 11</td>
    <td>N/A</td>
    <td>N/A</td>
    <td>Required IE configurations: <a href="https://docs.katalon.com/katalon-studio/docs/internet-explorer-configurations.html" target="_blank" rel="noopener noreferrer">Internet Explorer Configurations</a>.</td>
  </tr>
  <tr>
    <td>Microsoft Edge</td>
    <td>18</td>
    <td>N/A</td>
    <td>N/A</td>
    <td></td>
  </tr>
  <tr>
    <td>Microsoft Edge (Chromium)</td>
    <td>80+</td>
    <td>80+</td>
    <td>N/A</td>
    <td>Supported in Katalon Studio v7.3.0+</td>
  </tr>
  <tr>
    <td>Firefox</td>
    <td>56+</td>
    <td>56+</td>
    <td>56+</td>
    <td>To use Firefox 57 with Katalon Studio, install Katalon Studio v5.1.0+</td>
  </tr>
  <tr>
    <td>Google Chrome</td>
    <td>58+</td>
    <td>58+</td>
    <td>58+</td>
    <td></td>
  </tr>
  <tr>
    <td>Opera</td>
    <td>N/A</td>
    <td>N/A</td>
    <td>N/A</td>
    <td></td>
  </tr>
  <tr>
    <td>Safari</td>
    <td>N/A</td>
    <td>12+</td>
    <td>N/A</td>
    <td></td>
  </tr>
</tbody>
</table>

## Mobile

<table>
<thead>
  <tr>
    <th>Installation</th>
    <th>Version on Windows</th>
    <th>Version on macOS</th>
    <th>Appium</th>
    <th>Native App support?</th>
    <th>Hybrid App support?(*)</th>
    <th>Mobile Browser support</th>
    <th>Xcode</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>Android</td>
    <td>6.x, 7.x, 8.x, 9.x</td>
    <td>6.x, 7.x, 8.x, 9.x</td>
    <td>1.12.1+</td>
    <td>Yes</td>
    <td>No(**)</td>
    <td>Yes</td>
    <td>N/A</td>
  </tr>
  <tr>
    <td>iOS</td>
    <td>N/A</td>
    <td>9, 10, 11, 12, 13</td>
    <td>1.12.1+</td>
    <td>Yes</td>
    <td>No</td>
    <td>Yes</td>
    <td>v9.4.1+</td>
  </tr>
</tbody>
</table>

(*) To handle hybrid apps, you can refer to the Appium document here: [Automating hybrid apps](http://appium.io/docs/en/writing-running-appium/web/hybrid/#automating-hybrid-apps).

(**) We offer some workarounds here: 
- [Capture elements in hybrid Android apps](https://docs.katalon.com/katalon-studio/docs/capture-elements-in-hybrid-android-apps.html).
- [Flutter-based application testing with custom SetText keyword](https://docs.katalon.com/katalon-studio/docs/flutter-based-application-testing.html).

## Windows

Katalon Studio fully supports automation testing for desktop apps written in the following platforms: 

- Universal Windows Platform (UWP)
- Windows Forms (WinForms)
- Windows Presentation Foundation (WPF)
- Classic Windows (Win32)
