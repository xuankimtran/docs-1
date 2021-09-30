---
title: "Katalon Compact Utility" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/katalon-compact-utility.html 
redirect_from:
description: 
---
> Requirements:
>
> * Katalon Studio version 8.0.0 onwards.
> * A Chrome Profile. Find more information here: [Share Chrome with others](https://support.google.com/chrome/answer/2364824/share-chrome-with-others-computer).

In restricted environments, unpacked extensions are disabled as a security feature. In that case, using the Spy, Record, and Smart Wait with Chrome might prompt this error: "_Loading the unpacked extension is disabled by the administrators_."

It is possible to use the packed extension **Katalon Compact Utility** as an alternative. The extension is available on Chrome Web Store.

This article will show you how to install the extension, configure your Profile, and use the Spy, Record, and Smart Wait in Katalon Studio.

> Notes:
>
> This utility is associated with your Chrome Profile, which means you can only have one active session at any given time.

## Installing Katalon Compact Utility

1. Open Chrome. Make sure you use the Profile you want to use the Spy, Record, or Smart Wait with.

2. Navigate to the Chrome Web Store page for this extension: [Katalon Compact Utility](https://chrome.google.com/webstore/detail/kataton-compact-utility/gkihajmjffefinkmpokfepcdbhnpflee?hl=en&authuser=1).

3. Download and install **Katalon Compact Utility**.

4. Make sure the extension is now active. You can find Google Support instructions to manage your Chrome extensions here: [Install and Manage Extensions](https://support.google.com/chrome_webstore/answer/2664769).

## Configuring and Using the Compact Utility with Chrome Profile

The next steps will help you associate your Chrome Profile with the Compact Chrome (with Profile) function in Katalon Studio.

### Finding your Chrome Profile in the User Data Directory

There are multiple Profiles in a given User Data Directory. This section will help you find the path to the correct one.

1. Open Chrome with the Profile you previously used to install Katalon Compact Utility. In the address bar, type `chrome://version` and press Enter.

2. The line "Profile Path:" now displays the path to your *active* Profile. For example: `C:\Users\your_username\AppData\Local\Google\Chrome\User Data\your_profile_name`.
3. Copy your profile name.
4. Close Chrome.

### Configuring and using Katalon Compact Utility with Chrome Profile

To configure and use Katalon Compact Utility, you need to update the Desired Capabilities. Do as follow:
1. Go to **Project > Settings > Desired Capabilities**.
2. In the **Desired Capabilities** section, select **WebUI > Chrome**.
3. Click **Add** to create a new capability named `args`, which type is `List`.
4. To add elements to your list, in the **Value** column of the capability you've created, click on the `...` button.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/katalon-compact-utility/capability.png" alt="element" width=80%>

5. The **List Properties Builder** dialog appears. Click **Add** to create two elements as below:
    
    <table width="70%">
	<tbody>
	<tr>
	<td><strong>Type</strong></td>
	<td><strong>Value</strong></td>
    </tr>
	<tr>
	<td rowspan="2">Element 1</td>
	<td rowspan="2">String</td>
	<td>
	<div>
	<div>For Windows: <code>user-data-dir=C:/Users/&lt;your_username&gt;/Desktop/User Data</code></div>
	</div>
	</td>
    </tr>
	<tr>
	<td>
	<div>
	<div>For Mac OS: <code>user-data-dir=/Users/&lt;username&gt;/Library/Application Support/Google/Chrome</code></div>
	</div>
	</td>
	</tr>
	<tr>
	<td>Element 2</td>
	<td>String</td>
	<td>
	<div>
	<div><code>profile-directory=&lt;your_profile_name&gt;</code></div>
	</div>
	</td>
	</tr>
	</tbody>
    </table>

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/katalon-compact-utility/list-properties-builder.png" alt="list" width=70%>

6. Execute feature by default Chrome option.

See also:
* [Spy Web Utility](https://docs.katalon.com/katalon-studio/docs/spy-web-utility.html)
* [Record with Chrome using Packed Extension](https://docs.katalon.com/katalon-studio/docs/record-web-utility-using-chrome-with-profile.html)
* [[WebUI] Smart Wait Function](https://docs.katalon.com/katalon-studio/docs/webui-smartwait.html)
