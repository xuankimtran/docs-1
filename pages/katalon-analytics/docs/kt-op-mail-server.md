---
title: "Configure Mail Server"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/kt-op-mail-server.html 
description: How to configure mail server on TestOps OnPremise.
---
Katalon TestOps OnPremise (KTOP) is designed exclusively for a restricted network environment. You need to configure a mail server to send and receive email notifications of:

* Managing users at the organization or team level.

* Executing test schedulers.

## Configuration steps

1. Go to KTOP. Refer to this [document](https://docs.katalon.com/katalon-analytics/docs/testops-op-installation.html) for how to install and set up KTOP.

2. Under an Organization, select **Settings** tab.

3. Provide the information for your mail server.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-op-mail-server/kt-op-mail-server-config.png)

* **Host:** the domain name of the mail server.
* **Port:** the port to be used for that server.
* **Username & Password:** the account to authenticate with the server.
* **Protocol:** the protocol to communicate with the mail server.

4. Click **Update** to save and apply your configurations.

> Note: You can test the configuration by providing a test recipient and click **Send test email**.
