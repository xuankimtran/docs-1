---
title: "Reusing Desired Capabilities across projects"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/import-export-desired-capabilities.html
---

### Requirements

- Katalon Studio version 8.0.0.
- An active Katalon Studio Enterprise license.

From version 8.0.0 onwards, you can reuse desired capabilities across Katalon Studio project(s) by importing and exporting desired capabilities in a JSON file. See also [Desired Capabilities](https://docs.katalon.com/katalon-studio/docs/introduction-to-desired-capabilities.html).

This is useful if you want to:
- Reuse or copy the configured desired capabilities to another projects with some minor changes.
- Share the configured desired capabilities for team members to reduce effort.

Follow these steps:
### Export Desired Capabilities

1. Go to **Project/Settings/Desired Capabilities** > Choose the driver with the desired capabilities you wish to export. Click **Export**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops/desired-capabilities-management/desired-capabilities.png" width=70%>

2. The dialog box appears. Select the destination folder, then click **Save**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops/desired-capabilities-management/export-chrome-save.png" width=55%>

### Import Desired Capabilities

After exporting the JSON files, you can modify them if needed, then import them into another projects. 

Follow these steps:

1. Go to **Project/Settings/Desired Capabilities** > choose the driver you want to import the desired capabilities of. Click **Import**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops/desired-capabilities-management/desired-capabilities.png" width=70%>

2. A dialog box appears. Click **Browse**. Navigate to the JSON file you want to import and select it. Click **OK**.

	> **Note**
	> 
	> You can decide whether to override all existing desired capabilities by checking/unchecking the **Override existing properties** box.

	<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops/desired-capabilities-management/chrome_dc.png" width=55%>


See also:

- [Test Artifacts Sharing](https://docs.katalon.com/katalon-studio/docs/import-export-test-artifact.html)
- [Private Plugins](https://docs.katalon.com/katalon-studio/docs/kse-use-plugins.html#private-plugins)
