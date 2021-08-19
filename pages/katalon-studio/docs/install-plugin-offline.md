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

1. Download a plugin package from Katalon Store. [Learn more](https://docs.katalon.com/katalon-store/docs/user/getting-started.html#download-plugin-packages).
2. Unzip your downloaded plugin package
3. Move the plugin package to **<project_name>/plugins**

   > Please be noted that *Platform* plugins need storing in the **<project_name>/plugins/platform** folder.

4. Open your project in Katalon Studio, and go to **Project > Settings > Plugins**, select one of the following options to use plugins offline:

* **Katalon Store and Local**: Katalon Studio will install plugins from Store and the Plugins folder of each project.
* **Local**: Katalon Studio will install plugins from the Plugins folder only.

5. Click **Reload Plugins**