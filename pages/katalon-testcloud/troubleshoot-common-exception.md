---
title: "Troubleshoot test not loading when executing with Chrome version 93,94 in Windows"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-testcloud/docs/troubleshoot-test-execution-chrome-93-94.html
description: 
---

When executing tests on TestCloud in Windows with Chrome version 93.x or 94.x, users may come across the following error:

```
SessionNotCreatedException: Message: session not created
from timeout: Timed out receiving message from renderer: 600.000
```

The tests hang on launching the browser and eventually time out. This is an issue from Chrome itself that doesn’t allow the ChromeDriver to start as Windows service normally.

There are two ways to solve this issue:

1. Downgrade to Chrome version 92.x
2. Set `--disable-gpu` for the desired capability in Chrome. For Katalon Studio users, to do so, go to **Project Settings > Desired Capabilities > Web UI > Chrome**. Click **Add**, then input as follows:

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

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/troubleshoot/TC-TROUBLESHOOT-Set-desired-capability.png" width="70%" alt="Set desired capabilities in Chrome">