---
title: "Using Plugins with Katalon Studio Enterprise License"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/kse-use-plugins.html
redirect_from:
    - "/katalon-studio/docs/offline-plugin.html"
    - "/katalon-studio/docs/private-plugins.html"
    - "/katalon-store/docs/user/plugin-console-installation/"
    - "/katalon-store/docs/user/plugin-console-installation.html"
description:
---
Katalon Plugin is to extend Katalon Studio's capabilities and integrate the software with your favorite tools. This section introduces plugins, different ways of using plugins with Katalon Studio Enterprise license and the detailed configuration of each way.

## Introduction to Plugins

### Plugins on Katalon Store

You can find many plugins published on [Katalon Store](https://store.katalon.com/), which are developed by the Katalon team or the community user.

Some plugins are exclusive for Katalon Studio Enterprise users only while the other plugins are available for the community, free of charge.

You can trial an Enterprise plugin for 30 days. After the trial period, if you wish to continue using the plugin for configuration, you need to subscribe to a Katalon Studio Enterprise license.

### Plugins' usage modes

All Katalon users are eligible for using the community plugins published on Store.

Compared to the community users, in addition to Store's plugins, Katalon Studio Enterprise users can use their private plugins or all plugins in an offline environment.

Katalon Runtime Engine users can use plugins in console mode.

### Plugin Repository

Katalon Studio Enterprise users can decide where Katalon Studio will download plugins for a project. Go to **Project > Settings > Plugins** and select one of the following options:

* **Katalon Store and Local**: Katalon Studio will install plugins from Store and the Plugins folder of each project.
* **Katalon Store**: Katalon Studio will install plugins from Katalon Store only.
* **Local**: Katalon Studio will install plugins from the Plugins folder only.

## Private Plugins

Private plugins are Katalon plugins that are developed for private use. With private plugins supported, you can build, distribute, install, and use your own plugins without publishing them on Store for public access.

> **Requirements**:
>
> * Your Katalon Studio version must be 7.0 or later.
> * You need an [active license for Katalon Studio Enterprise](https://docs.katalon.com/katalon-studio/docs/license.html#paid-license).

### Build Private Plugins

If you don't know how to build a plugin that can be used in Katalon Studio, please refer to the documents on how to develop [platform plugins](https://docs.katalon.com/katalon-store/docs/publisher/create-plugin.html) and [custom keywords plugins](https://docs.katalon.com/katalon-store/docs/publisher/develop-custom-keywords.html).

If you have already written custom keywords, then code reuse across projects can be achieved easily by distributing the keywords as plugins. This utility is especially helpful when you need to test a set of products that frequently encounter recurring problems. Before, you would have to copy and paste every custom keyword class from projects to projects. Whenever the implementation of the custom keyword changes, you would need to update that change in all projects. Now, you can deploy and install custom keyword plugins through only a few commands and manual steps.

### Store Private Plugins

You need to store private plugins in **<project_name>//Plugins** for Katalon Studio to treat them as local plugins. There are two types of plugins: *Platform* and *Custom Keyword*. Noticeably, *Platform* plugins need storing in the **Plugins//platform** folder.

The **Plugins** folder's structure:

```groovy

Plugins

 |

 |___ platform

         |___ IDE plugin 1.jar

         |___ IDE plugin 2.jar

         |___ ....

         |___ IDE plugin n.jar

 |___ Custom keyword plugin 1.jar

 |___ Custom keyword plugin 2.jar

 |___ ...

 |___ Custom keyword plugin n.jar
```

### Use Private Plugins

In **Project > Settings > Plugins**, select one of the following options:

* **Katalon Store and Local**: Katalon Studio will install plugins from Store and the Plugins folder of each project.
* **Local**: Katalon Studio will install plugins from the Plugins folder only.

## Use Plugins Offline

Together with offline features of Katalon Studio Enterprise, using plugins without Internet access is an excellent complimentary feature for you to:

* Install and use all the plugins that are available on Store without the Internet required.
* Build your plugins and use them directly in Katalon Studio without publishing on Store.

> **Requirements**:
>
> * Your Katalon Studio version must be 7.0 or later.
> * You need an [active license for Katalon Studio Enterprise](https://docs.katalon.com/katalon-studio/docs/license.html#paid-license).

To use any plugins published on Store without accessing the Internet, follow these steps:

1. Get a plugin package from Katalon Store. [Learn more](https://docs.katalon.com/katalon-store/docs/user/getting-started.html#download-plugin-packages).
2. Unzip your downloaded plugin package
3. Move the plugin package to **<project_name>/plugins**

   > Please be noted that *Platform* plugins need storing in the **<project_name>/plugins/platform** folder.

4. Open your project in Katalon Studio, and go to **Project > Settings > Plugins**, select one of the following options to use plugins offline:

* **Katalon Store and Local**: Katalon Studio will install plugins from Store and the Plugins folder of each project.
* **Local**: Katalon Studio will install plugins from the Plugins folder only.

5. Click **Reload Plugins**

## Use Plugins in Console Mode

> **Requirements**:
>
> * Your Katalon Studio version must be 7.0 or later
> * An active [Katalon Runtime Engine](https://docs.katalon.com/katalon-studio/docs/intro-RE.html) license
> * A [Katalon API Key](https://docs.katalon.com/katalon-analytics/docs/ka-api-key.html#create-an-api-key)

Your command needs API Key parameter for authentication when you want to use plugins installed on Katalon Store.

If you specify using the local plugin repository, make sure you store all plugins in **<project_name>//Plugins** folder.
