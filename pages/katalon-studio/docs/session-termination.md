---
title: "Session Termination Causes"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/session-termination.html
description:
---

You may encounter some situations when your session has been terminated due to a specific reason related to the license mechanism of Katalon Studio (KS), Katalon Studio Enterprise (KSE), Katalon Runtime Engine (KRE), and Katalon Floating Runtime Engine (KFRE). This section explains some common causes of your session termination.

**Standard license quota exceeded.**

Each Katalon account registered with a public email can have a standard license to use KS. The license quota is 1, which means the account is active on only one machine (one active session only) at a time.

This cause can also appear when a Katalon account registered with a business email after the trial period falls back to a standard license.

**Trial license quota exceeded.**

Each trial account has only one license to be active. If trial users try to use more than one session at a time, the later session will terminate the previous one as a result.

**Machine quota exceeded.**

Apart from license quota, the number of active licenses of KSE, KRE, and KFRE are also limited by machine quota. The number of registered machines cannot exceed the license quota.

**License quota exceeded.**

The number of active licenses of KSE, KRE, and KFRE cannot exceed the license quota.

**Trial license is only available for Katalon accounts registered with business emails.**

Katalon accounts registered with a public email cannot trial KRE. Only Katalon accounts registered with business emails are eligible for trial licenses of KRE/KSE. Standard license is not supported for KRE.

**inactive session; the license has been transferred to <another_user>.**

When your session is inactive, another granted user from your Organization can occupy your license.

**Your account is logged into another machine.**

One Katalon account can be active on one machine at a time.

**A trial license is already associated with this account.**

A trial license grants you only one working session. When you try to use more than one KRE session, this error may occur to you.

**This machine has been removed from the registered list.**

This happens when your Organization Admins or Owner remove your machine from the registered list on Katalon TestOps. This removal will end your session on the Katalon Studio app.
