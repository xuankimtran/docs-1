---
title: "Integrate TestCloud with Studio" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/testcloud-integration.html
---

Katalon TestCloud is a cloud-based test execution environment where you can automate test scripts across the most common and updated browsers and/or operating systems (OS) and/or a combination of both. See: [TestCloud Overview](https://docs.katalon.com/katalon-testcloud/docs/testcloud-overview.html).

This guide shows you how to configure TestCloud integration (Beta) in Katalon Studio (KS) and execute tests/view reports with TestCloud.

> Requirements:
>
> Katalon Studio version 8.2.5 onwards.

## Integrate TestCloud with Studio

Follow these steps:

1. Open KS.
2. Go to **Project** > **Settings** > **Katalon TestCloud**.

    > Notes:
    >
    > You can also click on the *TestCloud* icon in the top right corner of KS to open the settings.
    >
    > <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/studio-integration/testcloud-icon.png" width=30% alt="tc icon in ks">

    The **Project Settings** dialog appears as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/studio-integration/testcloud-project-settings.png" width=70% alt="tc icon in ks">

3. Make sure the **Enable Katalon TestCloud integration** box is checked.

4. Choose the organization you wish to run your test with.

   > Notes:
   >
   > If you cannot find your desired organization, click **Fetch Organization** to refresh. This action retrieves all available organizations you have joined. You then can select the organization you want in the dropdown menu.

5. Click **Apply and Close**.

You have enabled TestCloud integration in KS.

Once you have enabled TestCloud integration, you have the option to run a test suite/test suite collection (TS/TSC) with TestCloud.

Follow the guides below for TS and TSC executions.

## Run test suites with TestCloud

> Notes:
>
> You cannot run test cases with TestCloud.

To run TS with TestCloud, follow these steps:

1. Open your TS.
2. Click on the dropdown icon of the *Run* button and choose to run with TestCloud.

     <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/studio-integration/run-with-testcloud.png" width=30% alt="tc config dialog">

    The **TestCloud Configuration (Beta)** dialog appears as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/studio-integration/tc-config-dialog-run-public.png" width=50% alt="tc config dialog">

3. Select the OS, browser, and browser version in the **Configuration** section.

    > Notes:
    >
    > * We currently only support Linux (remote OS). For browsers, we support Chrome and Firefox.
    > * The tunnel box is unchecked by default. TestCloud Tunnel is for running tests in private domains. See: [Configure TestCloud Tunnel](/katalon-studio/docs/testcloud-integration.html#configure-testcloud-tunnel).

4. Click **Run**.

## Run test suite collections with TestCloud

To run TSC with TestCloud, follow these steps:

1. Open your TSC and double-click the **Run with** column.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/studio-integration/tsc-execution-info.png" width=70% alt="run with tc">

    The **Select an environment** dialog appears as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/studio-integration/run-tsc-testcloud-as-environment.png" width=50% alt="run config tsc">

2. Choose **TestCloud** as your test environment, then click **OK**.

3. Double click on the **Run Configuration** column to open the **TestCloud Configuration** dialog.

    The **TestCloud Configuration (Beta)** dialog appears as below.

     <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/studio-integration/tsc-run-config-tc-config-dialog.png" width=70% alt="tc config dialog">

4. Select the OS, browser, and browser version in the **Configuration** section.

    > Notes:
    >
    > * We currently only support Linux (remote OS). For browsers, we support Chrome and Firefox.
    > * The tunnel box is unchecked by default. TestCloud Tunnel is for running tests in private domains. See: [Configure TestCloud Tunnel](/katalon-studio/docs/testcloud-integration.html#configure-testcloud-tunnel).

4. Click **OK**.

## Configure TestCloud Tunnel

If you want to execute TS/TSC in private domains, you must use TestCloud Tunnel.

For detailed information on TestCloud Tunnel and how to utilize it, see [TestCloud Tunnel](https://docs.katalon.com/katalon-testcloud/docs/testcloud-tunnel.html).

To configure TestCloud Tunnel, follow these steps:

1. Open the **TestCloud Configuration (Beta)** dialog.
2. Check the **Execute with Tunnel for private domain testing** box.

    You will see a message in red as follows:

     <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/studio-integration/tunnel-setup-helper-link.png" width=50% alt="tc config dialog">

3. Click on the **Tunnel Setup Helper** link in the message.

    The **Tunnel Setup Helper** dialog appears as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/studio-integration/tunnel-helper.png" width=50% alt="tunnel setup helper">

4. Follow the step-by-step instructions in the dialog to set up the tunnel client in your local machine:

    * Step 1: Select your OS and download the .zip file, then unzip it.
    * Step 2: Open the command-line interface (CLI), copy the command line from the dialog, then run it in the CLI.

         An example command looks like this:

        ```groovy
        ./kt config --tenant KatalonStudio --username "your_username" --organization-id "your_organization_id" --api-key "your_api_key"
        ```

        You have set up the tunnel client in your local machine.

    * Step 3: Copy the command in the dialog and run it in your CLI to start the tunnel.

        An example command looks like this:
        
        ```groovy
        ./kt start
        ```

        <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/studio-integration/setup-tunnel-studio.png" width=100% alt="kt start">

    > Notes:
    >
    > Keep your CLI (cmd/terminal) open until you have finished running tests.

5. Go back to the **Tunnel Setup Helper** dialog and click **Close**.

    Once you have started the tunnel in your local machine, the **TestCloud Configuration (Beta)** dialog displays a green *Status: Available* message.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/studio-integration/tc-config-tunnel-setup-available.png" width=50% alt="tunnel setup helper">

    > Notes:
    >
    > You can also click on the **Refresh** button to have the status updated.

6. Click **Run** to start executing TS/TSC with TestCloud Tunnel.

## View TestCloud reports

After executing tests, execution data is consolidated in logs and reports. You can view TestCloud reports in the following formats: CSV, PDF, JUnit, HTML.

See: [Test Suite and Test Suite Collection Reports](https://docs.katalon.com/katalon-studio/docs/test-suite-report.html).