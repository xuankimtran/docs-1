---
title: "Integration with Jira" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/ka-integration-jira.html 
description: How to integrate KA with Jira
---
## Configuration

**Prerequisites:**
* The [Katalon BDD Add-on for Jira](https://docs.katalon.com/katalon-studio/docs/BDD-field-jira-cloud.html#install-and-use-katalon-bdd-custom-field-in-jira-cloud) installed 

**In Jira**

1. Navigate to **Katalon Settings** at the bottom of Project Settings.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/jira-ka-configure/1-jira-ka-config.png)

2. Enter the email registered for Katalon account.
3. Enter an **[API Key](https://docs.katalon.com/katalon-analytics/docs/api-key.html)**.
4. Enter **[Organization ID](https://docs.katalon.com/katalon-analytics/docs/getting-started.html)**.

then click **Save**.

**In Katalon Analytics**

1. Navigate to **Jira Settings** located in the toolbar of the project page.
2. Enter Jira URL, Username and Password.

* Jira Cloud

    a. Jira URL must be in the form of _Https://<site_name>.atlassian.net_.\
    b. Enter your email registered for the Jira Cloud account in Username.\
    c. Enter an Atlassian Cloud's API token in Password. See the instructions **[here](https://confluence.atlassian.com/cloud/api-tokens-938839638.html)**.

* Jira Server

    a. Jira URL must be in the form of _Http(s)://domain_ without any trailing parts e.g. _/secure_.\
    b. Use your username instead of an email in Username.\
    c. Enter Password.

then click **Save**.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/jira-ka-configure/2-jira-ka-config.png)

## Jira releases


1. In **Katalon Analytics**, create a new release, then link your test case with the release. The test cases that you already linked will be shown under **Release** section.

2. In Jira, create a new release or use an existing release to integrate with **Katalon Analytics**. 


3. After everything is setup, open section **Release** in **Katalon Analytics** and select **Jira Project** and **Jira Release** from drop-down lists.


Example of viewing release status in **Jira Cloud**:

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/jira-ka-configure/3-jira-release.png)


## Jira issues

1. Go to project and select a test case under **ID** section.

*Note: You can filter by Release by selecting a release in the drop-down list.*


2. Click on **test case ID** in **History**.


3. Add **Jira issue** to **Test Result** in **Katalon Analytics**.

> Note: You can add more than one issue by typing [issue1,issue2,...].


