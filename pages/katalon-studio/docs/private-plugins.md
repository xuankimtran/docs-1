---
title: "Private Plugins Introduction"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/private-plugins.html
---

> Starting from **Katalon Studio version 7.0.0**, **Katalon Studio Enterprise** allows you to use self-developed plugins, without having to upload to Katalon Store.

You can create private plugins for your organziations or customers and distribute them directly without uploading to Katalon Store. Therefore, you can freely improve your testing capabilities while maintaining the plugins safe in your own prem.


### Private plugins

**Katalon Studio's private plugins** are only used by those authenticated organizational users and not published on Katalon Store for public use.

If you have already written [custom keywords](https://docs.katalon.com/katalon-store/docs/publisher/develop-custom-keywords.html), then code reuse can be achieved easily through distributing the keywords as plugins to new test automation projects. This is especially meaningful when you need to test a set of products that frequently encounters recurring problems. Before, you would have to copy and paste every custom keyword class from projects to projects. Whenever the implementation of the plugin change, you would need to copy and paste the new implementations to all projects. Now, plugin deployment and plugin installation can be done through only a few commands and a few manual steps.


### Plugins Folder

Private plugins are stored in a Katalon project, under the Plugins folder. They are treated as local plugins. 

Plugins folder structure:

```

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

> Notes: All [platform plugins](https://github.com/katalon-studio/katalon-studio-platform) should be placed at the Plugins/platform folder while all [Custom Keyword plugins](https://docs.katalon.com/katalon-store/docs/publisher/develop-custom-keywords.html) should be placed at the bottom of the Plugins folder.

### Plugin Repository

You're allowed to choose a Plugin Repository by following this path: **Preferences** > **Katalon** > **Plugins**.

There are three options for you:

* **Katalon Store and Local**: Katalon Studio will install plugins from Katalon Store and the Plugins folder of each project.
* **Katalon Store**: Katalon Studio will install plugins from Katalon Store only.
* **Local**: Katalon Studio will install plugins from the Plugins folder only.
