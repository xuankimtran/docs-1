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

### Plugins usage modes

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
> * Katalon Studio version 7.0.0 onwards.
> * An active Katalon Studio Enterprise license. To learn more about activating licenses, you can refer to this document: [Activate Katalon licenses](https://docs.katalon.com/katalon-studio/docs/activate-license.html#activate-a-license-with-internet-access).

### Build Private Plugins

If you don't know how to build a plugin that can be used in Katalon Studio, please refer to the documents on how to develop [platform plugins](https://docs.katalon.com/katalon-store/docs/publisher/create-plugin.html) and [custom keywords plugins](https://docs.katalon.com/katalon-store/docs/publisher/develop-custom-keywords.html).

If you have already written custom keywords, then code reuse across projects can be achieved easily by distributing the keywords as plugins. This utility is especially helpful when you need to test a set of products that frequently encounter recurring problems. Before, you would have to copy and paste every custom keyword class from projects to projects. Whenever the implementation of the custom keyword changes, you would need to update that change in all projects. Now, you can deploy and install custom keyword plugins through only a few commands and manual steps.

### Store Private Plugins

You need to store private plugins in the `<project_name>//Plugins` folder for Katalon Studio to treat them as local plugins. There are two types of plugins: **Platform** and **Custom Keyword**. Noticeably, **Platform** plugins need storing in the `Plugins//platform` folder.

Below is the structure of the `Plugins` folder:

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

> **Notes**: To install plugins offline, see [Offline Plugin Installation](https://docs.katalon.com/katalon-studio/docs/install-plugin-offline.html)

## Use Plugins in Console Mode

> Requirements:
>
> * Katalon Studio version 7.0.0 onwards
> * An active Katalon Runtime Engine license. To learn more about activating the Katalon Runtime Engine license, you can refer to this document: [Activate Katalon licenses](https://docs.katalon.com/katalon-studio/docs/activate-license.html#activate-a-license-with-internet-access).
> * An API key. To learn more about API keys, you can refer to this document: [Katalon API Key](https://docs.katalon.com/katalon-analytics/docs/ka-api-key.html#create-an-api-key).

To use plugins from Katalon Store in console mode:

- Install the plugin from Katalon Store.
- While generating commands, use the API Key of the users who have the plugin installed. The command-line options of API Key, including -apiKey=<Your_API_Key> and -apikey=<Your_API_Key> are both accepted.

> Notes:
> 
> From versions 7.7.0 onwards, if you belong to more than one Organization subscribing to Runtime Engine licenses, you can choose which Organization validates your license usage with the following command line: -orgID=<Katalon_OrgID>.

If you use the private plugins, make sure you store all plugins in the `<project_name>//Plugins` folder. See [Private Plugins](https://docs.katalon.com/katalon-studio/docs/kse-use-plugins.html#private-plugins), above.