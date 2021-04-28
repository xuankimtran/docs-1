---
title: "Install TestOps On-premises with Docker" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/kt_install_premises_docker.html 
redirect_from:
    - "/katalon-analytics/docs/kt_install_premises_docker/"
description: 
---

* Step 1: Install Docker for Windows (Hyper-V should be enabled).
* Step 2: Allow Remote Access to PostgreSQL database:

1. Open **pg_hba.conf** file in an editor.

   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt_install_premises_docker/kt_open_pg_hba.png)

2. Add an entry of the host IP address from which you try to connect. You can input the entry of the host to which you would like to provide access to as shown in the image.

   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt_install_premises_docker/kt_entry_host.png)

3. Restart the postgres SQL server.

   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt_install_premises_docker/kt_restart_sql_server.png)

* Step 3: Install Postgres 9.6. and connect to Postgres depend on default postgres_user = “postgres“ and password set by user when install.

   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt_install_premises_docker/kt_install_connect_postgres.png)

* Step 4: Create a database with name “kit“.

   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt_install_premises_docker/kt_create_database_kit.png)

* Step 5: Update docker-compose.yml.

   Replace <DB_HOST> with database host (IP address of the machine which the database installed in). Ex: 172.18.63.97

   Replace <DB_PORT> with database port. Ex: 9999

   Replace <DB_USERNAME> with database username

   Replace <DB_PASSWORD> with database password

   Replace <FILE_STORAGE_URL> with the location which report files are stored in

   Add an environment variable to testops service named KIT_SERVER_URL with  the address of your site. E.g. http://172.18.63.97:8080

   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt_install_premises_docker/kt_docker_compose.png)

* Step 6: Load TestOps image from tar file running: docker load -i testops.tar.

   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt_install_premises_docker/kt_run_docker_load.png)

* Step 7: docker-compose up -d.

   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt_install_premises_docker/kt_docker_compose_up.png)

   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt_install_premises_docker/kt_docker_compose_up_1.png)
