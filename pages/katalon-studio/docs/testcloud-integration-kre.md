---
title: "Run TestCloud with Katalon Runtime Engine" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/testcloud-integration-kre.html
---

## Configure TestCloud Tunnel

If you want to execute TS/TSC in private domains, you can use a tunnel in TestCloud.

For detailed information on TestCloud Tunnel and how to utilize it, see [TestCloud Tunnel](https://docs.katalon.com/katalon-testcloud/docs/testcloud-tunnel.html).

To configure TestCloud Tunnel, follow these steps:

1. Open the **TestCloud Configuration** dialog.
2. Check **Execute with Tunnel** box.

    The **Tunnel Setup Helper** dialog appears as below.

     <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops-intergration.png"  width=100% alt="tunnel setup helper">

3. Copy the command lines in the dialog.

4. Go to **Generate Command for Console Mode** in KRE.
5. In the **Executive Platform** section, choose **TestCloud** to run with, then click **OK**.

6. Paste the command lines in KRE.

-testcloudEnvironmentId="38" (fixed API - user  configure this Id) -browserType="TestCloud"

-testcloudTunnel=

Option override ?