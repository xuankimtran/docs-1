---
title: "Command Syntax (Command-line/Console Mode Execution)"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/console-mode-execution.html
redirect_from:
   - "/display/KD/Console+Mode+Execution/"
   - "/display/KD/Console%20Mode%20Execution/"
   - "/x/WQAM/"
   - "/katalon-studio/docs/console-mode-execution/"
   - "/katalon-studio/tutorials/generate_command_line.html"

description:
---

> Notes:
> 
> Starting from **version 7.0.0**, you need a Runtime Engine (RE) [license](https://docs.katalon.com/katalon-studio/docs/license.html) to activate and run Katalon Studio (KS) or Katalon Studio Enterprise (KSE) from the command line.
>
> Katalon Studio only supports **Chrome, Firefox and Remote** options for console mode execution **using Linux version**.
>
> API Keys are required to use **Katalon Studio Plugins** in console mode. [Learn more](/katalon-store/docs/user/plugin-console-installation.html).

You can execute automation test without launching Katalon Studio by using command line mode execution.

Execute Katalon in CMD
----------------------

> Starting from **Katalon Studio version 7.0.0**, you need to download the Runtime Engine package from [Katalon website](https://katalon.com/download). The Katalon launcher (`katalon.exe`) is replaced by `katalonc.exe`.

1. Open the command prompt and navigate to the folder of your Katalon Studio build: `katalonc.exe` (Windows), Applications folder (Mac OS), or `katalonc` (Linux) file.

2. Enter the following syntax to execute automation test:

    **Windows:**

    ```groovy
    katalonc {option1} {option2} ... {optionN}
    ```

    **macOS:**

    ```groovy
    cd /Applications/Katalon\ Studio\ Engine.app/Contents/MacOS 

    ./katalonc --args {option1} {option2} ... {optionN}
    ```

    **Linux**:

    ```groovy
    ./katalonc {option1} {option2} ... {optionN}
    ```

    For example:

   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/console-mode-execution/katalonc.png)

3. Press **Enter** to start execution.
4. **Exit Code**

   Below is the list of exit codes after console mode execution:

   * 0: the execution passed with no failed or error test case.
   * 1: the execution has failed test cases.
   * 2: the execution has error test cases.
   * 3: the execution has failed test cases and error test cases.
   * 4: the execution cannot start because of invalid arguments.

Katalon Studio Plugins in Console Mode
--------------------------------------

> To be used in console mode, Katalon Studio Plugins must be installed using Katalon Store's API keys. Please follow instructions [here](/katalon-store/docs/user/plugin-console-installation.html).

General Options
---------------

Here's the list of options supported for the `katalon` commands in Katalon Studio prior to version 7.0.0, and the `katalonc` commands for Katalon Studio version 7.0.0 and later.

<table>
   <thead>
      <tr>
         <th>Katalonc Command Line Option</th>
         <th>Description</th>
         <th>Mandatory?</th>
      </tr>
   </thead>
   <tbody>
      <tr>
         <td>-runMode=console</td>
         <td>Enable console mode.</td>
         <td>Y</td>
      </tr>
      <tr>
         <td>-statusDelay=&lt;seconds&gt;</td>
         <td>System updates execution status of the test suite after the delay period (in seconds) specified.</td>
         <td>N</td>
      </tr>
      <tr>
         <td>-projectPath=&lt;path&gt;</td>
         <td>Specify the project location (include .prj file). The absolute path must be used in this case.</td>
         <td>Y</td>
      </tr>
      <tr>
         <td>-testSuitePath=&lt;path&gt;</td>
         <td>Specify the test suite file (without extension .ts). The relative path (root being project folder) must be used in this case.</td>
         <td>Y</td>
      </tr>
      <tr>
         <td>-testSuiteCollectionPath=&lt;path&gt;</td>
         <td>
            <p>Specify the test suite file (without extension .tsc). The relative path (root being project folder) must be used in this case.</p>
            <p>Note: Available only in 4.4+</p>
         </td>
         <td>Y (<em>If -testSuitePath is not used. Otherwise it's optional</em>)</td>
      </tr>
      <tr>
         <td>-browserType=&lt;browser&gt;</td>
         <td>
            <p>Specify the browser type used for test suite execution.</p>
            <p>The following browsers are supported in Katalon:</p>
            <ul>
               <li>Firefox</li>
               <li>Chrome</li>
               <li>IE</li>
               <li>Edge</li>
               <li>Edge (Chromium)</li>
               <li>Safari</li>
               <li>Remote</li>
               <li>Android</li>
               <li>iOS</li>
               <li>Web Service</li>
            </ul>
         </td>
         <td>
            <p>Y</p>
            <p>
               <strong>Only Chrome, Firefox and Remote is available for use in Linux version.</strong>
            </p>
            <p>
               <strong><code>Web Service</code> is used for Web Service test execution.
            </p>
         </td>
      </tr>
      <tr>
         <td>-retry=&lt;number of retry times&gt;</td>
         <td>Number of times running test cases in the test suite.</td>
         <td>N</td>
      </tr>
      <tr>
         <td>-retryFailedTestCases=&lt;true, false&gt;</td>
         <td>Retry failed test cases fail in test suite ( override setting in test suite file ). There are 2 options for retry: true if you want run fail test case and otherwise false</td>
         <td>N</td>
      </tr>
      <tr>
         <td>-reportFolder=&lt;path&gt;</td>
         <td>Specify the destination folder for saving report files. Can use absolute path or relative path (root being project folder).</td>
         <td>N</td>
      </tr>
      <tr>
         <td>-reportFileName=&lt;name&gt;</td>
         <td>Specify the name for report files (.html, .csv, .log). If not provide, system uses the name "report" (report.html, report.csv, report.log). This option is only taken into account when being used with "-reportFolder" option.</td>
         <td>N</td>
      </tr>
      <tr>
         <td>-sendMail=&lt;e-mail address&gt;</td>
         <td>Specify the e-mail address for receiving report files. If the e-mail address was not specified, the report files is not to be sent.</td>
         <td>N</td>
      </tr>
      <tr>
        <td>-remoteWebDriverUrl=&lt;remote web server url&gt;</td>
        <td>Specify the remote web driver URL</td>
        <td>N</td>
      </tr>
      <tr>
         <td>-remoteWebDriverType=&lt;Selenium, Appium&gt;</td>
         <td>Remote web's driver type</td>
         <td>Y <em>(If -remoteWebDriverUrl is used)</em></td>
      </tr>
      <tr>
         <td>-deviceId=&lt;device Id for Android/device uuid for ios&gt;</td>
         <td>Specify the device's ID to execute test scripts using this device</td>
         <td>Y<em> (If -browserType=Android or -browserType=iOS is used)</em></td>
      </tr>
      <tr>
         <td>-executionProfile</td>
         <td>
            <p><strong>Starting from Katalon Studio version 5.4</strong></p>
            <p>Specify the&nbsp;<a href="/pages/viewpage.action?pageId=13697476">execution profile</a>&nbsp;to be executed with</p>
         </td>
         <td>N</td>
      </tr>
      <tr>
         <td>-g_XXX</td>
         <td>
            <p><strong>Starting from Katalon Studio version 5.9</strong></p>
            <p>Override Execution Profile variables.</p>
            <p>Example:</p>
            <p><code class="java plain"> -g_userName="admin"</code></p>
         </td>
         <td>N</td>
      </tr>
      <tr>
         <td>--info -buildLabel="text" -buildURL="text" </td>
         <td>
            <p><strong>Starting from Katalon Studio version 7.0</strong></p>
            <p>Pass the build's label and URL, which are displayed in Katalon TestOps.</p>
            <p>Example:</p>
            <p><code class="java plain"> --info -buildLabel="Build 1" -buildURL="http://192.168.35.52:8080/job/katalon-demo/job/master/179/"</code></p>
         </td>
         <td>N</td>
      </tr>
   </tbody>
</table>

Windows-Only Options
--------------------

<table>
   <thead>
      <tr>
         <th>Katalonc Command Line Option</th>
         <th>Description</th>
         <th>Mandatory?</th>
      </tr>
   </thead>
   <tbody>
      <tr>
         <td>-consoleLog</td>
         <td>Display log in the console. Only use this option when running Katalon Studio in Windows Command Prompt. Do not use this option in other OSes or CI tools e.g. Jenkins.</td>
         <td>N</td>
      </tr>
      <tr>
         <td>-noExit</td>
         <td>Keep the console open after the execution is completed. Only use this option when running Katalon Studio in Windows Command Prompt. Do not use this option in other OSes or CI tools e.g. Jenkins.</td>
         <td>N</td>
      </tr>
   </tbody>
</table>

Proxy Options
-------------

>In **version 7.5+**, there are two types of proxy configurations: Authentication and System proxies. Refer to [this document](https://docs.katalon.com/katalon-studio/docs/proxy-preferences.html) for further details.
>
> In **version 7.2+**, you can exclude proxy in **manual** configuration.
>
> In **version 7.0+**, you can pass proxy details via a request object in Web Service testing. Refer to [this document](https://docs.katalon.com/katalon-studio/docs/proxy-preferences.html#pass-proxy-details-through-the-script) for further details.

These proxy options must be used with `--config` parameter e.g. `--config -proxy.auth.option=MANUAL_CONFIG`.

```groovy
katalonc -noSplash -runMode=console -projectPath="C:\Users\Katalon Studio\Project\YourProject.prj" -retry=0 -testSuitePath="Test Suites/download" -executionProfile="default" -browserType="Chrome" --config -proxy.auth.option=MANUAL_CONFIG -proxy.auth.server.type=HTTP -proxy.auth.server.address=192.168.1.16 -proxy.auth.server.port=16000 -proxy.system.option=MANUAL_CONFIG -proxy.system.server.type=HTTP -proxy.system.server.address=127.0.0.1 -proxy.system.server.port=12701 -proxy.system.username=katalon -proxy.system.password=T3stP@zZW0rol -proxy.system.applyToDesiredCapabilities=true
```

### Authentication Proxy

<table>
   <thead>
      <tr>
         <th>Authentication Proxy Option</th>
         <th>Description</th>
         <th>Mandatory?</th>
      </tr>
   </thead>
   <tbody>
      <tr>
         <td colspan="3">
            <strong>
         </td>
      </tr>
      <tr>
         <td>-proxy.auth.option</td>
         <td>NO_PROXY, USE_SYSTEM, MANUAL_CONFIG</td>
         <td>Y</td>
      </tr>
      <tr>
         <td>-proxy.auth.server.type</td>
         <td>&nbsp;HTTP, HTTPS, or SOCKS</td>
         <td>Y</td>
      </tr>
      <tr>
         <td>-proxy.auth.server.address</td>
         <td>Example: locahost,&nbsp;<a class="external-link" href="katalon.com" rel="nofollow">katalon.com</a></td>
         <td>Y</td>
      </tr>
      <tr>
         <td>-proxy.auth.server.port</td>
         <td>Example: 80, 8080, 9999</td>
         <td>Y</td>
      </tr>
      <tr>
         <td>-proxy.auth.excludes</td>
         <td>Example: 127.0.0.1, localhost, myserver.com</td>
         <td>N</td>
      </tr>
      <tr>
         <td>-proxy.auth.username</td>
         <td>Example:&nbsp;MyProxyUsername</td>
         <td>Optional (YES if your proxy server requires authentication)</td>
      </tr>
      <tr>
         <td>-proxy.auth.password</td>
         <td>Example: MyProxyPassword</td>
         <td>Optional (YES if your proxy server requires authentication)</td>
      </tr>
   </tbody>
</table>

### System Proxy

<table>
   <thead>
      <tr>
         <th>System Proxy Option</th>
         <th>Description</th>
         <th>Mandatory?</th>
      </tr>
   </thead>
   <tbody>
      <tr>
         <td colspan="3">
            <strong>
         </td>
      </tr>
      <tr>
         <td>-proxy.system.option</td>
         <td>NO_PROXY, USE_SYSTEM, MANUAL_CONFIG</td>
         <td>Y</td>
      </tr>
      <tr>
         <td>-proxy.system.server.type</td>
         <td>&nbsp;HTTP, HTTPS, or SOCKS</td>
         <td>Y</td>
      </tr>
      <tr>
         <td>-proxy.system.server.address</td>
         <td>Example: locahost,&nbsp;<a class="external-link" href="katalon.com" rel="nofollow">katalon.com</a></td>
         <td>Y</td>
      </tr>
      <tr>
         <td>-proxy.system.server.port</td>
         <td>Example: 80, 8080, 9999</td>
         <td>Y</td>
      </tr>
      <tr>
         <td>-proxy.system.excludes</td>
         <td>Example: 127.0.0.1, localhost, myserver.com</td>
         <td>N</td>
      </tr>
      <tr>
         <td>-proxy.system.username</td>
         <td>Example:&nbsp;MyProxyUsername</td>
         <td>Optional (YES if your proxy server requires authentication)</td>
      </tr>
      <tr>
         <td>-proxy.system.password</td>
         <td>Example: MyProxyPassword</td>
         <td>Optional (YES if your proxy server requires authentication)</td>
      </tr>
      <tr>
         <td>-proxy.system.applyToDesiredCapabilities</td>
         <td>Example: true or false </td>
         <td>N</td>
      </tr>
   </tbody>
</table>

### Proxy Configurations prior to 7.5.0

<table>
   <thead>
      <tr>
         <th>Option</th>
         <th>Description</th>
         <th>Mandatory?</th>
      </tr>
   </thead>
   <tbody>
      <tr>
         <td colspan="3">
            <strong>
         </td>
      </tr>
      <tr>
         <td>-proxy.option</td>
         <td>NO_PROXY, USE_SYSTEM, MANUAL_CONFIG</td>
         <td>Y</td>
      </tr>
      <tr>
         <td>-proxy.server.type</td>
         <td>&nbsp;HTTP, HTTPS, or SOCKS</td>
         <td>Y</td>
      </tr>
      <tr>
         <td>-proxy.server.address</td>
         <td>Example: locahost,&nbsp;<a class="external-link" href="katalon.com" rel="nofollow">katalon.com</a></td>
         <td>Y</td>
      </tr>
      <tr>
         <td>-proxy.server.port</td>
         <td>Example: 80, 8080, 9999</td>
         <td>Y</td>
      </tr>
      <tr>
         <td>-proxy.excludes</td>
         <td>Example: 127.0.0.1, localhost, myserver.com</td>
         <td>N</td>
      </tr>
      <tr>
         <td>-proxy.username</td>
         <td>Example:&nbsp;MyProxyUsername</td>
         <td>Optional (YES if your proxy server requires authentication)</td>
      </tr>
      <tr>
         <td>-proxy.password</td>
         <td>Example: MyProxyPassword</td>
         <td>Optional (YES if your proxy server requires authentication)</td>
      </tr>
   </tbody>
</table>

Integration Options
-------------------

<table>
   <thead>
      <tr>
         <th>Katalonc Command Line Option</th>
         <th>Description</th>
         <th>Mandatory?</th>
      </tr>
   </thead>
   <tbody>
      <tr>
         <td>--config -kobiton.authentication.username=[yourKobitonusername]-kobiton.authentication.password=xxxxx</td>
         <td>Passing Kobiton username and password</td>
         <td>N</td>
      </tr>
      <tr>
         <td>-qTestDestId=&lt;destination's id&gt;</td>
         <td>Id of the destination where the result is uploaded on it</td>
         <td>N</td>
      </tr>
      <tr>
         <td>-qTestDestType=&lt;destination's type&gt;</td>
         <td>Type of the destination. There are 4 options for destination's type:"test-suite", "test-cycle", &nbsp;"release", and "root".</td>
         <td>N</td>
      </tr>
   </tbody>
</table>

Automatically Updating WebDriver Option
-------------------

<table>
   <thead>
      <tr>
         <th>Katalonc Command Line Option</th>
         <th>Description</th>
         <th>Mandatory?</th>
      </tr>
   </thead>
   <tbody>
      <tr>
         <td>--config -webui.autoUpdateDrivers=true</td>
         <td>Allow WebDriver binaries to be updated automatically in console mode.</td>
         <td>N</td>
      </tr>
   </tbody>
</table>

Command Builder
---------------

Use the following steps to quickly generate commands to use in console mode:  

1. Click on **Build CMD** from the main toolbar.
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/console-mode-execution/Screenshot-at-Jun-20-15-42-46.png)

2. The **Generate Command for Console Mode** is displayed. Configure your options as needed.
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/console-mode-execution/image2018-2-9-113A443A30.png)
    where:

    <table><thead><tr><th>Section</th><th>Description</th></tr></thead><tbody><tr><td>Test Suite</td><td>The Test Suite or Test Suite Collection to be executed</td></tr><tr><td>Executed Platform</td><td><p>The platform to execute the test on. Select an environment</p><p><img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/console-mode-execution/image2018-2-9-123A13A31.png"></p><p>&nbsp;</p></td></tr><tr><td>Other Options</td><td><p><img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/console-mode-execution/image2017-2-17-163A193A15.png"></p></td></tr></tbody></table>

3. Click **Generate Command** after completing the configuration.
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/console-mode-execution/image2017-2-17-173A153A41.png)

4. You can **Copy to Clipboard** and paste to command prompt for execution.

Use console.properties file
---------------------------

We support running console mode using **console.properties** file where you can manually modify the content if needed.

1. Generate **console.properties** file using our generator:
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/console-mode-execution/image2018-2-9-123A33A30.png)

2. The **console.properties** file is generated at your preferred location. You can open and update the parameters manually as needed.
    For example:
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/console-mode-execution/image2017-2-20-103A303A2.png)

3. Run the **console.properties** file in console mode with the following syntax:

   ```groovy
   katalonc -propertiesFile="<absolute path to console.properties file>" -runMode=console -apiKey="<Your_API_Key>"
   ```

   For example:

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/console-mode-execution/property-apikey.png"> 

4. You can add additional `katalonc` command options if needed. Any option already defined in the **console.properties** file is overwritten by the one declared in the command line.  

    ```groovy
    katalonc -propertiesFile="<absolute path to console.properties file" -runMode=console -apiKey="<Your_API_Key>" -browserType=IE
    ```

    In the example above, since we also declare `browserType` option in the command line, the automation test is executed using IE instead of Chrome.
