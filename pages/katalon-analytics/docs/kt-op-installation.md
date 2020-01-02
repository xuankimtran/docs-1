---
title: "Install and Setup"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/testops-op-installation.html
description: How to install and setup Katalon TestOps OnPremise
---
Katalon TestOps OnPremise (KTOP) allows you to access insightful features of Katalon TestOps for managing automation testing data imported from Katalon Studio in a restricted network environment.

**Prerequisites:**

* Download [Postgres Database](https://www.postgresql.org/download/). KTOP only supports PostgreSQL from version 11.

* Contact [Katalon Sales](mailto:business@katalon.com) team to get the Katalon TestOps OnPremise installer.

You're recommended to get the versions that are compatible with your operating system. (Only Linux and Windows supported).

## Install and create PostgreSQL database

1. Run the **PostgreSQL** installer and follow the wizard setup.

2. After installation, sign in using your Username and Password.

3. **PgAdmin** starts on your browser.

4. Create a database named **kit**.

 ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-op-installation/postgresql-dashboard.png)

## Run the KTOP installer

1. Run the KTOP installer and follow the wizard setup.

* **Destination directory** – this is where KTOP will be installed in your machine.

* **TCP ports** – these are the HTTP connector and control ports that KTOP will run on. You're recommended to use the default ports unless you're running another application on the same port. 

* **Database URL** – the JDBC URL for your database.

* **Server URL** - the address of your KTOP site. Syntax: http://<_IPAddress_>:<_configport_>. E.g., http://localhost:8080

* **Install as service** - KTOP will be installed as a service.

2. KTOP will start on your browser once the installation completes with the Activate TestOps screen.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-op-installation/kt-op-activation-by-file.png)

3. On [Katalon TestOps](https://analytics.katalon.com/) Cloud, generate an offline license for KTOP using the Machine ID on the **Activate TestOps** screen. [Learn more](https://docs.katalon.com/katalon-studio/docs/license-management.html#create-and-assign-an-offline-rekse-license).

4. On the Activate TestOps Screen, choose the newly generated license file and click **Activate**.

5. After activation, you will be asked to create a default account.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-op-installation/kt-op-create-root-account.png)

7. Sign in using the default account.

Now, you are at the KTOP Dashboard. First, you can start by creating a new organization and inviting your team members.

> Note: You need to configure the mail server to send and receive email notifications. [Learn more](https://docs.katalon.com/katalon-analytics/docs/kt-op-mail-server.html).
