---
title: "Integrate TestCloud with TestOps"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-testcloud/docs/integrate-testcloud-with-testops.html
description: Instructions on how to use TestCloud in TestOps
---

Katalon TestCloud (trial period) is now available for seamless integration with Katalon TestOps.

Current test environments require time and effort to set up and maintain while providing limited browser/operating system (OS) options. By contrast, with just a few clicks, you can easily set up a TestCloud Test Environment in Katalon TestOps for your test execution across browsers and OS.

The TestCloud Test Environment also allows you to:

* execute tests on a public domain.
* execute tests on a private domain via a TestCloud tunnel.
* track your TestCloud testing quota.

TestCloud stabilizes the test results when you execute a massive number of parallel tests.

## Integrate TestCloud with TestOps

All users who belong to a TestOps organization can now use Katalon TestCloud (trial period).

Follow the guidelines below to run tests in a TestCloud environment.

> Requirements:
>
> Kobiton integration must be disabled. You can toggle **Kobiton** off in advanced settings. See: [Advanced settings](https://docs.katalon.com/katalon-analytics/docs/create-plan.html#advanced-settings).

## Run tests in public domains with TestCloud

Follow these steps:

1. Sign in to [Katalon TestOps](https://testops.katalon.io/login) and go to your Project.

2. Go to **Test Planning** and click **Schedule Test Run**.

    The **Schedule Test Run** dialog pops up.

3. Select **TestCloud Test Environment** from the dropdown list in the **Test Environment Type** section.

    The **TestCloud** section appears as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/testops-integration/public-domains/beta-testcloud-browser-selections.png" width=100% alt="testcloud section in schedule test run dialog">

4. Select the OS and browsers you want to test in the **TestCloud** section.

5. Click **Schedule**.

    You will be directed to the **Test Run List** page, where you can see the TestCloud Test Environment.

6. Click on the *Play* icon to run tests.

You have successfully run tests in public domains using the TestCloud Test Environment.

To check the progress of your test runs, see: [View Logs](https://docs.katalon.com/katalon-testcloud/docs/integrate-testcloud-with-testops.html#view-logs).

## Run tests in private domains with TestCloud

Follow these steps:

1. Sign in to [Katalon TestOps](https://testops.katalon.io/login) and go to your Project.

2. Go to **Test Planning** and click **Schedule Test Run**.

    The **Schedule Test Run** dialog pops up.

3. Select **TestCloud Test Environment** from the dropdown list in the **Test Environment Type** section.

4. Switch the toggle **Use TestCloud Tunnel** on.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/testops-integration/private-domains/beta-switch-testcloud-tunnel-on.png" width=100% alt="test run types page run with testcloud successfully">

5. Select the OS and browsers in the **TestCloud** section.

6. Click **Schedule**.  

	You will be directed to the **Test Run List** page, where you can see the newly-added TestCloud Test Environment.

7. Follow the below guideline to configure TestCloud Tunnel.

### Configure TestCloud Tunnel

> Notes:
>
> For detailed information on TestCloud Tunnel and how to utilize it, see [TestCloud Tunnel](https://docs.katalon.com/katalon-testcloud/docs/testcloud-tunnel.html).

After scheduling your test runs using TestCloud Tunnel, you need to activate this tunnel to start test executions in private domains.

Follow these steps:

1. Go to **Configurations** > **TestCloud Tunnels**.

    The **TestCloud Tunnels** page appears.

2. Select the **Setup** tab.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/testops-integration/private-domains/beta-activate-tescloud-tunnel-in-kt-configuration.png" width=100% alt="testcloud tunnel page">

    You will see an on-screen step-by-step instruction to set up your TestCloud Tunnel.

    Follow the on-screen instruction:

    i.  Select your OS, download the binary file, then unzip the file.

    ii. Right click on the file to open it in the terminal (for macOs), or open the file in cmd.exe (for Windows).

    > Notes for macOS users:
    >
    > If you cannot run the tunnel file, see [Unable to set up TestCloud Tunnel in macOS](/katalon-testcloud/docs/troubleshoot-macos-workaround.html) for a troubleshoot and workaround.

    iii. Copy the command in the **Generate configuration** section, paste it in Terminal/cmd, then click *Enter* to run the command.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/testops-integration/private-domains/beta-open-termina-for-configuring-testcloud-tunnel.png" width=100% alt="configure testcloud tunnel">

    iv. Copy the command in the **Start a tunnel** section, paste it in Terminal/cmd, then click *Enter* to run the command.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/testops-integration/private-domains/beta-open-termina-for-starting-testcloud-tunnel.png" width=100% alt="configure testcloud tunnel">

    You have successfully configured the TestCloud Tunnel.

3. Go to the **TestCloud Tunnels** page and select the **Tunnels** tab.

     <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/testops-integration/private-domains/beta-testcloud-tunnel-active.png" width=100% alt="configure testcloud tunnel">

    You can now see the *Active* status in the TestCloud Tunnel you have just activated.

4. Go to the **Test Run List** page and click on the *Play* icon to run your tests.

You have successfully run tests in private domains using the TestCloud Test Environment.

To check the progress of your test runs, see: [View Logs](https://docs.katalon.com/katalon-testcloud/docs/integrate-testcloud-with-testops.html#view-logs).

## View Logs

You can check the progress of your test runs by viewing the test run logs.

There are different ways to access logs.

To view logs via the test run page, follow these steps:

1. Go to **Test Execution** > **Test Run List**.

    The **Test Run List** page appears as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/testops-integration/view-logs/tc-test-run-list-page.png" width=100% alt="test run list page">

2. Click on the Test Run name (e.g., **Untitled**).

    The **Test Runs** page appears as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/testops-integration/view-logs/tc-untitled-test-runs-page.png" width=100% alt="tc test run page config column">

3. Mouse over the **Configuration** column and select the session ID in the column (e.g., **#3672**).

    The session ID page (e.g., the **Session: #3672** page) appears as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/testops-integration/view-logs/tc-3672-log.png" width=100% alt="tc test run page config column">

    You can view logs here.

Alternatively, you can view logs via the test environment page.

Follow these steps:

1. Go to **Test Execution** > **Test Run List**.

    The **Test Run List** page appears as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/testops-integration/view-logs/tc-test-run-list-page.png" width=100% alt="test run list page">

    You can see a list of all test runs with their test environments here.

2. Mouse over the **Test Environment** column of the test run you want to check, select a test environment in the column.

    The **Test Environments** page appears.

3. Scroll down to the **Sessions** section on the page.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/testops-integration/view-logs/tc-test-environment-session-id.png" width=100% alt="test run list page">

4. Click on a session ID (e.g., **3466**) to view logs.

    You can see the progress of your test runs here.
