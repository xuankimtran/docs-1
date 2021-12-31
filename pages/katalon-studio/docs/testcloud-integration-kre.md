---
title: "Run TestCloud with Katalon Runtime Engine" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/testcloud-integration-kre.html
---

To run Test Suite/Test Suite Collection (TS/TSC) with TestCloud in Katalon Runtime Engine (KRE), follow these steps:

1. Enable TestCloud integration in Katalon Studio (KS). See: [Integrate TestCloud with Studio](link).

2. Set up the tunnel client in your local machine. See: [Configure TestCloud Tunnel](link).

3. Go to **Generate Command for Console Mode** in KRE.

4. In the **Executive Platform** section, choose **TestCloud** to run with, then click **OK**.

5. Use the following Katalonc Command-line options:

    `-testcloudEnvironmentId="38"`

    `-browserType="TestCloud"`

    `-testcloudTunnel=`

## Override...?