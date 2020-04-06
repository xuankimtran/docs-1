---
title: "Setup an OnPremise License Server in Linux (Ubuntu)" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/license-server-ubuntu.html
description: 
---
## Prerequisites

- A folder where you want to store report files
- An OnPremise license server package (.sh file)


## Grant permission for the report file

To grant permissions for the report file, use the following command:


```groovy
cd TestOps
chmod 777 testops-linux.sh
sudo ./testops-linux.sh
```


Then provide your password and follow the instructions.


```
Click Next to continue, or Cancel to exit Setup.

Select the folder where you would like TestOps to be installed, then click Next.

Where should TestOps be installed?
[/opt/testops]

Configure which port TestOps will use

TestOps requires a TCP port that is not being used by any other applications on this machine. The HTTP port is where you will access TestOps through your browser.

HTTP Port Number
[8080]
```


Note: You can change the ports or keep the default ones.


## Configure database information


Configure your database username, password, host, database name to link with the license server. For example:

```groovy
Username:
[katalon]
postgres
Password:

Database URL:
[localhost:5433/kit]

Configure other info
Upload location:
[/root/testops]
/home/katalon/testops
```



- **TCP ports** – these are the HTTP connector and control ports that the license server will run on. You're recommended to use the default ports unless you're running another application on the same port.

- **Database URL** – the JDBC URL for your database.

- **Server URL** - the address of your license server site. Syntax: http://: E.g., http://localhost:8080

- **Upload location** - a location of the folder that you have created at the beginning. For example: `/home/katalon/testops`.


Congratulations! The license server is now ready on your machine. You can check by opening the server in a browser.


