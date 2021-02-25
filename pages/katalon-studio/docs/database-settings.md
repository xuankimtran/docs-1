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
This document shows which kind of databases and how to use each one that Katalon Studio supports in Data-driven testing (DDT).

To define a global database connection to be used in other features of Katalon Studio, access the settings at **Project > Settings > Database**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/database-settings/new-ui.png" width=70%>

Where:

* Username: The username for authentication in the connected database server.
* Password: The password for authentication in the connected database server.
* JDBC Driver: The ClassDriverName of the database that has a supported library connection (JDBC).
* Connection URL: The connection string of database server. Katalon Studio supports the following databases:
  * MySQL
  * SQLServer
  * Oracle
  * Postgre

> Starting from **version 7.0.0 and later**, Katalon Studio users can configure additional database sources with the supported JDBC Driver field.

## Supported Databases

 Katalon Studio supports the four following databases. For more details, please refer to the original documents as below:

- Built-in database sources:

    - [SQLServer](https://docs.microsoft.com/en-us/sql/connect/jdbc/connecting-to-sql-server-with-the-jdbc-driver?view=sql-server-ver15) (applied for Katalon Studio Enterprise license).

    - [Oracle](https://docs.oracle.com/database/121/JJDBC/urls.htm#JJDBC28268) (applied for Katalon Studio Enterprise license).

    - [Postgre](https://jdbc.postgresql.org/documentation/head/connect.html) (applied for Katalon Studio license). 

- External database source:

    > From **7.9 onwards**:
    >
    > MySQL is removed from Katalon Studio built-in function.

    - [MySQL](https://dev.mysql.com/doc/connectors/en/connector-j-reference-configuration-properties.html) (applied for Katalon Studio license).

    Additionally, the Kakalon Studio Enterprise license allows you to connect to the external database if it has JDBC (please refer to this [example](https://docs.katalon.com/katalon-studio/docs/database-settings.html#example)).

## Example

This example is to show how to create a test file from MariaDB.

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
