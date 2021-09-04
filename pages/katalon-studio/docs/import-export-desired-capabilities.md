---
title: "Reusing Desired Capabilities across projects"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/import-export-desired-capabilities.html
---

From version 8.0.0 onwards, you can use desired capabilities across Katalon Studio project(s) by importing and exporting desired capabilities in a JSON file. With this new feature, you don't have to manually re-define them again in another project, making your work more efficient and less error-prone. See also [Desired Capabilities](https://docs.katalon.com/katalon-studio/docs/introduction-to-desired-capabilities.html).

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
				<p>Reuse or copy the configured desired capabilities to multiple places with some minor changes.</p>
			</td>
			<td rowspan="2">
				<p>Do as follows:</p>
					<ol>
						<li>Choose the driver with the desired capabilities you want to export &gt; <a href="https://docs.katalon.com/katalon-studio/docs/import-export-desired-capabilities.html#export-desired-capabilities">Export</a> it as a JSON file.</li>
						<li>Modify the JSON file if needed.</li>
						<li>Choose the driver you want to import the desired capabilities &gt; <a href="https://docs.katalon.com/katalon-studio/docs/import-export-desired-capabilities.html#import-desired-capabilities">Import</a> the modified JSON file.</li>
					</ol>
			</td>
		</tr>
		<tr>
			<td>Share the configured desired capabilities for team members to reduce the effort spent on modification and recreation of the same settings.</td>
		</tr>
	</tbody>
</table>

### Requirements

- Katalon Studio version 8.0.0.
- An active Katalon Studio Enterprise license.

### Import Desired Capabilities

1. Create new desired capabilities configuration using **JSON file**.

2. Go to **Project/Settings/Desired Capabilities** > choose the driver you want to import the desired capabilities.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops/desired-capabilities-management/desired-capabilities.png" width=70%>

3. Click **Import**. In the dialog box, **Browse** the imported JSON file > **OK**.

> **Notice**
> 
> After importing new desired capabilities from the JSON file, it overwrites all existing ones.
>
>

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops/desired-capabilities-management/chrome_dc.png" width=55%>

### Export Desired Capabilities

1. Go to **Project/Settings/Desired Capabilities** > Choose the driver with the desired capabilities you wish to export.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops/desired-capabilities-management/desired-capabilities.png" width=70%>

2. Click **Export**. In the dialog box, select the destination folder to save the exported JSON file > **Save**.

    > **Note**
    > 
    > The export configuration as a **JSON file** reduces your effort on modification and recreation capabilities in case you want to copy the configuration to multiple places with minor changes.
	>

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops/desired-capabilities-management/export-chrome-save.png" width=55%>

See also:

- [Test Artifacts Sharing](https://docs.katalon.com/katalon-studio/docs/import-export-test-artifact.html)
- [Private Plugins](https://docs.katalon.com/katalon-studio/docs/kse-use-plugins.html#private-plugins)
