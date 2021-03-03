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

## Connect to Built-in database libraries

Katalon Studio provides you with the following built-in libraries list that allows the built-in database connection support.

- MySQL.
- SQL Server.
- Oracle SQL.
- PostgreSQL.

The following example illustrates how to connect to a built-in database by **Creating a test file from MyQSL**.

**Pre-requisites**:

- Katalon Studio v7.9 onwards.
- Setting up MySQL database.
- MySQL database is running.

To start the connection, go to **Project > Settings > Database**.

1. In **Database**,
    - Select "Secure User and Password" to enable "User" and "Password".
    - Input "User" name and "Password" used for authentication, "JDBC Driver" and "Connection URL".
    - Click **Test Connection** to check whether your database is connected to Katalon Studio. 

    Once the database is connected succesfully, the result is shown as below.
    
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/database-settings/database-settings.png" width=70%>

    - Click **Apply and Close** to complete the connection process.

2. Create a new **Test Data** with the "Database Data" type.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/database-settings/new-test-data.png" width=70%>

3. - Click **Edit Query** > select "Use global database connection settings" in the **Database Connection and Query Settings** dialog to use the database setting up in step 1 to query data.
    - Input **SQL Query** > click **OK**.

        <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/database-settings/SQL-query.png" width=70%>
    
        The result is shown as below:

        <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/database-settings/data.png" width=70%>

In addition, you can connect to the external database libraries if they have JDBC driver using **Kakalon Studio Enterprise license**. For more details, please refer to the [External database sources with JDBC driver](https://docs.katalon.com/katalon-studio/docs/database-settings.html#how-jdbc-connection-works) section.

## Connect to External database libraries with JDBC driver

> **Kakalon Studio Enterprise license** is required to connect external database libraries to Katalon Studio.

This section provides guidance to connect to an external database that has JDBC driver by **Creating a test file from MariaDB**.

**Pre-requisites**:

- Katalon Studio v7.9 onwards.
- Setting up MariaDB.
- MariaDB is running.

To start the connection:

1. Download the executable jar file of MariaDB library [here](https://downloads.mariadb.org/connector-java/2.4.4/).

2. Go to **Project > Settings > Library Management** to add the downloaded jar file > click **Apply**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/database-settings/mariadb-jar-file.png" width=70%>

3. In **Database**: 

    - Select "Secure User and Password" to enable "User" and "Password".
    - Input "User" name and "Password" used for authentication, "JDBC Driver" and "Connection URL".
    - Click **Test Connection** to check whether your database is connected to Katalon Studio.

        Once the database is connected succesfully, the result is shown as below.

        <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/database-settings/database-mariadb.png" width=70%>

    - Click **Apply and Close** to complete the connection process.

4. Create a new **Test Data** with the "Database Data" type.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/database-settings/new-test-data.png" width=70%>

5. - Click **Edit Query**. In the **Database Connection and Query Settings** dialog, you can connect to the MariaDB to query data.

    - Input **SQL Query** > click **OK**.

        <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/database-settings/secure-mariadb.png" width=70%>

        The result is shown as below:

        <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/database-settings/result-mariadb.png" width=70%>
