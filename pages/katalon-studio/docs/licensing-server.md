---
title: "Katalon Licensing Server" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/licensing-server.html
description: 
---
Katalon licensing server is a web-based application that provides dynamic perspectives and an insightful look at your automation testing data in a restricted network environment.

## Features
- Install and set up on your machine privately (within your internal network). [Learn more](https://docs.katalon.com/katalon-studio/docs/licensing-server.html#install-and-setup-a-server)
- Manage users & organizations. [Learn more](https://docs.katalon.com/katalon-analytics/docs/ktop.html#create-an-organization)
- Manage licenses. 
- Manage accounts (login, change & reset password). [Learn more](https://docs.katalon.com/katalon-analytics/docs/ktop.html#reset-and-forget-password)
- Configure mail server to send and receive notification about projects. [Learn more](https://docs.katalon.com/katalon-analytics/docs/ktop.html#configure-mail-server)
- Activate Katalon Studio with KTOP server. [Learn more](https://docs.katalon.com/katalon-analytics/docs/ktop.html#activate-katalon-studio-with-ktop-server)
- Use Katalon plugins with KTOP server. [Learn more](https://docs.katalon.com/katalon-analytics/docs/ktop.html#use-katalon-plugins-with-ktop-server)

## Install and setup a server

### Prerequisite

- Download [PostgreSQL Database version 9.6.16](https://www.postgresql.org/download/)
- For integration, Katalon Studio version should be 7.2.2
- Contact Katalon team to get the **Katalon licensing server package** and a **license file** (.lic file) to activate the licensing server.
Install and create a PostgreSQL database

PostgreSQL database is where you manage all data, including Organizations, Teams, and user accounts used in the server. Please first download [PostgreSQL Database version 9.6.16](https://www.postgresql.org/download/).

1. Run the PostgreSQL installer and follow the PostgreSQL Setup Wizard.

- Create a password for the database superuser (postgres)

  <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/ktop-server/3.PNG" width="" height=""> 

- Select the port number the server should listen on

  <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/ktop-server/4.PNG" width="" height=""> 

2. After installation, open **PgAdmin** which starts on your browser.

3. Sign in with the superuser's password.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/ktop-server/pgadmin.PNG" width="" height=""> 

4. Create a database named kit.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/ktop-server/kit.PNG" width="" height="">

> Note: You can use the default superuser postgres or create another Login role with the superuser's privileges.

### Install Katalon online licensing server

> Contact [Katalon Sales team](mailto:business@katalon.com) to get the package and license file. We recommend installing the versions that are compatible with your operating system (only Linux and Windows are supported).

1. Run the installer and follow the Setup Wizard.

- **Destination directory** – this is where KTOP will be installed in your machine

  <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/ktop-server/5.PNG" width="" height=""> 

- **TCP ports** – these are the HTTP connector and control ports that KTOP will run on. You're recommended to use the default ports unless you're running another application on the same port.


- **Database URL** – the JDBC URL for your database.


- **Server URL** - the address of your KTOP site. Syntax: http://<IPAddress>:<TCPPort>
E.g., http://localhost:8080

The server will start on your browser once the installation completes with the Activate screen.
You will receive a license file which is used to activate the server as below:

  <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/ktop-server/activate.PNG" width="" height="">

2. After activation, you will be asked to create a default account.

3. Sign in using the default account.

Now, you are at the server Dashboard. You can begin with creating a new organization and inviting your members to join.

