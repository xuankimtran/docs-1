---
title: "Tests not loading when executing with Chrome version 93,94 in Windows"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-testcloud/docs/troubleshoot-test-execution-chrome-93-94.html
description: 
---

When executing tests on TestCloud in Windows with Chrome version 93.x or 94.x, users may come across the following error:

``` groovy
SessionNotCreatedException: Message: session not created
from timeout: Timed out receiving message from renderer: 600.000
```

The tests hang on launching the browser and eventually time out. This is an issue from Chrome version 93.x and 94.x that doesn’t allow the ChromeDriver to start as a Windows service.

Here are two workarounds for this issue:

1. Set `--disable-gpu` for the desired capability in Chrome. For Katalon Studio users, to do so, go to **Project Settings > Desired Capabilities > Web UI > Chrome**. Click **Add**, then input as follows:

    <table width="587">
    <tbody>
    <tr>
    <td><strong>Name</strong></td>
    <td><strong>Type</strong></td>
    <td><strong>Value</strong></td>
    </tr>
    <tr>
    <td>args</td>
    <td>List</td>
    <td>--disable-gpu</td>
    </tr>
    </tbody>
    </table>

    With the configured desired capabilities, you can continue to work with Chrome version 93.x or 94.x

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/troubleshoot/TC-DS-2.jpg" width="90%" alt="Set desired capabilities in Chrome">

2. Downgrade to Chrome version 92.x. For Katalon Studio users, to downgrade ChromeDriver versions, you can refer to this guide here: [Update or Downgrade WebDrivers](https://docs.katalon.com/katalon-studio/docs/update-or-downgrade-webdrivers.html#update-a-webdriver).

    You can find other ChromeDriver versions here at the ChromeDriver website: [ChromeDriver](https://chromedriver.chromium.org/downloads).