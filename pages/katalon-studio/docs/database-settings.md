---
title: "Database Settings" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/database-settings.html 
redirect_from:
    - "/display/KD/Database+Settings/"
    - "/display/KD/Database%20Settings/"
    - "/x/tgFO/"
    - "/katalon-studio/docs/database-settings/"
description: 
---
This document shows which kind of databases and how to use database sources that Katalon Studio supports in Data-driven testing.

To define a global database connection to be used in other features of Katalon Studio, access the settings at **Project > Settings > Database**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/database-settings/new-ui.png" width=70%>

Where:

* User: The username for authentication in the connected database server.
* Password: The password for authentication in the connected database server.
* JDBC Driver: The ClassDriverName of the database that has a supported library connection (JDBC).
* Connection URL: The connection string of database server. Katalon Studio supports the following databases.
  * For Katalon Studio license: MySQL and PostgreSQL.
  * For Katalon Studio Enterprise license: Oracle and SQL Server.

> Starting from **version 7.0.0 and later**, Katalon Studio users can configure additional database sources with the supported JDBC Driver field.

## Built-in database libraries

Katalon Studio provides you with the following built-in libraries list that allows the built-in database connection support.

- MySQL.
- SQL Server.
- Oracle SQL.
- PostgreSQL.

This section shows how to connnect MySQL database to Katalon Studio to conduct Data-driven testing.

**Requirements**:

- Katalon Studio v7.9 onwards.
- Setting up MySQL database.
- MySQL database is running.

To start the connection, go to **Project > Settings > Database**.

- Select "Secure User and Password" to enable "User" and "Password".
- Input "User" name, "Password", "JDBC Driver" and "Connection URL".
- Click **Test Connection** to check whether your database is connected to Katalon Studio. 

    Once the database is connected succesfully, the result is shown as below.
    
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/database-settings/database-settings.png" width=70%>

- Click **Apply and Close** to complete the connection process.

In addition, you can connect the external database libraries to Katalon Studio if they have JDBC driver using **Kakalon Studio Enterprise license**. For more details, please refer to the [External database sources with JDBC driver](https://docs.katalon.com/katalon-studio/docs/database-settings.html#how-jdbc-connection-works) section.

## External database libraries with JDBC driver

> **Kakalon Studio Enterprise license** is required to connect external database libraries to Katalon Studio.

This section provides guidance to connect to the external database that has JDBC driver via a specific example - Create a test file from MariaDB. 

1. Download the executable jar file of the library [here](https://downloads.mariadb.org/connector-java/2.4.4/) for connecting to MariaDB.

2. Create a new project and configure this project as below:

* In **External Libraries**: Add the downloaded library.

    ![image](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/database-settings/add.png)

* In **Database**: Enter the username and password used for authentication; and the ClassDriverName of the database that has the supported library connection (`JDBC`). Click **Test Connection**.

    ![image](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/database-settings/link.png)

3. Create a new Test Data File with the Database type.

4. Click **Edit Query**. In the **Database Connection and Query Settings** dialog, you can connect to the MariaDB to query data.

    ![image](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/database-settings/edit-query.png)

    ![image](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/database-settings/query-data.png)
