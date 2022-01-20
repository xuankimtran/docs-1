---
title: "Katalon TestCloud Release Notes" 
sidebar: katalon_studio_docs_sidebar
permalink: /katalon-testcloud/docs/release-notes.html
redirect from: 
description:
---

## Trial Period - January 20th, 2022

### New features

* Introduced TestCloud trial period as the new multi-browser testing environment in Katalon Studio, Katalon TestOps, and Katalon Runtime Engine. See: [Integrate TestCloud with TestOps](https://docs.katalon.com/katalon-testcloud/docs/integrate-testcloud-with-testops.html) and [Integrate TestCloud with Studio](https://docs.katalon.com/katalon-studio/docs/testcloud-integration.html).
    * Enabled users to use TestCloud tunnel to execute tests in both public and private domains. See: [TestCloud tunnel](https://docs.katalon.com/katalon-testcloud/docs/testcloud-tunnel.html).
    * Allowed users to contact Katalon at success@katalon.com to buy extra usage quota when running out of free trial package quota.
* Supported new versions of Chrome (96, 97), FireFox (95, 96), Microsoft Edge (96, 97).

### Enhancements from Beta version

* Stabilized TestCloud tunnel performance for testing in private domains:
    * Improved resilience of TestCloud proxy server.
    * Queued up the execution if the number of requests exceeds the parallel quota.
* [UI] Displayed the **Trial** tag for the TestCloud option when scheduling test runs in TestOps.
* [UI] Displayed the **TestCloud** option when clicking on **Run** to execute tests in Katalon Studio.

