---
title: "Integrate TestCloud with TestOps"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-testcloud/docs/integrate-testcloud-with-testops.html
description: Instructions on how to use TestCloud in TestOps
---

Katalon TestCloud (Beta) is now available for a seamless integration with Katalon TestOps.

Current test environments require time and effort to set up and maintain them while providing limited browser/operating system (OS) options. By contrast, with just a few clicks, you can easily set up a TestCloud Test Environment in Katalon TestOps for your test execution across browsers and OS.

The TestCloud Test Environment also allows you to:
* execute tests on a public domain.
* execute tests on a private domain via a TestCloud tunnel.
* track your TestCloud testing quota.

TestCloud stabilizes the test results when you execute a massive number of parallel tests.

## Integrate TestCloud with TestOps

> Requirements:
>
> You have joined the TestCloud Beta Testing program to enable TestCloud in Katalon TestOps. Contact us at success@katalon.com for detailed information on how to join our Beta Testing program.

Once you have joined our Beta Testing program, we will enable TestCloud in your TestOps account. You can then schedule your test runs on a TestCloud environment.

> Notes:
>
> Our Beta Testing program currently limits TestCloud usage based on the number of parallel tests and execution time. Contact us at success@katalon.com for further information.

## Run tests in public domains with TestCloud

Follow these steps:

1. Sign in to [Katalon TestOps](https://testops.katalon.io/login) and go to your Project.

2. Go to **Test Planning** and click **Schedule Test Run**.
    
    The **Schedule Test Run** dialog pops up.

3. Select **TestCloud Test Environment** from the dropdown list in the **Test Environment Type** section.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/testops-integration/public-domains/beta-testcoud-test-environment-in-kt.png" width=100% alt="testcloud integrated in schedule test run dialog">
    
    The new **TestCloud** section appears.
4. Select the OS and browsers you want to test in the **TestCloud** section, then click **Schedule**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/testops-integration/public-domains/beta-testcloud-browser-selections.png" width=100% alt="testcloud section in schedule test run dialog">
    
    You will be directed to the **Test Run Types** page, where you can see the newly-added TestCloud Test Environment.

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

    You still need to activate the TestCloud Tunnel in order to start the test execution.

### Configure the TestCloud Tunnel

After scheduling your test runs using a TestCloud Tunnel, you need to activate this TestCloud Tunnel in order to start test executions in private domains.

Follow these steps:

1. Go to **Configurations** > **TestCloud Tunnels**. 

    The **TestCloud Tunnels** page appears. 

2. Select the **Setup** tab.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/testops-integration/private-domains/beta-activate-tescloud-tunnel-in-kt-configuration.png" width=100% alt="testcloud tunnel page">

3. Copy the command in the **Generate configuration** section, paste it in Terminal (for MacOs) or cmd (for Windows), then click *Enter* to run the command.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/testops-integration/private-domains/beta-open-termina-for-configuring-testcloud-tunnel.png" width=100% alt="configure testcloud tunnel">

    You have successfully set up the TestCloud Tunnel in your local machine.

4. Copy the command in the **Start a tunnel** section, paste it in Terminal/cmd, then click *Enter* to run the command.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/testops-integration/private-domains/beta-open-termina-for-starting-testcloud-tunnel.png" width=100% alt="configure testcloud tunnel">

    You have successfully started the TestCloud Tunnel.

5. Go to the **TestCloud Tunnels** page and select the **Tunnels** tab.

     <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/testops-integration/private-domains/beta-testcloud-tunnel-active.png" width=100% alt="configure testcloud tunnel">

    You can now see the *Active* status in the TestCloud Tunnel you have just activated.

6. Go to the **Test Run Types** page and click on the *Play* icon to run your tests.

You have successfully run tests in private domains using the TestCloud Test Environment.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/testops-integration/private-domains/beta-run-test-in-private-domain-testcloud.png" width=100% alt="test run types page run with testcloud successfully">

## Track TestCloud testing quota
