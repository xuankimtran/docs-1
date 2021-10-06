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

1. Go to **Project** > **Settings**.

    The **Project Settings** dialog appears.

2. Select **Desired Capabilities** > **Web UI** > **Firefox**.

3. Add a new property as follows.

    * **Name**: enter `firefox_profile`.
    * **Type**: select `Dictionary`.
    * **Value**: enter `browser.privatebrowsing.autostart=true`.

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/start-browsers-in-private-mode/1-private-mode.png" width=100% alt="ks firefox private mode">

## Chrome

1. Go to **Project** > **Settings**.

    The **Project Settings** dialog appears.

2. Select **Desired Capabilities** > **Web UI** > **Chrome**.

3. Add a new property as follows.

    * **Name**: enter `args`.
    * **Type**: select `List`.
    * **Value**: enter `--incognito`.

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/start-browsers-in-private-mode/2-private-mode.png" width=100% alt="ks chrome private mode">

## Edge Chromium

1. Go to **Project** > **Settings**.

    The **Project Settings** dialog appears.

2. Select **Desired Capabilities** > **Web UI** > **Edge Chromium**.

3. Add a new property as follows.

    * **Name**: enter `ms:edgeOptions`.
    * **Type**: select `Dictionary`.
    * **Value**: open the **Dictionary Property Builder** dialog and add the following property.
    
        * **Name**: enter `args`.
        * **Type**: select `List`.
        * **Value**: enter `-inprivate`.

        <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/start-browsers-in-private-mode/edge-chromium-2.png" width=100% alt="ks edge chromium dictionary property builder">

4. Add a second property as follows.

    * **Name**: enter `ms:edgeChromium`.
    * **Type**: select `Boolean`.
    * **Value**: `true`.

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/start-browsers-in-private-mode/edge-chromium-1.png" width=100% alt="ks edge chromium private mode">
