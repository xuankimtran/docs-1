---
title: "Katalon Preferences" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/katalon-preferences.html 
redirect_from:
    - "/display/KD/Katalon+Studio+Preferences/"
    - "/display/KD/Katalon%20Studio%20Preferences/"
    - "/x/NQRO/"
    - "/katalon-studio/docs/katalon-studio-preferences/"
    - "/x/YYUw/"
    - "/katalon-studio/docs/execution-preferences-version-50-and-below/"
    - "/katalon-studio/docs/execution-preferences-version-50-and-below.html"
    - "/katalon-studio/docs/katalon-studio-preferences.html"
description: 
---

Katalon Preferences define default behaviors of Katalon Studio across projects. In Katalon Preferences, you can configure:

- [Git](https://docs.katalon.com/katalon-studio/docs/git-integration.html#configure-git-integration)
- [Kobiton](https://docs.katalon.com/katalon-studio/docs/integrate_with_kobiton.html#enable-kobiton-integration)
- [Mobile](https://docs.katalon.com/katalon-studio/docs/mobile-preferences.html)
- [Object Spy](https://docs.katalon.com/katalon-studio/docs/object-spy-preferences.html)
- [Plugin](https://docs.katalon.com/katalon-studio/docs/kse-use-plugins.html)
- [Proxy](https://docs.katalon.com/katalon-studio/docs/proxy-preferences.html)
- [Recorder](https://docs.katalon.com/katalon-studio/docs/record-web-utility-using-chrome-with-profile.html#configuring-and-using-katalon-record-utility-with-chrome-profile)
- [Test Case](https://docs.katalon.com/katalon-studio/docs/test-case-preferences.html)

In this article, you can learn some basic configurations for general behaviors at startup.

## Katalon Preferences

To configure Katalon general behaviors at startup, from the main menu, go to **Katalon Studio > Preferences > Katalon**.

Shortcut to open the **Preferences** dialog: 
  * macOC: <button>⌘</button> <button>`</button>
  * Windows: Ctrl + Shift + P

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/katalon-studio-preferences/KS-PREF-Katalon-preferences.png" width=80% alt="Katalon preferences">

You can see the following options:

<table>
<thead>
  <tr>
    <th>Options</th>
    <th>Capabilities</th>
  </tr>
</thead>
<tbody>
<tr>
    <td>On the next starting application</td>
    <td>This option allows you to <strong>Auto restore the previous session</strong> or <strong>Open a clean session</strong> when starting Katalon Studio.</td>
    <td></td>
  </tr>
  <tr>
    <td>Show Help at startup</td>
    <td>This option allows you to turn on/off the <strong>Help</strong> page at startup.</td>
    <td></td>
  </tr>
  <tr>
    <td>Automatically check for new version</td>
    <td>This option allows Katalon Studio to automatically check for the latest version.</td>
    <td></td>
  </tr>
</tbody>
</table>

You need an active Katalon Studio Enterprise license to disable these functions below:

<table>
<thead>
  <tr>
    <th>Options</th>
    <th>Capabilities</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>Allow usage tracking</td>
    <td>This option allows you to configure the usage tracked by Katalon Studio. <br>By default, Katalon Studio is allowed to collect errors, execution logs, and other information about your application use. <br>You can refer to this document: <a href="https://www.katalon.com/terms/katalon/privacy-policy/">Privacy Policy</a> for further details of our tracking.</td>
  </tr>
  <tr>
    <td>Received dynamic content notifications</td>
    <td>From Katalon version 8.2.0 onwards, you can stop receiving notifications from the Katalon Studio team by unchecking this option.</td>
  </tr>
  <tr>
    <td>Show Start Page contents</td>
    <td>From Katalon version 8.2.0 onwards, you can hide Start Page contents by unchecking this option.</td>
  </tr>
</tbody>
</table>

> To learn more about Katalon licenses, see [Types of Licenses](https://docs.katalon.com/katalon-studio/docs/license.html).

> All the above preferences are saved into the `com.kms.katalon.composer.testcase.prefs` file under the "**config\\.metadata\\.plugins\\org.eclipse.core.runtime\\.settings**" location in your Katalon Studio build folder. You can manually modify the values in this file to change these preference settings.

You can also import Preferences to reuse a previous configuration. See [Import Preferences](https://docs.katalon.com/katalon-studio/docs/import-preferences.html).