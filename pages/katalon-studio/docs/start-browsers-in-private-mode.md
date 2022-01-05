---
title: "Start browsers in private mode" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/start-browsers-in-private-mode.html 
redirect_from:
    - "/display/KD/Start+browsers+in+private+mode/"
    - "/display/KD/Start%20browsers%20in%20private%20mode/"
    - "/x/XAbR/"
    - "/katalon-studio/docs/start-browsers-in-private-mode/"
description: 
---

The following guidelines show you how to start browsers (Firefox, Chrome, Edge Chromium) in a private mode in Katalon Studio.

## Firefox

1. Go to **Project > Settings > Desired Capabilities > Web UI > Firefox**.

2. Click **Add** on the command toolbar, then input the following values:

   <table>
   <thead>
   <tr>
      <th colspan="3">Table 1</th>
   </tr>
   </thead>
   <tbody>
   <tr>
      <td>Name</td>
      <td>Type</td>
      <td>Value</td>
   </tr>
   <tr>
      <td>moz:firefoxOptions</td>
      <td>Dictionary</td>
      <td>Click More (...). In the pop-up <strong>Dictionary Property Builder</strong> dialog, click <strong>Add</strong>, then input values from Table 2.</td>
   </tr>
   </tbody>
   </table>

   <table>
   <thead>
   <tr>
      <th colspan="3">Table 2</th>
   </tr>
   </thead>
   <tbody>
   <tr>
      <td>Name</td>
      <td>Type</td>
      <td>Value</td>
   </tr>
   <tr>
      <td>args</td>
      <td>List</td>
      <td>--private</td>
   </tr>
   </tbody>
   </table>

   <a class="pop">
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/project-settings-new-ui/KS-DC-FIRFOX-Private-mode.png" width="70%" alt="Open Firefox with devtools in the private mode">
   </a>
   <p style="text-align: center;"><em>Click the image to enlarge it</em></p>

3. Click **Apply and Close**.

## Chrome

1. Go to **Project > Settings > Desired Capabilities > Web UI > Chrome**.

2. Click **Add** on the command toolbar, then input the following values:

    <table>
    <thead>
    <tr>
    <th>Name</th>
    <th>Type</th>
    <th>Value</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>args</td>
    <td>List</td>
    <td>--incognito</td>
    </tr>
    </tbody>
    </table>

      <img src="https://github.com/katalon-studio/docs-images/raw/c057a1480081acac602a7847483260c61f106559/katalon-studio/docs/project-settings-new-ui/KS-DC-Chrome-INCOGNITO.png" width=100% alt="ks chrome private mode">

3. Click **Apply and Close**.

## Edge Chromium

1. Go to **Project > Settings > Desired Capabilities > Web UI > Edge Chromium**.

2. Add a new property as follows.

   <table>
   <thead>
   <tr>
      <th colspan="3">Table 1</th>
   </tr>
   </thead>
   <tbody>
   <tr>
      <td>Name</td>
      <td>Type</td>
      <td>Value</td>
   </tr>
    <tr>
    <td>ms:edgeChromium</td>
    <td>boolean</td>
    <td>true</td>
   </tr>
   <tr>
      <td>ms:edgeOptions</td>
      <td>Dictionary</td>
      <td>Click More (...). In the pop-up <strong>Dictionary Property Builder</strong> dialog, click <strong>Add</strong>, then input values from Table 2.</td>
   </tr>
   </tbody>
   </table>

   <table>
   <thead>
   <tr>
      <th colspan="3">Table 2</th>
   </tr>
   </thead>
   <tbody>
   <tr>
      <td>Name</td>
      <td>Type</td>
      <td>Value</td>
   </tr>
   <tr>
      <td>args</td>
      <td>List</td>
      <td>-inprivate</td>
   </tr>
   </tbody>
   </table>

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/project-settings-new-ui/KS-DC-Edge-Chromium-Private-mode-1.png" width=100% alt="ks edge chromium dictionary property builder">

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/project-settings-new-ui/KS-DC-Edge-Chromium-Private-mode-2.png" width=100% alt="ks edge chromium private mode">

3. Click **Apply and Close**.