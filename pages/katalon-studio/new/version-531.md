---
title: "Version 5.3.x"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/new/version-531.html
redirect_from:
    - "/display/KD/Version+5.3.1/"
    - "/display/KD/Version%205.3.1/"
    - "/x/JAHR/"
    - "/katalon-studio/new/version-531/"
    - "/katalon-studio/new/version-530.html"
    - "/display/KD/Version+5.3.0/"
    - "/display/KD/Version%205.3.0/"
    - "/x/CoC9/"
    - "/katalon-studio/new/version-530/"
description:
---

## Version 5.3.1

### Integration and Email Accounts Encryption

Provide user an option in Project Settings to encrypt all integration and email accounts with Katalon Studio. This helps to ensure the security of accounts information in sharing such as via Git. 

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-531/image2018-3-1-113A523A11.png)

### Masking Password Field in Record Web

Since version 5.3.1, Katalon Studio will auto-detect and masked the input text of Password field while Recording.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-531/image2018-3-1-123A273A59.png)

### Support Private Kobiton Devices

Enhance Kobiton integration to support mobile testing with **Private** Kobiton devices. 

### Support Proxy in Console Mode Execution

Allow users to pass Proxy settings in Console Mode command

| Option Name | Value Type | Value | Mandatory? |
| --- | --- | --- | --- |
| proxy.option | Fixed | NO\_PROXY, USE\_SYSTEM, MANUAL_CONFIG | YES |
| proxy.server.type | Fixed |  HTTP, HTTPS, or SOCKS | YES |
| proxy.server.address | String | Example: http://192.168.12.32, [http://katalon.com](http://katalon.com/) | YES |
| proxy.server.port | Integer | Example: 80, 8080, 9999 | YES |
| proxy.username | String | Example: MyProxyUsername | Optional (YES if your proxy server requires authentication) |
| proxy.password | String | Example: MyProxyPassword | Optional (YES if your proxy server requires authentication) |

**Example:**

```groovy
katalon -noSplash  -runMode=console -consoleLog -noExit -projectPath="C:\Users\Katalon Studio\Project\YourProject.prj" -retry=0 -testSuitePath="Test Suites/TS_RegressionTest" -browserType="Chrome (headless)" --config -proxy.option=MANUAL_CONFIG -proxy.server.type=HTTP -proxy.server.address="http://192.168.12.32" -proxy.server.port="8888"
```

### Issues fixed

Support negative verification on API error response code (4xx, 5xx, etc)

## Version 5.3.0

### General

*   In version 5.3, Katalon team enhanced generated **XPath** for Test Objects. With the new robust XPath, test objects can be better located in the AUT. Thus, test quality is improved significantly. 
*   **Auto-saved** last **execution environment** is implemented in Version 5.3 to help save the last selected execution environment as default. Katalon Studio will replace the current default execution environment with the selected one (if it's different).
*   For Katalon to be Docker-ready
    *   Add extra argument for Chrome in **Console Mode** execution
        *   **--no-sandbox**
    *   Remove splash screen in CLI mode

    *   Separate command for generate/update classpath
    *   Fix bugs when using CLI mode with properties file

### Test Suite

Implement [**Setup** / **Teardown**](/x/E4C9) for Test Suite. This feature is another great extension besides [Test Listener](/katalon-studio/docs/test-listeners-test-hooks.html) to extend your current testing flow as much as possible.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-530/image2018-1-8-163A253A42.png)

### Execution

Introduce all new [**Headless** execution mode for **Firefox**](/katalon-studio/tutorials/headless-browsers-execution/)  supports user in Continuous Delivery process, UI regression and quick environment coverage. Tests execution will be much faster and more effective.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-530/image2018-1-8-163A483A32.png)

### Selenium IDE

Introducing Katalon Studio new capability that allow users to **import** Selenium IDE Scripts (Beta) into Katalon Studio for advanced scripting and test execution including advanced conditions, dynamic validation or to be executed with external data sources. 

(This feature is in beta stage. There will be some cases that imported Selenium IDE Scripts will not be converted successfully to Katalon Studio scripts. Katalon team welcomes all of your feedback and suggestions)

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-530/image2018-1-22-103A363A19.png)

### Record/Spy

*   Added ability to move captured objects in Object Repository pane for Spy and Record Web. Users can **freely move captured objects** to organize test artifacts before saving. 
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-530/image2018-1-8-163A443A6.png)


*   **[Default locators](/x/MwDR)** for captured objects in Record/Spy now can be set in **Project Setting**. Selected locators will be added automatically while Recording or Spying the application under test.

    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-530/image2018-1-25-163A563A26.png)

### Mobile Testing

*   Support iOS 11 devices


*   Enhance UI of selecting mobile devices window for test execution to improve users experience
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/new/version-530/image2018-1-26-123A63A59.png)