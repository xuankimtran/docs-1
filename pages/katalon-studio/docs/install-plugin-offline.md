---
title: "Install Plugin Offline"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/install-plugin-offline.html
redirect_from:
description:
---
To leverage your testing experience, Katalon Store provides you a library of useful plugins developed by Katalon team and the community users. You can intall plugins online by navigating to Katalon Store. However, there are cases when you might want to:

* Install and use all the plugins that are available on Store without the Internet required.
* Build your plugins and use them directly in Katalon Studio without publishing on Store.

In this document, you can find step-by-step guide on how to install plugin offline in Katalon Studio.

## Install Plugin Offline

> **Requirements**:
>
> * Katalon Studio version 7.0.0 onwards.
> * An [active license for Katalon Studio Enterprise](https://docs.katalon.com/katalon-studio/docs/license.html#paid-license).

To use any plugins published on Store without accessing the Internet, follow these steps:

1. In [Katalon Store](https://store.katalon.com/), select the plugin you want to install. In the **Information** section, check the type of that plugin. There are two types of plugin: **Custom Keywords Plugin** and **Katalon Studio Plugin**.

2. Download the plugin package. To learn how to download a plugin package, see [Download plugin packages](https://docs.katalon.com/katalon-store/docs/user/getting-started.html#download-plugin-packages).

3. Unzip your downloaded plugin package.

4. Move the plugin package **jar.** file to the following folder:

- For Custom Keywords Plugin: **<project_name>/plugins**
- For Katalon Studio Plugin: **<project_name>/plugins/platform**

5. Open your project in Katalon Studio, and go to **Project > Settings > Plugins**, select one of the following options to use plugins offline:

* **Katalon Store and Local**: Katalon Studio installs plugins from Store and the Plugins folder of each project. Make sure that you log in Katalon Studio and Katalon Store with the same account
* **Local**: Katalon Studio will install plugins from the Plugins folder only.

6. In the **Toolbar > Your Profile**, click **Reload Plugins**.