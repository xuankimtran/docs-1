---
title: "Install and Setup"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/testops-op-installation.html 
description: How to install and setup Katalon TestOps OnPremise
---
Katalon TestOps OnPremise (KTOP) allows you to access to insightful features of Katalon TestOps for managing automation testing data imported from Katalon Studio in a restricted network environment.

**Prerequisites:**

* Download [Postgres Database](https://www.postgresql.org/download/). KTOP only supports PostgreSQL from version 11 onwards. 

* Download [Katalon TestOps OnPremise installer]().

You're recommended to get the versions that are compatible with your operating system.

## Install and create PostgreSQL database

1. Run the PostgreSQL installer and follow the wizard setup.

2. After installation, sign in using your username and password.

3. **PgAdmin** will start up on your browser.

4. Create a kit database.

 ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-op-installation/postgresql-dashboard.png)

## Run the KTOP installer

1. Run the KTOP installer and follow the wizard setup.

* **Destination directory** – this is where KTOP will be installed in your machine.

* **TCP ports** – these are the HTTP connector port and control port KTOP will run on. Stick with the default unless you're running another application on the same port. 

* **Database URL** – the JDBC URL for your database.

* **Server URL** - this is the address you will use to access your KTOP site.

* **Install as service** - KTOP will be installed as a service.

2. KTOP will start up on your browser once the installation is complete with Activation Screen.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-op-installation/kt-op-activation-by-file.png)

3. Copy the **Machine ID** on Activate KTOP screen to generate the license for your machine.

4. Log in to [TestOps Cloud](https://analytics.katalon.com/) to generate an offline license for KTOP. [Learn more](https://docs.katalon.com/katalon-studio/docs/license-management.html#create-and-assign-an-offline-rekse-license).

5. Import the license to the KTOP Activation Screen and click **Activate**.

6. After activation, you will be asked to create a default account.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-op-installation/kt-op-create-root-account.png)

7. Sign in using the default account.

Now, you are at the KTOP Dashboard, and you can start by creating a new organization and inviting your team members to collaborate.

> Note: You need to configure the mail server to send and receive email notification. [Learn more](https://docs.katalon.com/katalon-analytics/docs/kt-op-mail-server.html).
