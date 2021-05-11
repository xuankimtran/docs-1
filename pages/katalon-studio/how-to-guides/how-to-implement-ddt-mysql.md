---
title: "How to implement Data-driven Testing with MySQL?"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/how-to-guides/how-to-implement-ddt-mysql.html
redirect_from:
    - "/katalon-studio/tutorials/how-to-implement-ddt-mysql.html"
description:
---

Before v8.0.0, MySQL is among the libraries having built-in JDBC driver in Katalon Studio. From v8.0 onwards, the JDBC driver is no longer embedded in our tool. To continue using MySQL database, you need to add its driver to Katalon Studio. See which libraries Katalon Studio supports built-in JDBC drivers [here](https://docs.katalon.com/katalon-studio/docs/database-settings.html#introduce-database-connection).

This document shows you how to add a driver for MySQL database connection to keep it in use.

**Requirements**

- Katalon Studio v8.0.0+.
- You have already set up MyQSL Database.
- MySQL Database is running.

### Add an external JDBC driver for MySQL database connection

Do as follows:

1. Download the executable jar file [here](https://dev.mysql.com/downloads/connector/j/).
2. Go to **Project/Settings/Library Management** > **Add** the jar file to the external library.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/how-to-guides/configure_mysql/my-sql-jar-file.png" width=70%>

3. In **Project Settings**, go to **Database** to configure the database connection.

    - Select **Secure User and Password** to enable **User** and **Password** for editing.
    - Input **User** name and **Password** used for authentication.
    - Enter **Connection URL**.
    - Click **Test Connection** to verify whether your database is connected successfully.

        <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/database-settings/database-settings.png" width=70%>

    - Click **Apply and Close** to complete the connection process.

Next: See [Manage Test Data](https://docs.katalon.com/katalon-studio/docs/manage-test-data.html#create-a-database-data).
