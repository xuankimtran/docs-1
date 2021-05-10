---
title: "How to implement Data-driven Testing with MySQL?"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/tutorials/how-to-implement-ddt-mysql.html 
description:
---

Prior to v8.0.0, MySQL is one of the libraries having built-in JDBC driver in Katalon Studio. From v8.0 onwards, the JDBC driver is no longer embedded in our tool. To continue using MySQL database, you need to add its driver to Katalon Studio. This document shows you how to configure MySQL database connection to keep it in use.

> See which libraries Katalon Studio supports built-in JDBC drivers [here](https://docs.katalon.com/katalon-studio/docs/database-settings.html#introduce-database-connection).

### Connect to MySQL database with an external JDBC driver

This section provides an usage example by connecting to MySQL database with its external JDBC driver.

**Requirements**

- Katalon Studio v8.0.0+.
- An active Katalon Studio Enterprise license.
- You have already set up MyQSL Database.
- MySQL Database is running.

To establish the connection:

1. Download the executable jar file [here](https://dev.mysql.com/downloads/connector/j/).
2. Go to **Project/Settings/Library Management** > **Add** the jar file to the external library.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/how-to-guides/configure_mysql/my-sql-jar-file.png" width=70%>

3. In **Project Settings**, go to **Database** to configure the database connection. 

    - Select **Secure User and Password** to enable **User** and **Password** for editing.
    - Input **User** name and **Password** used for authentication.
    - Enter **JDBC Driver**.
    - Enter **Connection URL**.
    - Click **Test Connection** to verify whether your database is connected successfully.

        <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/database-settings/database-settings.png" width=70%>

    - Click **Apply and Close** to complete the connection process.

Next: See [Manage Test Data](https://docs.katalon.com/katalon-studio/docs/manage-test-data.html#create-a-database-data).
