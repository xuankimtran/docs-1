---
title: "Install Plugin Offline"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/install-plugin-offline.html
redirect_from:
description:
---
To leverage your testing experience, Katalon Store provides you a library of plugins developed by Katalon and the Katalon community. The plugins are available on the [Katalon Store](https://store.katalon.com/). However, in some cases, you might want to:

* Install and use all the plugins that are available on the Store without internet access.
* Build your plugins and use them directly in Katalon Studio without publishing on Store. See also: [Private Plugins](https://docs.katalon.com/katalon-studio/docs/kse-use-plugins.html#private-plugins).

Below is a step-by-step guide to install plugins offline in Katalon Studio.

## Install Plugin Offline

> **Requirements**:
>
> * Katalon Studio version 7.0.0 onwards.
> * An [active license for Katalon Studio Enterprise](https://docs.katalon.com/katalon-studio/docs/license.html#paid-license).

To use any plugins published on Store without accessing the Internet, follow these steps:

1. In [Katalon Store](https://store.katalon.com/), select the plugin you want to install. In the **Information** section, check the type of that plugin. There are two types of plugins: **Custom Keywords Plugin** and **Katalon Studio Plugin**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/install-offline-plugin/KS-install-plugin-offline-plugin-type.png" alt="Plugin Type" width=100%>

2. Download the plugin package. To learn how to download a plugin package, see [Download plugin packages](https://docs.katalon.com/katalon-store/docs/user/getting-started.html#download-plugin-packages).

3. Unzip your downloaded plugin package.

4. Move the plugin package **.jar** file to the following folder:

    * For Custom Keywords Plugin: **<project_name>/plugins**
    * For Katalon Studio Plugin: **<project_name>/plugins/platform**

        <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/install-offline-plugin/KS-install-plugin-offline-platform.png" alt="Platform Plugin" width=70%>

5. Open your project in Katalon Studio and go to **Project > Settings > Plugins**. Select one of the following options to use plugins offline:

* **Katalon Store and Local**: Katalon Studio installs plugins from the Store and the **Plugins** folder of each project. Make sure that you log in Katalon Studio and Katalon Store with the same account.
* **Local**: Katalon Studio will install plugins from the **Plugins** folder only.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/install-offline-plugin/KS-install-plugin-offline-project%20settings.png" alt="project settings" width=60%>

6. In the **Toolbar**, click **Your Profile > Reload Plugins**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/install-offline-plugin/KS-offline-plugin-reload.png" width=40%>

    The **Plugins** dialog appears with the reload status.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/install-offline-plugin/KS-install-plugin-offline-reload-success.png" alt="reload success" width=60%>
