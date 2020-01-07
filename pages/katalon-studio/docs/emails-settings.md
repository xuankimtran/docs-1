---
title: "Emails Settings" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/emails-settings.html 
redirect_from:
    - "/display/KD/Emails+Settings/"
    - "/display/KD/Emails%20Settings/"
    - "/x/tAFO/"
    - "/katalon-studio/docs/emails-settings/"
description: 
---

These settings allow you to define global email configurations to be used in other features of Katalon Studio. Katalon Studio allows users to receive summary reports via **Email** after **Test Suites** execution. You can access the settings at **Project > Settings > Email**.

> **Send test email** button only available once **Mail Server Settings** and **Recipients** are filled correctly.

## Configure Mail Server

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/emails-settings/email1.png" width="" height="">

**Mail Server Settings** define the mail server which Katalon Studio will use to send emails.

* **Host**: the domain name of the mail server.
* **Port**: the port to be used for that server.
* **Username** & **Password**: the account to authenticate with the server.
* **Protocol**: the protocol to communicate with the mail server (None, SSL, TLS).
* **Encrypt authentication data** is recommended for sensitive data protection.

> In case your email servers are using two-step authentication, please turn it off.
>
> For those who use Gmail & Yahoo! Mail, make sure to allow low secure apps to access your account. Follow the guide [here ](https://support.google.com/accounts/answer/6010255)for Gmail users, or [here](https://help.yahoo.com/kb/account/SLN27791.html) for Yahoo! Mail users.

Below is SMTP configuration for popular email servers:

**Gmail:**

* Host: _[smtp.gmail.com](http://smtp.gmail.com/)_
* Port: _465_
* Username: _Your full Gmail address (e.g. [yourusername@gmail.com](mailto:yourusername@gmail.com))_
* Password: Your Gmail password

**Yahoo! Mail:**

* Host: _[smtp.mail.yahoo.com](http://smtp.mail.yahoo.com/)_
* Port: _465_
* Username: _Your full Yahoo! Mail address (e.g. [yourusername@yahoo.com](mailto:yourusername@yahoo.com))_
* Password: _Your Yahoo! Mail password_

**Outlook:**

* Host: _[smtp.mail.outlook.com](http://smtp.mail.outlook.com/)_
* Port: _587 or 25_
* Username: _Your full Microsoft email address (e.g. [yourusername@outlook.com](mailto:yourusername@outlook.com))_
* Password: _Your Microsoft password_
* Protocol: _TLS_

## Edit Email Template

**Email Template** defines the list of emails to receive reports from Katalon Studio.

You can customize the body of the email by selecting **Edit Template** or **Project > Settings > Email > Template**. All fields in the template is editable. Click **Apply** when finished.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/emails-settings/email2.png" width="" height="">

Where:

| Variable | Description |
| --- | --- |
| hostName | Host's name |
| os | Operating system |
| Browser | Browser name and version |
| deviceId | Id of executed device |
| deviceName | Name of executed device |
| suiteId | Id of test suite |
| suiteName | Name of test suite |
| totalTestCases | total executed test cases |
| totalPassed | total passed test cases |
| totalFailed | total failed test cases |
| totalError | total error test cases |

## Configure Report Format

**Report Format** allows you to decide whether to include test execution report as email attachment or not. Specifically, you are given options to include **execution log** and configure which **report format** of test suite executions to be sent as attachments in the notification email.
