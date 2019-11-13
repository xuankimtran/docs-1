---
title: "Install and Setup TestOps On-Premise" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/testops-op-installation.html 
description: How to install and setup TestOps On-Premise
---

**Prerequisites:**
* [Install and setup a Postgres Database.]() 
* Download [TestOps On-Premise installer]() for your operating system.

## Run the installer
TestOps On-Premise allows the user to access to insightful features of Katalon TestOps for managing automation testing data imported from Katalon Studio in a restricted network environment..

1. Run the TestOps OP installer and follow the wizard setup.

* **Destination directory** – this is where TestOps OP will be installed.

* **TCP ports** – these are the HTTP connector port and control port TestOps OP will run on. Stick with the default unless you're running another application on the same port. 
* Configure to connect to your PostgreSQL Database with username and password.

2. TestOps OP will start up in your browser once the installation is complete with Activation Screen.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-op-installation/kt-op-license-activation.png)

3. Copy the **Machine ID** on Activate TestOps screen to generate the license for your machine.

4. Login to TestOps Cloud to generate the offline license for TestOps Om-Premise. Learn more in this [document]().

5. Import license to the TestOps On-Premise Activation Screen and click **Activate**.

6. After activation, you will be asked to create a default account.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-op-installation/kt-op-create-root-account.png)

7. Sign in using the recently created account.

8. Now, you are at the TestOps On-Premise Dashboard, and you can start by creating a new organization and inviting your team members to collaborate.
