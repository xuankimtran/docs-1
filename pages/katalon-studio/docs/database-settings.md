---
title: "Set up Database Connection for Data-Driven Testing" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/database-settings.html 
redirect_from:
    - "/display/KD/Database+Settings/"
    - "/display/KD/Database%20Settings/"
    - "/x/tgFO/"
    - "/katalon-studio/docs/database-settings/"
description: 
---

> From v8.0 onwards, MySQL's JDBC Driver is removed from Katalon Studio's built-in libraries. To continue using it, follow [this guide](https://docs.katalon.com/katalon-studio/tutorials/how-to-implement-ddt-mysql.html).

This document gives you information on which database can be used for Data-driven testing and how to set up the database connection in Katalon Studio.

## Introduce Database Connection 

To do data-driven testing with a database, you can define a database connection that can be used for the whole project and override this global configuration in a test data file later. [Learn more](https://docs.katalon.com/katalon-studio/docs/manage-test-data.html#create-a-database-data)

To set up a global database connection, go to **Project** > **Settings** > **Database**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/database-settings/new-ui.png" width=70%>

**Where:**

- **Secure User and Password**: select to authenticate the connected database server, disabled by default.
- **User**: The username for authentication in the connected database server.
- **Password**: The password for authentication in the connected database server.
- **JDBC Driver**: The ClassDriverName of the database that has a supported library connection (JDBC).
- **Connection URL**: The connection string of the database server. Katalon Studio supports built-in JDBC Drivers for the following databases:
    - [SQL Server](https://docs.microsoft.com/en-us/sql/connect/jdbc/connecting-to-sql-server-with-the-jdbc-driver?view=sql-server-ver15).
    - [Oracle SQL](https://docs.oracle.com/database/121/JJDBC/urls.htm#JJDBC28268).
    - [PostgreSQL](https://jdbc.postgresql.org/documentation/head/connect.html).

You can set up a connection to one of those three database types with its executable jar file already embedded. Refer to the following table for an availability check: 
<p>&nbsp;</p>
<table>
<tbody>
<tr style="height: 35px;">
<td style="text-align: center; height: 35px;">&nbsp;</td>
<td style="text-align: center; height: 35px;">
<p><strong>Katalon Studio version</strong></p>
</td>
<td style="text-align: center; height: 35px;">
<p><strong>MySQL</strong></p>
</td>
<td style="text-align: center; height: 35px;">
<p><strong>PostgreSQL</strong></p>
</td>
<td style="text-align: center; height: 35px;">
<p><strong>Oracle SQL</strong></p>
</td>
<td style="text-align: center; height: 35px;">
<p><strong>SQL Server&nbsp;</strong></p>
</td>
</tr>
<tr style="height: 35px;">
<td style="text-align: center; height: 70px;" rowspan="2">
<p><strong>Katalon Studio license</strong></p>
</td>
<td style="text-align: center; height: 35px;">
<p><strong>7.0+</strong></p>
</td>
<td style="text-align: center; height: 140px;" rowspan="4">
<p><span style="font-weight: 400;">v8.0+</span></p>
</td>
<td style="text-align: center; height: 140px;" rowspan="4">
<p><span style="font-weight: 400;">all versions</span></p>
</td>
<td style="text-align: center; height: 70px;" rowspan="2">
<p><span style="font-weight: 400;">N/A</span></p>
</td>
<td style="text-align: center; height: 70px;" rowspan="2">
<p><span style="font-weight: 400;">N/A</span></p>
</td>
</tr>
<tr style="height: 35px;">
<td style="text-align: center; height: 35px;">
<p><strong>7.5+</strong></p>
</td>
</tr>
<tr style="height: 35px;">
<td style="text-align: center; height: 70px;" rowspan="2">
<p><strong>Katalon Studio Enterprise license</strong></p>
</td>
<td style="text-align: center; height: 35px;">
<p><strong>7.0+</strong></p>
</td>
<td style="text-align: center; height: 70px;" rowspan="2">
<p><span style="font-weight: 400;">all versions</span></p>
</td>
<td style="text-align: center; height: 35px;">
<p><span style="font-weight: 400;">2008 - 2016</span></p>
</td>
</tr>
<tr style="height: 35px;">
<td style="text-align: center; height: 35px;">
<p><strong>7.5+</strong></p>
</td>
<td style="text-align: center; height: 35px;">
<p><span style="font-weight: 400;">2008 - 2017</span></p>
</td>
</tr>
</tbody>
</table>
<p><br /><br /></p>

In case you want to use a version other than the version those built-in drivers are compatible with, learn more about [excluding built-in libraries](https://docs.katalon.com/katalon-studio/docs/external-libraries.html#exclude-built-in-libraries). 

For those who wish to connect to an external database having a JDBC driver, you need to install its executable jar file accordingly then tell Katalon Studio where to use it for connection. 

## Connect to a database with a built-in driver

The following example illustrates how to connect to a Postgre database that can be used in a whole project.

**Requirements**:

- You have already set up your Postgre database.
- Postgre database is running.

To establish a connection, go to **Project > Settings > Database**. In **Database**:
   
1. Select **Secure User and Password** to enable **User** and **Password**.
2. Input **User** name and **Password** used for authentication and **Connection URL**.
3. Click **Test Connection** to verify whether your database is connected successfully.
   
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/database-settings/postgre-db.png" width=65%>
4. Click **Apply and Close** to save your setting.

## Connect to a database with an external JDBC driver

This section provides a usage example by connecting to MariaDB, a database with an external JDBC driver.

**Requirements**:

- You have already set up MariaDB.
- MariaDB is running.
- An active Katalon Studio Enterprise license.

To start the connection:

1. Download the executable jar file of the MariaDB library [here](https://downloads.mariadb.org/connector-java/2.4.4/).
2. Go to **Project** > **Settings** > **Library Management** to **Add** the jar file > click **Apply**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/database-settings/mariadb-jar.png" width=65%>

3. In Project Settings, go to **Database**: 

    - Select **Secure User and Password** to enable **User** and **Password**.
    - Input **User** name and **Password** used for authentication and **Connection URL**.
    - Enter **JDBC Driver**.
    - Enter **Connection URL**.
    - Click **Test Connection** to verify whether your database is connected successfully. 

       <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/database-settings/database-mariadb.png" width=65%>

    - Click **Apply and Close** to complete the connection process.

Next: See [Manage Test Data](https://docs.katalon.com/katalon-studio/docs/manage-test-data.html#create-a-database-data)
