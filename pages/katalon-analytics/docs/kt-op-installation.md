---
title: "Install and Setup"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/kt-op-installation.html
description: How to install and setup Katalon TestOps OnPremise
---
Katalon TestOps OnPremise (KTOP) allows you to access insightful features of Katalon TestOps for managing automation testing data imported from Katalon Studio in a restricted network environment.

**Prerequisites:**

* Download [PostgreSQL Database version 9.6.16](https://www.postgresql.org/download/)

* Contact [Katalon Sales](mailto:business@katalon.com) team to get the Katalon TestOps OnPremise installer.

We recommend installing the versions that are compatible with your operating system (only Linux and Windows are supported).

## Install and create PostgreSQL database

1. Run the **PostgreSQL** installer and follow the PostgreSQL Setup Wizard.

* Provide a password for the database superuser (postgres)

  <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/ktop-server/3.PNG" width="" height=""> 

* Select the port number the server should listen on

  <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/ktop-server/4.PNG" width="" height=""> 

2. After installation, open **PgAdmin** which starts on your browser.

3. Sign in with the superuser's password.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/ktop-server/pgadmin.PNG" width="" height=""> 

4. Create a database named **kit**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/ktop-server/kit.PNG" width="" height="">

> You can use the default superuser **postgres** or create another Login role with the superuser's privileges.

## Install Katalon TestOps OnPremise

1. Run the KTOP installer and follow the Setup Wizard.

* **Destination directory** – this is where KTOP will be installed in your machine.

  <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/ktop-server/5.PNG" width="" height=""> 

* **TCP ports** – these are the HTTP connector and control ports that KTOP will run on. You're recommended to use the default ports unless you're running another application on the same port.

  <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/ktop-server/defaultport.PNG" width="" height="">


  <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/ktop-server/tomcat2.PNG" width="" height="">
  
* **Database URL** – the JDBC URL for your database.
   
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/ktop-server/config_db.PNG" width="" height="">

* **Server URL** - the address of your KTOP site. Syntax: http://<_IPAddress_>:<_TCPPort_>. E.g., http://localhost:8080

2. KTOP will start on your browser once the installation completes with the **Activate TestOps** screen.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/ktop-server/activate.PNG" width="" height="">

3. On [Katalon TestOps](https://analytics.katalon.com/) Cloud, generate an offline license for KTOP using the Machine ID on the **Activate TestOps** screen. [Learn more](https://docs.katalon.com/katalon-studio/docs/license-management.html#create-and-assign-an-offline-rekse-license).

4. On the Activate TestOps Screen, choose the newly generated license file and click **Activate**.

5. After activation, you will be asked to create a default account.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/ktop-server/account.PNG" width="" height="">

7. Sign in using the default account.

Now, you are at the KTOP Dashboard. First, you can start by creating a new organization and inviting your team members.

> Note: You need to configure the mail server to send and receive email notifications. [Learn more](https://docs.katalon.com/katalon-analytics/docs/kt-op-mail-server.html).
