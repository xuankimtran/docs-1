---
title: "FAQ & Troubleshooting Instructions"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-recorder/docs/faq-and-troubleshooting-instructions.html
redirect_from:
    - "/x/7gHR/"
    - "/katalon-recorder/docs/faq-and-troubleshooting-instructions/"
description:
---

## Common failures and resolutions
Try the following suggestions when your automation scripts fail. If they don't work either, open a thread on [our forum](https://forum.katalon.com/c/katalon-recorder/17) to ask experts for help.

### Your automation script passes but the actual action was not performed

Add the following step:
- Command: waitForElementPresent
- Target: Same target as the failing step.
- Value: none.

before the failing step.

If that doesn't work, then add the following step:
- Command: pause.
- Target: none.
- Value: 10000 (miliseconds).

before the failing step.

### Your automation script fails because of element not found
Locators are methods that KR use to find elements on websites. If your automation script fails because of an element not found, click on the target dropdown of the failed step and choose another locator.

## FAQ

### Upload files

Currently, only the Chrome version of Katalon Recorder supports file uploading.

Right click on the extension icon on the top right toolbar, select **Manage extensions**. In the **Manage extensions** page, enable "Allow access to file URLs".

![](https://raw.githubusercontent.com/katalon-studio/docs-images/master/katalon-recorder/docs/katalon-recorder-allow-access-to-file-urls.png)

The action was completed using "type" command. Example:

```
type | id=file-upload | C:\file.txt (or /home/me/file.txt for Linux)
```

> **Note**
>
> Do not `click` on the input element.

We are still actively looking for a solution for Firefox. If you have any question or suggestion, please join the discussion [here](https://forum.katalon.com/discussion/4833/katalon-automation-recorder-how-to-do-a-file-upload-htmlinputelement).

### Drag and drop

If the drag-and-drop feature on your website was built with HTML5, please use the command "dragAndDropToObject". If it was built with jQuery UI, please use the command "dragAndDropToObjectByJqueryUI".

### Set text values for text-based input elements

Due to the differences between web pages, there are three commands you can use to set text values for text-based input elements (e.g. type="text" or "number"). If you encounter troubles setting text values, please try those commands in this order:

1.  type
2.  sendKeys
3.  setText

**For input elements with type=**"**number", you have to use "setText" to set negative values.**

### Content Security Policy errors

We are looking for a solution right now. Technically, it's possible to overwrite CSP rules with add-ons, but it would be insecure to do that on every web page.

For now, to work around the issue on Chrome, users can use a third-party add-on (e.g. Disable Content-Security-Policy [https://chrome.google.com/webstore/detail/disable-content-security/ieelmcmcagommplceebfedjlakkhpden?hl=en](https://chrome.google.com/webstore/detail/disable-content-security/ieelmcmcagommplceebfedjlakkhpden?hl=en)) to disable CSP rules, then execute the test in KR as usual. **Don't forget to disable that add-on when unused.**

On Firefox, please disable the "security.csp.enable" option in "about:config" to achieve the same effect. **Don't forget to enable it when unused.**
