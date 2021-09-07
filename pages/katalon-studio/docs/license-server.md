---
title: "On-Premises License Server"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/license-server.html
description: 
---

> Notes:
>
> * Only applicable to users with an On-Premises package.
>
> * For existing On-Premises users, contact our Sales team at business@katalon.com for data migration.  

The Katalon On-Premises License Server allows installation at the client's network location.

The License Server allows you to activate Katalon Studio offline.

To acquire the Katalon On-Premises License Server, contact our Sales team at business@katalon.com.

## Features

The following features are available for users of a Katalon Studio On-Premises License Server:

* Private installation and setup (within your internal network).
* User and organization management.
* License management.
* Katalon Studio subscription.

## System requirements

<table><thead><tr><th>&nbsp;</th><th>Requirements</th></tr></thead><tbody><tr><th>Operating System</th><td>MacOS, Windows, Linux (Ubuntu based)</td></tr><tr><th>CPU</th><td>Minimum 4</td></tr><tr><th>Memory</th><td><p</p><p>Minimum 8 GB RAM (64-bit)</p><p><em.</p><p></p><p><em</p><p><em></p></td></tr><tr><th>Hard Drive</th><td>At least 40 GB available hard disk space.</td></tr></tbody></table>

> Notice:
>
> The current On-Premises License Server does not support M1 chip (macOS).

## Set up Docker

* To install Docker for Windows, see [Install Docker Desktop for Windows](https://docs.docker.com/desktop/windows/install/) (Hyper-V should be enabled).
* To install Docker for MacOS, see [Install Docker Desktop for Mac](https://docs.docker.com/desktop/mac/install/).

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-aug-license-server/docker-resources.png" width=80% alt="docker resources">

## Install and setup an On-Premises License Server (for Windows)

> Requirements:
>
> * You have downloaded [PostgreSQL database version 10 onwards](https://www.postgresql.org/download/).
> * Katalon Studio version 7.2.2 onwards (for Katalon Studio Enterprise).
> * Katalon License Server installer and a license file for activation. To acquire them, contact our Sales team at business@katalon.com.

### Install and create a PostgreSQL database

PostgreSQL database is where you manage all data including organizations, teams, and user accounts used in the server.

Follow these steps:
1. Download [PostgreSQL database](https://www.postgresql.org/download/).

2. Run the PostgreSQL installation and follow the PostgreSQL setup instructions.

* Create a password for the database superuser (postgres).

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/ktop-server/3.PNG"  width=60% alt="prosgres password">
  
* Select the port number the server should listen on.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/ktop-server/4.PNG"  width=60% alt="prosgres port">

3. After installation, open PgAdmin on your browser.

4. Sign in with the superuser's password.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/ktop-server/pgadmin.PNG" width=60% alt="pgadmin page">

5. Create a database named *kit*. 

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/ktop-server/kit.PNG" width=60% alt="kit database">

6. Create a database named *k1*.

> Notes:
>
> You can use the default PostgreSQL superuser or create another login role with the superuser's privileges.

### Install and set up the Katalon License Server

> Notes:
>
> Contact our Sales team at business@katalon.com for the On-Premises package and license file. We recommend you install the version that is compatible with your operating system.

1. Run the Katalon License Server installer and follow the setup instructions.

* **Destination directory**: the location where the License Server is installed in your machine.
   
* **TCP ports**: the HTTP connector and control ports which the License Server runs on.

   > Notes:
   >
   > We recommend you use the default ports (unless you're running another application on the same port).

* **Database URL**: the JDBC URL for your database.

* **Server URL**: the address for the License Server's site (e.g., http://localhost:8080).

   After completing the installation, the server starts on your browser.
   
2. Activate the server with the license file you have received.

3. Create a root user to login.

4. Sign in using the newly-created account.

You have set up the server successfully. 

## Install and setup an On-Premises License Server (for MacOS)


> Requirements:
>
> * You have downloaded [PostgreSQL database version 10 onwards](https://www.postgresql.org/download/).
> * Katalon Studio version 7.2.2 onwards (for Katalon Studio Enterprise).
> * Katalon License Server installer and a license file for activation. To acquire them, contact our Sales team at business@katalon.com.

Follow these steps:

1. Install the Katalon License Server.
2. Install [PostgreSQL](https://www.postgresql.org/download/macosx/).
3. Edit the *pg_hba.conf* file and add the following entry.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-aug-install-onpremises-docker/edit-prosgresql.png" width=100% alt="add entry hba conf">

4. Create a database.

   `docker run --name postgres -dp 5432:5432 -e POSTGRES_PASSWORD=admin postgres:alpine`

5. Create the database *kit* in DBeaver.
6. Create the database *k1* in DBeaver.
7. Edit .env file.

   ```
   LICENSE_SERVER_VERSION=latest
   LICENSE_SERVER_PORT=80
      
   DB_HOST=192.168.250.103
   DB_PORT=5432
   DB_USERNAME=postgres
   DB_PASSWORD=admin
   LICENSE_SERVER_URL=http://192.168.250.103
   ```

8. Use the following commands to run.

   <table>
   <tbody>
   <tr>
   <td>Load image</td>
   <td>docker&nbsp;load&nbsp;-I&nbsp;images.tar.gz</td>
   </tr>
   <tr>
   <td>Start image</td>
   <td>docker-compose&nbsp;up&nbsp;-d.</td>
   </tr>
   <tr>
   <td>Unload image</td>
   <td>docker-compose&nbsp;down</td>
   </tr>
   </tbody>
   </table>

9. Activate the License Server.

## Activate Katalon Studio offline

> Requirements:
>
> You have downloaded Katalon Studio.

You need to activate the License Server in the **Katalon Studio Activation** dialog.

1. Open the **Katalon Studio Activation** dialog in Katalon Studio.
2. Fill in the required information.

* In the **Server URL** section, enter the address of your License Server's site that you have configured.
* In the **Email** and **Password** sections, enter the account you have registered with the Katalon On-Premises License Server.

3. Click **Activate** to connect with your License Server and retrieve your organizations.
4. Select an Organization you want to work on, then click **OK**.
