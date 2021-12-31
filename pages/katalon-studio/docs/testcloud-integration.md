---
title: "Integrate TestCloud with Studio" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/testcloud-integration.html
---

This guide shows you how to configure TestCloud integration in Katalon Studio (KS) and execute tests/view reports with TestCloud.

## Integrate TestCloud with Studio

Follow these steps:

1. Open KS.
2. Go to **Project** > **Settings** > **Katalon TestCloud**.

    > Notes:
    >
    > You can also click on the *TestCloud* icon in the top right corner of KS to open the settings.
    >
    > <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops-intergration.png"  width=100% alt="tc icon in ks">

3. Check the **Enable Katalon TestCloud integration** box.
4. Select your organization, then click **Fetch Organization**.
5. Click **Apply** to finish.

You have activated your General Availability trial (GA trial) to use TestCloud.

## Run Test Suite/Test Suite Collection in public domains with TestCloud

Once you have enabled TestCloud integration, you have the option to run a test suite/test suite collection (TS/TSC) with TestCloud.

First, go to **Project** > **Settings** > **Execution**, then select **TestCloud** to configure the execution.

Secondly, follow the guides below for TS and TSC executions.

### Run Test Suite without TestCloud Tunnel

To run TS with TestCloud, follow these steps:

1. Create a TS with at least one test case.
2. Open the TS and choose to run with TestCloud.

    The **TestCloud Configuration** dialog appears as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops-intergration.png"  width=100% alt="tc icon in ks">

3. Select the OS/browser and its version in the **Configuration** section.

    > Notes:
    >
    > The tunnel box is unchecked by default. TestCloud Tunnel is for running tests in private domains. See: [Run Test Suite/Test Suite Collection in private domains with TestCloud](link).

4. Click **Run**.

### Run Test Suite Collection without TestCloud Tunnel

To run TSC with TestCloud, follow these steps:

1. Create a TSC, then add TS into the TSC.
2. Open the TSC, double-click the **Run with** column, and select **TestCloud**.
3. Double click on the **Run Configuration** column to open the **TestCloud Configuration** dialog.

    The **TestCloud Configuration** dialog appears as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops-intergration.png"  width=100% alt="tc config dialog">

3. Select the OS/browser and its version in the **Configuration** section.

    > Notes:
    >
    > The tunnel box is unchecked by default. TestCloud Tunnel is for running tests in private domains. See: [Run Test Suite/Test Suite Collection in private domains with TestCloud](link).

4. Click **Run**.

You have run TS/TSC in public domains with TestCloud.

### View TestCloud reports

After test execution, all information are consolidated in execution logs and reports. You can view TestCloud reports in the following format: CSV, PDF, JUnit, html.

See: [Test Suite and Test Suite Collection Reports](https://docs.katalon.com/katalon-studio/docs/test-suite-report.html).

## Run Test Suite/Test Suite Collection in private domains with TestCloud

If you want to execute TS/TSC in private domains, you can use a tunnel in TestCloud.

For detailed information on TestCloud Tunnel and how to utilize it, see [TestCloud Tunnel](https://docs.katalon.com/katalon-testcloud/docs/testcloud-tunnel.html).

### Configure TestCloud Tunnel

> Notes:
>
> Currently, you cannot setup the tunnel directly on KS. We provide **Tunnel Setup Helper** for a workaround.

Follow these steps:

1. Open the **TestCloud Configuration** dialog.
2. Check **Execute with Tunnel for private domain testing** box.

    You will see a message in red as follows:

     <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops-intergration.png"  width=100% alt="tunnel setup helper">

3. Click on the **Tunnel Setup Helper** link in the message.

    The **Tunnel Setup Helper** dialog appears as below.

4. Follow the instructions in the dialog to set up the tunnel client in your local machine.

    * Step 1: Select your OS and download the file, then unzip the file.
    * Step 2: Copy the command line in the dialog and paste it into your CLI to set up the tunnel.
    * Step 3: Copy the command line in the dialog and paste it into your CLI to start the tunnel.

After starting the tunnel, go back to KS and you can now run tests in private domains.
