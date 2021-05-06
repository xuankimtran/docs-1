---
title: "Desired Capabilities Management"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/import-export-desired-capabilities.html
---

When desired capabilities need to be used across projects, users have to manually re-define them again in a project in use, which is time-consuming and error-prone. 

Consequently, from version 8.0.0, Katalon Studio allows you to import and export desired capabilities in the Katalon Studio project(s). These functions support you to work with **Desired Capabilities** more efficiently and less error-prone.

<table>
	<tbody>
		<tr>
			<td>
				<p><strong>Problem</strong></p>
			</td>
			<td>
				<p><strong>Solution</strong></p>
			</td>
		</tr>
		<tr>
			<td>
				<p>To reuse or copy the configured desired capabilities to multiple places with some minor changes.</p>
			</td>
			<td rowspan="2">
				<ol>
					<li>Choose the driver you want to export its desired capabilities &gt; <a href="https://docs.katalon.com/%20katalon-studio/docs/import-export-desired-capabilities.html/export-desired-capabilities">Export</a> it as JSON file.</li>
					<li>Modify the JSON file if needed.</li>
					<li>Choose the driver you want to import the desired capabilities &gt; <a href="https://docs.katalon.com/%20katalon-studio/docs/import-export-desired-capabilities.html/import-desired-capabilities">Import</a> the JSON file.</li>
				</ol>
			</td>
		</tr>
		<tr>
			<td>To share the configured desired capabilities for team members to reduce the effort spent on modification and recreation of the same settings.</td>
		</tr>
	</tbody>
</table>

### Requirements

- Katalon Studio version 8.0.0.
- An active Katalon Studio Enterprise license.

### Import Desired Capabilities

1. Create new desired capabilities configuration using **JSON file**.

2. Go to **Project/Settings/Desired Capabilities** > choose the driver that you want to import the desired capabilities.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops/desired-capabilities-management/desired-capabilities.png" width=70%>

3. Click **Import**. In the dialog box, **Browse** the imported JSON file > **OK**.

    By default, all current existing desired capabilities will be overridden by imported ones.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops/desired-capabilities-management/chrome_dc.png" width=55%>

### Export Desired Capabilities

1. Go to **Project/Settings/Desired Capabilities** > choose the driver that you want to export its desired capabilities.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops/desired-capabilities-management/desired-capabilities.png" width=70%>

2. Click **Export**. In the dialog box, select the destination folder to save the exported file > **Save**.

    > **Note**
    > 
    > The export configuration will be saved as a **JSON file** to reduce your effort spent on modification and recreation capabilities in case you want to copy the configuration to multiple places with some minor changes.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops/desired-capabilities-management/export-chrome-save.png" width=55%>

See also:

- [Test Artifacts Sharing](https://docs.katalon.com/katalon-studio/docs/import-export-test-artifact.html)
- [Private Plugins](https://docs.katalon.com/katalon-studio/docs/kse-use-plugins.html#private-plugins)
