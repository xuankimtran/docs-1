---
title: "Integrate TestCloud with Studio" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/testcloud-integration.html
---

Katalon TestCloud is a cloud-based test execution environment where you can automate test scripts across the most common and updated browsers and/or operating systems (OS) and/or a combination of both. See: [TestCloud Overview](https://docs.katalon.com/katalon-testcloud/docs/testcloud-overview.html).

This guide shows you how to configure TestCloud integration (Beta) in Katalon Studio (KS) and execute tests/view reports with TestCloud.

> Requirements:
>
> Katalon Studio Enterprise version 8.2.5 onwards.

## Integrate TestCloud with Studio

Follow these steps:

1. Open KS.
2. Go to **Project** > **Settings** > **Katalon TestCloud**.

    > Notes:
    >
    > You can also click on the *TestCloud* icon in the top right corner of KS to open the settings.
    >
    > <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/studio-integration/testcloud-icon.png" width=50% alt="tc icon in ks">

    The **Project Settings** dialog appears as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/studio-integration/testcloud-project-settings.png" width=100% alt="tc icon in ks">

3. Make sure the **Enable Katalon TestCloud integration** box is checked.

4. Check your organization.

   > Notes:
   >
   > Click **Fetch Organization** to refresh. This action retreives all available organizations you have joined. You then can select the organization you want in the dropdown menu.

5. Click **Apply and Close**.

You have enabled TestCloud integration in KS.

## Run Test Suite/Test Suite Collection in public domains with TestCloud

> Notes:
>
> You cannot run Test Case with TestCloud.

Once you have enabled TestCloud integration, you have the option to run a test suite/test suite collection (TS/TSC) with TestCloud.

First, go to **Project** > **Settings** > **Execution**, then select **TestCloud** to configure the execution.

Secondly, follow the guides below for TS and TSC executions.

### Run Test Suite without TestCloud Tunnel

To run TS with TestCloud, follow these steps:

1. Open your TS.
2. Click on the dropdown icon of the *Run* button and choose to run with TestCloud.

     <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/studio-integration/run-with-testcloud.png" width=50% alt="tc config dialog">

    The **TestCloud Configuration (Beta)** dialog appears as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/studio-integration/tc-config-dialog-run-public.png" width=100% alt="tc config dialog">

3. Select the OS, browser and its version in the **Configuration** section.

    > Notes:
    >
    > * We currently support remote OS (Linux) and FireFox, Chrome browsers only.
    > * The tunnel box is unchecked by default. TestCloud Tunnel is for running tests in private domains. See: [Run Test Suite/Test Suite Collection in private domains with TestCloud](/katalon-studio/docs/testcloud-integration.html).

4. Click **Run**.

### Run Test Suite Collection without TestCloud Tunnel

To run TSC with TestCloud, follow these steps:

1. Open your TSC and double-click the **Run with** column.

    The **Select an environment** dialog appears as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/studio-integration/run-tsc-testcloud-as-environment.png" width=100% alt="run config tsc">

2. Choose **TestCloud** as your test environment, then click **OK**.

3. Double click on the **Run Configuration** column to open the **TestCloud Configuration** dialog.

    The **TestCloud Configuration (Beta)** dialog appears as below.

     <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/studio-integration/tc-config-dialog-run-public.png" width=100% alt="tc config dialog">

4. Select the OS, browser and its version in the **Configuration** section.

     > Notes:
    >
    > * We currently support remote OS (Linux) and FireFox, Chrome browsers only.
    > * The tunnel box is unchecked by default. TestCloud Tunnel is for running tests in private domains. See: [Run Test Suite/Test Suite Collection in private domains with TestCloud](/katalon-studio/docs/testcloud-integration.html).

4. Click **Run**.

You have run TS/TSC in public domains with TestCloud.

### View TestCloud reports

After test execution, all information are consolidated in execution logs and reports. You can view TestCloud reports in the following format: CSV, PDF, JUnit, html.

See: [Test Suite and Test Suite Collection Reports](https://docs.katalon.com/katalon-studio/docs/test-suite-report.html).

## Run Test Suite/Test Suite Collection in private domains with TestCloud

If you want to execute TS/TSC in private domains, you must use a TestCloud Tunnel.

For detailed information on the TestCloud Tunnel and how to utilize it, see [TestCloud Tunnel](https://docs.katalon.com/katalon-testcloud/docs/testcloud-tunnel.html).

### Configure TestCloud Tunnel

Follow these steps:

1. Open the **TestCloud Configuration (Beta)** dialog.
2. Make sure the **Execute with Tunnel for private domain testing** box is checked.

    You will see a message in red as follows:

     <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/studio-integration/tunnel-setup-helper-link.png" width=100% alt="tc config dialog">

3. Click on the **Tunnel Setup Helper** link in the message.

    The **Tunnel Setup Helper** dialog appears as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/studio-integration/tunnel-helper.png" width=100% alt="tunnel setup helper">

4. Follow the step-by-step instructions in the dialog to set up the tunnel client in your local machine:

    * Step 1: Select your OS and download the .zip file, then unzip it.
    * Step 2: Open the CLI, copy the command line from the dialog, then run it in the CLI.
    
        For example, the command line is `./kt config --tenant KatalonStudio --username "your_username" --organization-id "your_organization_id" --api-key "your_api_key"`.

        <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/studio-integration/windows-cmd-tunnel-config.png" width=100% alt="kt config cmd">
    
        You have set up the tunnel client in your local machine.

    * Step 3: Copy the command line in the dialog and run it in your CLI to start the tunnel.

        For example, the command line is `./kt start`.

        <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/studio-integration/setup-tunnel-studio.png" width=100% alt="kt start">

    > Notes:
    >
    > Keep your CLI (cmd/terminal) open until you have finished running tests.

5. Go back to KS.

    Once you have started the tunnel in your local machine, the tunnel status on the **Tunnel Setup Helper** dialog is *Available*.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/studio-integration/tc-config-tunnel-setup-available.png" width=100% alt="tunnel setup helper">

    > Notes:
    >
    > You can also click on the **Refresh** button to make sure the tunnel is available.