---
title: "Private Plugins"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/private-plugins.html
---

> Starting from **Katalon Studio version 6.3.4**, Katalon Studio's private plugins are available for users in a team and an organization.

View and copy your an organization ID at [https://analytics.katalon.com](https://analytics.katalon.com/), and then send it to us for enabling this feature.

This new feature allows users to **add** a private plugin to the Plugins Folder, then **download** and **use** it like those plugins downloaded from Katalon Store.

### **Private plugins**

**Katalon Studio's private plugins** are [Katalon Studio plugins](https://docs.katalon.com/katalon-store/docs/publisher/create-plugin.html) that are only used by those authenticated organizational users and not published on Katalon Store for public use.

You're allowed to use private plugins only when being authenticated by Katalon Store. Unlike normal users, those users granted to use private plugins can use an unlimited number of plugins.

### **Plugins Folder**

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

### **2. Plugin Repository**

You're allowed to choose a Plugin Repository by following this path: **Preferences**> **Katalon**> **Plugins**.

There are three options for you:

* **Katalon Store and Local**: Katalon Studio will download plugins from Katalon Store and the Plugins folder of each project.
* **Katalon Store**: Katalon Studio will download plugins from Katalon Store only.
* **Local**: Katalon Studio will download plugins from the Plugins folder only.
