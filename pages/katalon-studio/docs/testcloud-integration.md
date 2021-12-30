---
title: "Integrate TestCloud with Studio" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/testcloud-integration.html
---

This guide shows you how to configure TestCloud integration in Katalon Studio (KS) and execute tests/view reports with TestCloud.

## Enable TestCloud integration

Follow these steps:

1. Open KS.
2. Go to **Project** > **Settings** > **Katalon TestCloud**.
3. Check the **Enable Katalon TestCloud integration** box.
4. Select your organization, then click **Fetch Organization**.
5. Click **Apply** to finish.

You have activated your General Availability trial (GA trial) to use TestCloud.

## Configure test execution with TestCloud

Once you have enabled TestCloud integration, you have the option to run a test suite/test suite collection (TS/TSC) with TestCloud. 

To run TS with TestCloud, follow these steps:

1. Select your TS.
2. Click on the *Run* button, then select **TestCloud**.

To run TSC with TestCloud, follow these steps:

1. Select your TSC.
2. Double click **Run with** and select **TestCloud**.
3. Double click on the **Run Configuration** column to open the **TestCloud Configuration** dialog.

    The **TestCloud Configuration** dialog appears as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops-intergration.png"  width=100% alt="tc config dialog">

3. Fill in the required information.

    * In the **Configuration** section, select the OS/browser and its version.
    * If you want to use TestCloud Tunnel, check **Execute with Tunnel** box.

        > Notes:
        >
        > You need to configure TestCloud Tunnel in the **Tunnel Setup Helper** section. See the guide below.

4. Click **Run**.

You have run TS/TSC in public domains with TestCloud.

After test execution, information is consolidated into a report. You can view execution data and reports... (where?)
