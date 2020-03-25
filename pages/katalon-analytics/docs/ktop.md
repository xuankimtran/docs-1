---
title: "Setup Katalon TestOps OnPremise" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/ktop.html
redirect_from:
    - "/katalon-analytics/docs/ktop-overview.html"
    - "/katalon-analytics/docs/kt-op-installation.html"
    - "/katalon-analytics/docs/ktop-setup-org-team-project.html"
    - "/katalon-analytics/docs/kt-op-mail-server.html"
description: 
---
**Katalon TestOps OnPremise (KTOP)** is a web-based application that provides dynamic perspectives and an insightful look at your automation testing data in a **restricted network environment**. You can leverage your automation testing data by transforming and visualizing your data, analyzing test results, and seamlessly integrating with such tools as Katalon Studio and Jira.

## Benefits

* Save time spent reviewing and analyzing test execution results.
* Provide insightful visualizations on critical testing data.
* Quickly troubleshoot your testing process and identify defects by locating exactly which test case failed.
* Smoothly integrate with your issues and releases in Jira.
* Maximize your testing capacity.

## Key Features

* Install and setup on your machine privately.
* Configure mail server to send and receive notification about projects.
* Import KTOP license generated from Katalon TestOps.
* And other features of KT are also included in KTOP. [Learn more.](https://docs.katalon.com/katalon-analytics/docs/overview.html)

## Install and Setup

> Prerequisites: 
>
> * Download PostgreSQL Database version 9.6.16
> * For integration, Katalon Studio version should be 7.2.2
> * Contact Katalon Sales team to get the Katalon TestOps OnPremise installer.

### Install and create a PostgreSQL database

PostgreSQL database is where you manage all data, including test executions, Organizations, Teams, Projects and user accounts used by KTOP. Please first download [PostgreSQL Database version 9.6.16](https://www.postgresql.org/download/).

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

### Install Katalon TestOps OnPremise

Contact [Katalon Sales team](mailto:business@katalon.com) to get the Katalon TestOps OnPremise installer. We recommend installing the versions that are compatible with your operating system (only Linux and Windows are supported).

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

Now, you are at the KTOP Dashboard. First, you can start by creating a new organization and inviting your team members. Please refer to [this tutorial](https://docs.katalon.com/katalon-analytics/docs/ktop-usage.html) to learn how to set up an Organization properly in Katalon TestOps OnPremise, and to create teams and projects. 

