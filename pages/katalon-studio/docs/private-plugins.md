---
title: "Private Plugins"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/private-plugins.html
---

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

To use private plugins, please refer to [the guide](https://docs.katalon.com/katalon-studio/docs/offline-plugin.html) on how to use plugins offline.
