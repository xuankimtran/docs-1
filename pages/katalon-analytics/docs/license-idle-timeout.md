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

You can define how long an open Katalon Studio app with a KSE license can stay inactive before the licensed user is considered idle. Licensed users considered idle will be automatically signed out. This setting impacts all the licensed users in the organization.

**In Katalon TestOps**:

To enable idle timeout, do as follows:

1. Log into [Katalon TestOps](https://testops.katalon.io/).
2. Select your **Organization** > select **Timeout**. The **Idle Timeout Settings** screen appears.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/idle-timeout/idle-timeout.png" width=100% alt="manage idle timeout">
   
3. Idle Timeout is disabled by default. Toggle it on to enable the setting.
4. Specify the desired timeout (in minutes). By default, Katalon sets 120 minutes as the timeout period.

5. From version 8.2.0 onwards, you can set the bypass threshold to limit the number of times that licensed users can resume the session after receiving the idle timeout notification.

   In the **Idle Timeout Bypass Limit** section, input the desired bypass limit. Leaving this section empty enables licensed users to resume the session unlimited times.

6. Click **Update** to save your setting.

**In Katalon Studio**:

When this setting is applied, Katalon Studio will notify the user 15 minutes before the end of the timeout period or when only a quarter of the time remains, whichever is shorter.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/license-mgt/noti.png" width=60%>

* To resume the session, the user can click **Continue**. The notification dialog displays how many times you have left to resume the session.
* To log out immediately, the user can click **Deactivate**.
* If the user does nothing or clicks on the _X_ button to close this notification dialog, the user will be logged out automatically at the end of the timeout period.
