---
title: "Unable to set up TestCloud Tunnel in macOS"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-testcloud/docs/troubleshoot-macos-workaround.html
description: 
---

When you download the tunnel agent and follow the instructions to configure it in your macOS, you may come across the following warning:

 <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/troubleshoot/macOS-workaround/mac-warning.png" width=50% alt="testcloud section in schedule test run dialog">

For security reasons, Apple does not recognize the TestCloud tunnel as a valid application.

We are in the progress of signing TestCloud with Apple. By doing so, our developers receive Apple certificates to validate our application in macOS.

While waiting for the certificate, we provide you with the following workaround to configure the tunnel in macOS:

1. Click **Cancel** to close the warning dialog in your macOS.
2. Go to **System Preferences** > **Security & Privacy** > **General**.

    You will see the message: *"kt" was blocked from use because it is not from an identified developer*.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/troubleshoot/macOS-workaround/mac-privacy-setting.png" width=70% alt="testcloud section in schedule test run dialog">

3. Click **Allow Anyway**.

You can now go back to the instructions to configure the tunnel.

For configuring the tunnel in Studio, see: [Integrate TestCloud with Studio](https://docs.katalon.com/katalon-studio/docs/testcloud-integration.html#configure-testcloud-tunnel).

For configuring the tunnel in TestOps, see: [Integrate TestCloud with TestOps](https://docs.katalon.com/katalon-testcloud/docs/integrate-testcloud-with-testops.html#configure-testcloud-tunnel).
