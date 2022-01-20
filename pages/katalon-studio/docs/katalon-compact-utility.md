---
title: "Katalon Compact Utility" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/katalon-compact-utility.html 
redirect_from:
description: 
---

> Requirements:
>
> * Katalon Studio version 8.2.5 onwards.
> * A Chrome Profile. Find more information at Google Help Center: [Share Chrome with others](https://support.google.com/chrome/answer/2364824/share-chrome-with-others-computer).

In restricted environments, unpacked extensions are disabled as a security feature. In that case, using the Spy, Record, and Smart Wait with Chrome might prompt this error: "_Loading the unpacked extension is disabled by the administrators_."

It is possible to use the packed extension **Katalon Compact Utility** as an alternative. The extension is available on Chrome Web Store.

This article will show you how to install the extension, configure your Profile, and use the Spy, Record, and Smart Wait in Katalon Studio.

> Notes:
>
> This utility is associated with your Chrome Profile, which means you can only have one active session at any given time.
>
> Hence, before executing, make sure you log out of all your Chrome sessions.

## Installing Katalon Compact Utility

1. Open Chrome. Make sure you use the Profile you want to use the Spy, Record, or Smart Wait with.

2. Navigate to the Chrome Web Store page for this extension: [Katalon Compact Utility](https://chrome.google.com/webstore/detail/kataton-compact-utility/gkihajmjffefinkmpokfepcdbhnpflee?hl=en&authuser=1).

3. Download and install **Katalon Compact Utility**.

4. Make sure the extension is now active. You can find Google Support instructions to manage your Chrome extensions here: [Install and Manage Extensions](https://support.google.com/chrome_webstore/answer/2664769).

## Configuring and Using the Compact Utility with Chrome Profile

The next steps will help you associate your Chrome Profile with the Spy, Record, and Smart Wait functions in Katalon Studio.

To configure and use Katalon Compact Utility, you need to update the Desired Capabilities. Do as follows:

1. Go to **Project > Settings > Desired Capabilities**.
2. In the **Desired Capabilities** section, select **Web UI > Chrome**.
3. Click **Add** to create a new capability named `args`, for which the type is `List`.
4. To add elements to your list, in the **Value** column of the capability you've created, click on the `...` button.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/katalon-compact-utility/add-desired-capabilities.png" alt="element" width=85%>

5. The **List Properties Builder** dialog appears. Click **Add** to create two elements as below. When you are done, click **OK** to save.

	<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/katalon-compact-utility/list-properties-builder.png" alt="list" width=85%>
    
<table>
	<tbody>
		<tr>
			<td><strong>Type</strong></td>
			<td><strong>Value</strong></td>
		</tr>
		<tr>
			<td rowspan="2">String<br /><br /></td>
			<td>For Windows:&nbsp;<code>user-data-dir=C:/Users/&lt;your_username&gt;/Desktop/User Data</code></td>
		</tr>
		<tr>
			<td>For Mac OS:&nbsp;<code>user-data-dir=/Users/&lt;your_username&gt;/Library/Application Support/Google/Chrome</code></td>
		</tr>
		<tr>
			<td>String</td>
			<td><code>profile-directory=&lt;your_profile_name&gt;</code></td>
		</tr>
	</tbody>
</table>

> **Finding your Chrome Profile in the User Data Directory**
>
> There are multiple Profiles in a given User Data Directory. To find the name of a Chrome Profile, do as follows:
>
> * Open Chrome with the Profile you previously used to install Katalon Compact Utility. In the address bar, type `chrome://version` and press Enter.
> * The line **Profile Path** displays the path to your active Profile. For example: `C:\Users\your_username\AppData\Local\Google\Chrome\User Data\your_profile_name`.

6. To save the Chrome configuration, click **Apply and Close**. 

	You can now use the Spy, Record, and Smart Wait features with the default Chrome option.

### Disable XPath visibility

From Katalon Studio version 8.2.5 onwards, you can enable/disable the XPath visibility while recording actions on your app under test. Do as follows:

1. Open Chrome, then click on the *Extension* icon.
2. Click on the *More* icon of the **Katalon Compact Utility**, then choose **Options**.
3. Click on the **XPath Visibility** toggle to enable/disable XPath visibility.

	<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/katalon-compact-utility/xpath-visibility.png" alt="xpath visibility" width=60%>

> Known limitation:
>
> * For web pages saved as HTML local files, Katalon Compact Utility cannot spy and capture objects, while unpacked extensions (from the native Spy and Record utility) can do that.

See also:

* [Spy Web Utility](https://docs.katalon.com/katalon-studio/docs/spy-web-utility.html)
* [Creating test cases using Record & Playback](https://docs.katalon.com/katalon-studio/docs/create_test_case_using_record_playback.html)
* [[WebUI] Smart Wait Function](https://docs.katalon.com/katalon-studio/docs/webui-smartwait.html)
