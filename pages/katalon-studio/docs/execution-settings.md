---
title: "Project Settings" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/execution-settings.html 
redirect_from:
    - "/display/KD/Execution+Settings/"
    - "/display/KD/Execution%20Settings/"
    - "/x/cgFO/"
    - "/katalon-studio/docs/execution-settings/"
    - "/katalon-studio/docs/emails-settings.html"
    - "/display/KD/Emails+Settings/"
    - "/display/KD/Emails%20Settings/"
    - "/x/tAFO/"
    - "/katalon-studio/docs/emails-settings/"
    - "/display/KD/Network+Settings/"
    - "/display/KD/Network%20Settings/"
    - "/x/gQ1O/"
    - "/katalon-studio/docs/network-settings/"
    - "/katalon-studio/docs/network-settings.html"
description:
---

## Execution Settings

Execution settings help users to set preferred behaviors for Katalon Studio during test execution. You can configure general execution preferences by accessing from the main menu: **Project > Settings > Execution**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-settings/execution-settings.png" width="" height="">

### Allow editing JVM parameters in Execution Settings

> Starting in version 7.2.4, Katalon Studio Enterprise users can edit VM arguments in Execution Settings.

VM Arguments entered in **Executions Settings** of a project change the behaviour of a Java process of each execution. Currently, Katalon Studio does not support VM arguments' values containing space. Below is a list of most used JVM Parameters:

Specify minimal and maximal heap sizes

* `-Xms<heap size>[unit]`
* `-Xmx<heap size>[unit]`
* `-XX:MaxMetaspaceSize=<metaspace size>[unit]`

Garbage Collection implementation types

* Serial Garbage Collector: `-XX:+UseSerialGC`
* Parallel Garbage Collector: `-XX:+UseParallelGC`
* CMS Garbage Collector: `-XX:+USeParNewGC`
* G1 Garbage Collector: `-XX:+UseG1GC`

Garbage Collection Logging

* Specify the log file rolling policy: `-XX:+UseGCLogFileRotation`
* Denote the max number of log files that can be written for a single application life cycle: `-XX:NumberOfGCLogFiles=< number of log files >`
* Specify the max size of the file: `-XX:GCLogFileSize=< file size >[ unit ]`
* Denote the file's location: `-Xloggc:/path/to/gc.log`

Handling Out of Memory

* Dump heap into physical file in case of OutOfMemoryError: `-XX:+HeapDumpOnOutOfMemoryError`
* Denote the path where the file is to be written: `-XX:HeapDumpPath=./java_pid<pid>.hprof`
* Issue emergency commands to be executed in case of out of memory error: `-XX:OnOutOfMemoryError="< cmd args >;< cmd args >"`
* Limits the proportion of the VM's time that is spent in GC before an OutOfMemory error is thrown: `-XX:+UseGCOverheadLimit`

Go to **Project > Settings > Execution > Launch Arguments**. In the **VM Arguments** tab, enter your arguments.

Below is an example:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-settings/settings.png" width="" height="">

To make sure if the configuration works, please add this simple test case:

```groovy
import com.kms.katalon.core.util.KeywordUtil
KeywordUtil.logInfo(System.getProperty("testme"))
```

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-settings/hello.png" width="" height="">

### Default Execution Settings

* **Default execution**: The default environment that Katalon Studio uses for executing test scripts.

* **Default Smart Wait**: to tell the web driver to wait for the web page to become static before any operations perform. [Learn more](https://docs.katalon.com/katalon-studio/docs/webui-smartwait.html).

* **Default wait for element timeout**: The default timeout period (in seconds) that Katalon Studio waits for the application under test to be loaded when executing automation test.

* **Log executed test steps**: to decide whether the logs include executed test steps or not. [Learn more](https://docs.katalon.com/katalon-studio/docs/working-with-execution-log.html#log-executed-test-steps).

* **Post-Execution Options**: These options decide the actions that Katalon Studio performs after finishing test execution.

  * Open report: Specify whether the report generated after your test suite's execution finishes is to be opened immediately.
  * Terminate drivers: Specify when any driver remains after execution is terminated.

### WebUI Settings

These settings decide the general behavior of Katalon Studio when executing WebUI testing.

* **Delay between actions**: The time for Katalon Studio to wait between test steps when executing test cases.
* **Default wait when IE hangs**: Specify the default period of waiting that Katalon Studio should use in case IE hangs.
* **Default page load timeout**:

  * *Wait until the page is loaded*: Katalon Studio waits for the web page to load completely.
  * *Wait for (in seconds)*: The default timeout period (in seconds) that Katalon Studio waits for the web page to load.

## Emails Settings

These settings allow you to define global email configurations to be used in other features of Katalon Studio. Katalon Studio allows users to receive summary reports via **Email** after **Test Suites** execution. You can access the settings at **Project > Settings > Email**.

> **Send test email** button only available once **Mail Server Settings** and **Recipients** are filled correctly.

### Configure Mail Server

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

### Edit Email Template

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

### Configure Report Format

**Report Format** allows you to decide whether to include test execution report as email attachment or not. Specifically, you are given options to include **execution log** and configure which **report format** of test suite executions to be sent as attachments in the notification email.

## Network settings

### Certificate settings

Katalon Studio supports the capability to bypass certificate validation so that users with protected network policy can work with Katalon Studio as usual. Go to **Project > Settings > Network**:

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/project-settings-network.png)

You are giving two options, including **None** or **Bypass certificate validation**.

* None
* Bypass certificate validation

The configuration here affects both WebUI and Web Service testings.

### Client certificate settings

> Please be noted that the setting for **Client certificate** is only available for **Katalon Studio Enterprise** users.
>
> This setting is only applied for requests in API/Web Services projects.

Katalon Studio can be configured to use the Client Certificate for all requests. To sign all the requests from Katalon Studio, specify the full path to your KeyStore file and the KeyStore Password. The recommended key store format is **PKCS #12** (.p12).

#### Create a Certificate

To generate public and private key pairs (KeyStore and KeyStore Password) for the above configuration, you can use the keytool utility that is included in the JDK installation.

1. Open the command prompt and navigate to the bin folder in the JDK folder.

2. Run this command to create a KeyStore:

   `keytool -genkey -alias katalon -keyalg RSA -keystore katalon.keystore`

3. Enter a password for the new KeyStore and provide the utility with the required information (your name, the name of your organization, and etc).

To export a certificate with your public key, run the this command:
`keytool -export -alias katalon -file katalon.cer -keystore katalon.keystore`.
