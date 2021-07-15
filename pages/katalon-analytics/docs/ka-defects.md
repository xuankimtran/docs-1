---
title: "Defects" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/ka-defects.html 
redirect_from: /katalon-analytics/docs/kt-jira-issue.html
description: 
---

Katalon TestOps links Defects with Jira issues (Jira Bugs) and you can view them in both Katalon TestOps and Jira.

> Requirements:
>
> * You have installed [Jira App](https://marketplace.atlassian.com/apps/1217501/katalon-bdd-test-automation-for-jira).
>
> * You have configured Jira integration. See: [Jira Settings](https://docs.katalon.com/katalon-analytics/docs/kt-jira-config.html).

## Link Test Runs to Defects

To link a Test Run to a Jira Bug, follow these steps:

1. Sign in to [Katalon TestOps](https://testops.katalon.io/login) and go to your Project.

2. Go to **Reports & Analytics** > **Test Runs**.

3. Select a Test Run by clicking on its ID, then click on the **Test Results** tab.

    The **Test Results** page appears as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-july-ka-defects/test-results-page-1467-defects-box.png"  width=100% alt="test results page with defects box">

    The *Defects* icon looks like a bug.

3. Mouse over the Test Run you want to link to Jira. The *Defects* icon of that Test Run appears.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-july-ka-defects/test-result-defect-bug-icon-appears.png"  width=100% alt="defect icon in red box">

4. Click on the *Defects* icon.

    The screen appears as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-july-ka-defects/jira-defect-screen-appears.png"  width=100% alt="defect screen">

5. Enter the Jira issue in the **Jira Defects** section, and click on the *Link* icon.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-july-ka-defects/jira-defect-screen-highligh-link-button.png"  width=100% alt="enter jira issue with link icon highlight">

You have linked a Test Run to a Jira Bug.

### Quick Tips

You can also install Katalon Plugin to directly create a Jira issue when linking a Test Run.

Follow these steps:

1. Download [Katalon Integration Plugin](https://chrome.google.com/webstore/detail/katalon-integration/cechonbcopffiimhnkgghckbgipciedg).

    > Notes:
    >
    > The download is only available on Chrome browser.

2. Enable Katalon Plugin in Chrome Extensions.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-july-ka-defects/chrome-extension-page-katalon-plugin.png"  width=100% alt="chrome extension page">
    
3. The *Create* icon is now enabled in the **Jira Defects** section in Katalon TestOps.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-july-ka-defects/create-icon-enabled-in-jira-defect.png"  width=100% alt="create icon enabled in testops">

4. Click on the **Create** icon to switch directly to Jira, and navigate to Jira Project where you want to create a new Jira issue.

> Notes:
>
> Once you have enabled Katalon Plugin, you can always see the *Plugin* icon in the corner of a Jira issue.
> <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-july-ka-defects/link-test-run-to-kat102defect-blurname.png"  width=100% alt="plugin icon floating in jira">
>
> You can alwasy click on the icon to quickly switch back to Katalon TestOps.

## View linked Test Runs in Jira

1. Go to the Jira issue you have linked the Test Runs to.

2. Click on the **Linked Test Runs** section to see the details of linked Test Runs.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-july-ka-defects/jira-link-test-run-section-plugin.png"  width=100% alt="jira linked test runs section">

## View Defects in Katalon TestOps

Go to a linked Test Run ID, then click on the **Defects** tab to see the Defects you have added to this Test Run.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-july-ka-defects/defects-of-a-test-run-id.png"  width=100% alt="test run id's defects tab">

To see all the Defects, go to **Test Management** > **Defects**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-july-ka-defects/all-defects-page.png"  width=100% alt="all defects page">
