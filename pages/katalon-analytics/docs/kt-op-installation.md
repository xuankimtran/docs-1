---
title: "Install and Setup TestOps OnPremise"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/testops-op-installation.html 
description: How to install and setup TestOps OnPremise
---
TestOps OnPremise allows you to access to insightful features of Katalon TestOps for managing automation testing data imported from Katalon Studio in a restricted network environment.

**Prerequisites:**

* Download [Postgres Database](https://www.postgresql.org/download/) capatible with your operating system. TestOps OnPremise only supports PostgreSQL from version 11 onwards. 

* Download [TestOps OnPremise installer]() capatible with your operating system.

## Install and create PostgreSQL database

1. Run the PostgreSQL installer and follow the wizard setup.

2. After installation, sign in using your username and password.

3. PgAdmin will start up in your browser.

4. Create a kit database.

 ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-op-installation/postgresql-dashboard.png)

## Run the TestOps OnPremise installer

1. Run the KTOP installer and follow the wizard setup.

* **Destination directory** – this is where KTOP will be installed in your machine.

* **TCP ports** – these are the HTTP connector port and control port TestOps OP will run on. Stick with the default unless you're running another application on the same port. 

* **Database URL** – the JDBC URL for your database.

* **Server URL** - this is the address you will use to access your KTOP site.

* **Install as service** - KTOP will install as service.

2. KTOP will start up in your browser once the installation is complete with Activation Screen.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-op-installation/kt-op-activation-by-file.png)

3. Copy the **Machine ID** on Activate TestOps OnPremise screen to generate the license for your machine.

4. Login to [TestOps Cloud](https://analytics-staging.katalon.com/) to generate the offline license for KTOP. [Learn more]().

5. Import license to the KTOP Activation Screen and click **Activate**.

6. After activation, you will be asked to create a default account.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-op-installation/kt-op-create-root-account.png)

7. Sign in using the recently created account.

8. Now, you are at the TestOps OnPremise Dashboard, and you can start by creating a new organization and inviting your team members to collaborate.

> Note: You need to configure the mail server to send and receive email notification. [Learn more]().
