---
title: "Configure Idle Timeout"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/license-idle-timeout.html
description:
---

> Requirement:
>
> * An active Katalon Studio Enterprise (KSE) license.
> * Katalon Studio version 7.8.0 onwards.
> * You must be an Admin or Owner of your Organisation.

## Configure Idle Timeout

With this function, you can optimize the usage of KSE licenses by setting a time restriction for users to have no interactions with Katalon Studio. This setting impacts all KSE users in this organization, which means KSE users will automatically sign out when they take no actions in the app.

**On Katalon Admin**:

To enable timeout setting for license usage, please do as follows:

1. Log into [Katalon TestOps](https://admin.katalon.com/).
2. Select your **Organization** > select **Timeout**
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/license-mgt/manage-idle-timeout.png" width=60% alt="manage idle timeout">
3. In the displayed **Idle Timeout Settings** screen, Katalon turns off the idle timeout by default, click on the switch button to enable the setting.
4. Specify the desired timeout (in minutes). By default, Katalon sets 120 minutes as the timeout period.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/license-mgt/manage-enabling-timeout.png" alt="set timeout" width=60%>

5. Click **Update** to save your setting.

**In Katalon Studio**:

When this setting is applied, if the users in that organization have been idle for the specified minutes, they will log out automatically. Katalon Studio will send a notification to the user before the automatic sign-out.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/license-mgt/noti.png" width=60%>