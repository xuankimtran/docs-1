---
title: "Working with Sensitive Text" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/working-with-sensitive-text.html 
redirect_from:
    - "/display/KD/Working+with+Sensitive+Text/"
    - "/display/KD/Working%20with%20Sensitive%20Text/"
    - "/x/3wHR/"
    - "/katalon-studio/docs/working-with-sensitive-text/"
description: 
---
Katalon Studio supports text encryption directly inside the test script. This feature is helpful in case the project team needs to share tests containing sensitive information with other team members or key stakeholders. There are two ways to leverage this feature in **Manual Mode** and **Script Mode**:

## Manual Mode

1. Open your desired Test Case in manual mode.
2. Click **Add** and select the `Set Encrypted Text` built-in keywords. To learn more about this keyword, see [[WebUI] Set Encrypted Text](https://docs.katalon.com/katalon-studio/docs/webui-set-encrypted-text.html).
3. In the `Set Encrypted Text` test step, double-click on the **Input** field. The **Input** dialog appears to help you encrypt any raw text.
4. Double-click on the **Value** field. Enter the **Raw Text**. The **Encrypted Text** is generated accordingly.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/working-with-sensitive-text/encrypted-text-manual.png" alt="encrypted text in manual mode" width="100%">

5. When you are done, click **Insert**. The **Encrypted Text** then closes. In the **Input** dialog, you can now see the **Value** is added. Click **OK**.

## Script Mode

> Raw text must be encrypted before using in Script Mode.

1. Open your desired Katalon project.
2. In the main menu, go to **Help > Encrypted Text**. The **Encrypted Text** dialog appears.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/working-with-sensitive-text/encrypted-text-script-mode.png" alt="encrypted text in script mode" width="60%">

3. Enter the **Raw Text**. The **Encrypted Text** is generated accordingly.
4. When you are done, click **Copy and Close**.
5. Open your test case in script mode, paste the encrypted text as a param of the `setEncryptedText` built-in keywords. To learn more about this keyword, see [[WebUI] Set Encrypted Text](https://docs.katalon.com/katalon-studio/docs/webui-set-encrypted-text.html).

For example:

``` groovy
'Input password'
WebUI.setEncryptedText(findTestObject('Page_Login/txt_Password'), 'g3/DOGG74jC3Flrr3yH+3D/yKbOqqUNM')
```
