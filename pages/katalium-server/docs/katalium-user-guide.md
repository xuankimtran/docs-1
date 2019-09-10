---
title: "Get Started" 
sidebar: katalon_studio_docs_sidebar
permalink: katalium-server/docs/katalium-user-guide.html 
description: User guide for Katalium end-user.
---

## Set up Katalium Server

1. Install Java. The recommended version is Java 8.

2. Download and extract the latest release of the Katalium Server from [here](https://github.com/katalon-studio/katalium-server/releases). The `kata-server.jar` can be executed in Standalone, Grid Hub, or Grid Node modes.

3. Set up Katalium Server by using Command Line.

### Standalone mode

To start the server in the standalone mode, execute `standalone.sh` file (in macOS and Linux) or `standalone.bat` file (in Windows) with these commands:

```
cd katalium-server
standalone.bat
```

```
cd katalium-server
chmod u+x ./standalone.sh
./standalone.sh
```

Successfully activated Katalium Server will be displayed as belows:

![](https://github.com/katalon-studio/docs-images/raw/master/katalium-server/docs/katalium-user-guide/1-standalone-mode.png)

When you activate the server for the first time, you have to enter the email and password of your Katalon Account. It is recommended to use Katalon API Keys instead of your account's password. Refer to [Katalon API Keys](https://docs.katalon.com/katalon-studio/docs/katalon-apikey-70.html) for further details.

**KATALON_EMAIL**: Enter your Katalon account. Click [here](https://www.katalon.com/create-account/) to sign up if you don't have an account.

**KATALON_API_KEY**: Enter the API Key. 

> If you want to re-activate Katalium Server, you have to remove `framework.properties` file in `.katalon` folder.

### Grid Mode

#### Grid Hub

To start Katalium Server as a Grid Hub, execute `hub.sh` file (in macOS and Linux) or `hub.bat` file (in Windows) with these commands:

```
cd katalium-server
hub.bat
```

```
cd katalium-server
chmod u+x ./hub.sh
./hub.sh
```

See **Standalone mode** for activation steps.

#### Grid Node

Before executing the scripts, please set the Hub URL in `nodeConfigForWindow.json` (for Windows) or `nodeConfig.json` (for macOS and Linux) so that Grid Nodes can register themselves with the above Grid Hub, e.g. `http://hub_ip:4444`.

To start Katalium Server as a Grid Node, execute `node.sh` file (in macOS and Linux) or `node.bat` file (in Windows). 

```
cd katalium-server
node.bat
```

```
cd katalium-server
chmod u+x ./node.sh
./node.sh
```

See **Standalone mode** for activation steps.
