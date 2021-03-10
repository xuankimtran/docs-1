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
This document gives you information on which database can be used for Data-driven testing and how to set up the database connection in Katalon Studio.

To define a global database connection to be used in other features of Katalon Studio, access the settings at **Project > Settings > Database**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/database-settings/new-ui.png" width=70%>

Where:
- Secure User and Password: select to authenticate the connected database server, disable by default.
- User: The username for authentication in the connected database server.
- Password: The password for authentication in the connected database server.
- JDBC Driver: The ClassDriverName of the database that has a supported library connection (JDBC).
- Connection URL: The connection string of the database server. Katalon Studio supports the following databases.
    - [MySQL](https://dev.mysql.com/doc/connectors/en/connector-j-reference-configuration-properties.html).
    - [SQL Server](https://docs.microsoft.com/en-us/sql/connect/jdbc/connecting-to-sql-server-with-the-jdbc-driver?view=sql-server-ver15).
    - [Oracle SQL](https://docs.oracle.com/database/121/JJDBC/urls.htm#JJDBC28268).
    - [PostgreSQL](https://jdbc.postgresql.org/documentation/head/connect.html).

## Connect to Built-in database libraries

Katalon Studio provides you with the following built-in libraries list that allows the built-in database connection support.

- For Katalon Studio license: 
    - MySQL up to version 8.0.15.
    - PostgreSQL up to version 42.2.17.
- For Katalon Studio Enterprise license: 
    - Oracle SQL up to version 12.1.0.2.
    - SQL Server 2008 - 2017, Azure SQL Database.

từ v7.0 thì mình support MySQL 8.0+
từ v7.5 thì mình support Microsoft SQL Server 2017
còn lại là đã sp từ version 5.x


The following example illustrates how to connect to a built-in database by **Creating a test file from Postgre**.

**Requirements**:

- Katalon Studio version 7.0 onwards.
- Setting up Postgre database.
- Postgre database is running.

To start the connection, go to **Project > Settings > Database**.

1. In **Database**:
    - Select "Secure User and Password" to enable "User" and "Password".
    - Input "User" name and "Password" used for authentication, "JDBC Driver" and "Connection URL".
    - Click **Test Connection** to verify whether your database is connected on Katalon Studio. 

    Once the database is connected successfully, the result is shown below.
    
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/database-settings/postgre-db.png" width=65%>

    - Click **Apply and Close** to complete the connection process.

2. Create a new **Test Data** with the "Database Data" type.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/database-settings/new-test-data.png" width=65%>

3. - Click **Edit Query** > select "Use global database connection settings" in the **Database Connection and Query Settings** dialog to use the database setting up in step 1 to query data.
    - Input **SQL Query** > click **OK**.

        <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/database-settings/SQL-query.png" width=65%>
    
        The result is shown as below:

        <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/database-settings/data.png" width=70%>

In case you want to use a version other than the built-in one, learn more about [Exclude built-in libraries](https://docs.katalon.com/katalon-studio/docs/external-libraries.html#exclude-built-in-libraries). 


## Connect to External database libraries with JDBC driver

> **The difference between built-in and external JDBC driver:**
> - For built-in libraries, Katalon Studio has embedded the executable jar files of those databases for usage.
> - For external libraries, users need to install the database's executable jar file then tell Katalon Studio where to use it for connecting to the database.
>
> **Kakalon Studio Enterprise license** is required to connect to external database libraries.

This section provides guidance to connect to an external database with a JDBC driver by **Creating a test file from MariaDB**.

**Requirements**:

- Katalon Studio version 7.0 onwards.
- Setting up MariaDB.
- MariaDB is running.
- An active Katalon Studio Enterprise license.

To start the connection:

1. Download the executable jar file of MariaDB library [here](https://downloads.mariadb.org/connector-java/2.4.4/).

2. Go to **Project > Settings > Library Management** to add the downloaded jar file > click **Apply**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/database-settings/mariadb-jar-file.png" width=65%>

3. In **Database**: 

    - Select "Secure User and Password" to enable "User" and "Password".
    - Input "User" name and "Password" used for authentication, "JDBC Driver" and "Connection URL".
    - Click **Test Connection** to verify whether your database is connected on Katalon Studio.

        Once the database is connected successfully, the result is shown below.

        <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/database-settings/database-mariadb.png" width=65%>

    - Click **Apply and Close** to complete the connection process.

4. Create a new **Test Data** with the "Database Data" type.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/database-settings/test-data-mariadb.png" width=65%>

5. - Click **Edit Query**. In the **Database Connection and Query Settings** dialog, you can connect to the MariaDB to query data.

    - Input **SQL Query** > click **OK**.

        <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/database-settings/secure-mariadb.png" width=65%>

        The result is shown below:

        <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/database-settings/result-mariadb.png" width=70%>
