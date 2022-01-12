---
title: "Integrate TestCloud with TestOps"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-testcloud/docs/integrate-testcloud-with-testops.html
description: Instructions on how to use TestCloud in TestOps
---

Katalon TestCloud (GA trial) is now available for seamless integration with Katalon TestOps.

Current test environments require time and effort to set up and maintain while providing limited browser/operating system (OS) options. By contrast, with just a few clicks, you can easily set up a TestCloud Test Environment in Katalon TestOps for your test execution across browsers and OS.

The TestCloud Test Environment also allows you to:

* execute tests on a public domain.
* execute tests on a private domain via a TestCloud tunnel.
* track your TestCloud testing quota.

TestCloud stabilizes the test results when you execute a massive number of parallel tests.

## Integrate TestCloud with TestOps

> Requirements:
>
> You have activated the TestCloud general availability trial (GA trial). Contact us at success@katalon.com for detailed information on the **free GA trial** package.

Once you have joined the GA trial, we will enable TestCloud in your TestOps account. You can then schedule your test runs on a TestCloud environment.

## Run tests in public domains with TestCloud

Follow these steps:

1. Sign in to [Katalon TestOps](https://testops.katalon.io/login) and go to your Project.

2. Go to **Test Planning** and click **Schedule Test Run**.

    The **Schedule Test Run** dialog pops up.

3. Select **TestCloud Test Environment** from the dropdown list in the **Test Environment Type** section.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/testops-integration/public-domains/test-environment-type-testcloud-beta-icon.png" width=100% alt="testcloud integrated in schedule test run dialog">

    The **TestCloud** section appears.
4. Select the OS and browsers you want to test in the **TestCloud** section, then click **Schedule**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/testops-integration/public-domains/beta-testcloud-browser-selections.png" width=100% alt="testcloud section in schedule test run dialog">

    You will be directed to the **Test Run Types** page, where you can see the TestCloud Test Environment.

5. Click on the *Play* icon to run tests.

You have successfully run tests in public domains using the TestCloud Test Environment.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/testops-integration/public-domains/beta-run-test-in-public-domain-testcloud.png" width=100% alt="test run types page run with testcloud successfully">

## Run tests in private domains with TestCloud

Follow these steps:

1. Sign in to [Katalon TestOps](https://testops.katalon.io/login) and go to your Project.

2. Go to **Test Planning** and click **Schedule Test Run**.

    The **Schedule Test Run** dialog pops up.

3. Select **TestCloud Test Environment** from the dropdown list in the **Test Environment Type** section.

4. Switch the toggle **Use TestCloud Tunnel** on.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/testops-integration/private-domains/beta-switch-testcloud-tunnel-on.png" width=100% alt="test run types page run with testcloud successfully">

5. Select the OS and browsers in the **TestCloud** section, then click **Schedule**.  

	You will be directed to the **Test Run Types** page, where you can see the newly-added TestCloud Test Environment.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/testops-integration/private-domains/beta-testcloud-tunnel-icon-in-test-run-types-page.png" width=100% alt="testcloud tunnel icon in test run types page">

    You still need to activate the TestCloud Tunnel to start the test execution.

### Configure the TestCloud Tunnel

> Notes:
>
> For detailed information on TestCloud Tunnel and how to utilize it, see [TestCloud Tunnel](https://docs.katalon.com/katalon-testcloud/docs/testcloud-tunnel.html).

After scheduling your test runs using a TestCloud Tunnel, you need to activate this TestCloud Tunnel to start test executions in private domains.

Follow these steps:

1. Go to **Configurations** > **TestCloud Tunnels**.

    The **TestCloud Tunnels** page appears.

2. Select the **Setup** tab.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/testops-integration/private-domains/beta-activate-tescloud-tunnel-in-kt-configuration.png" width=100% alt="testcloud tunnel page">

    You will see an on-screen step-by-step instruction to set up your TestCloud Tunnel.

    Follow the on-screen instruction:

    i.  Select your OS, download the binary file, then unzip the file.

    ii. Right click on the file to open it in the terminal (for macOs), or open the file in cmd.exe (for Windows).

    iii. Copy the command in the **Generate configuration** section, paste it in Terminal/cmd, then click *Enter* to run the command.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/testops-integration/private-domains/beta-open-termina-for-configuring-testcloud-tunnel.png" width=100% alt="configure testcloud tunnel">

    iv. Copy the command in the **Start a tunnel** section, paste it in Terminal/cmd, then click *Enter* to run the command.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/testops-integration/private-domains/beta-open-termina-for-starting-testcloud-tunnel.png" width=100% alt="configure testcloud tunnel">

    You have successfully configured the TestCloud Tunnel.

3. Go to the **TestCloud Tunnels** page and select the **Tunnels** tab.

     <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/testops-integration/private-domains/beta-testcloud-tunnel-active.png" width=100% alt="configure testcloud tunnel">

    You can now see the *Active* status in the TestCloud Tunnel you have just activated.

4. Go to the **Test Run Types** page and click on the *Play* icon to run your tests.

You have successfully run tests in private domains using the TestCloud Test Environment.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/testops-integration/private-domains/beta-run-test-in-private-domain-testcloud.png" width=100% alt="test run types page run with testcloud successfully">

## Track TestCloud testing quota

Follow these steps:

1. Go to **Settings** > **License Management**.

    The **Licenses** page appears.

2. Click on the **Katalon TestCloud** tab.

You can then check the following information:

* the number of parallel tests.
* the testing time.
