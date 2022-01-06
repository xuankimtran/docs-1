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
   - "/katalon-studio/tutorials/executing_console_mode.html"
description:
---
You can execute an automation test without launching Katalon Studio by using command-line mode execution.

> Requirements:
> * Katalon Runtime Engine installed. You can download Katalon Runtime Engine here: [Katalon products](https://www.katalon.com/all-products/).
> * A Katalon Runtime Engine License. To learn more about activating your license, you can refer to this document: [Katalon license](https://docs.katalon.com/katalon-studio/docs/activate-license.html#activate-a-license-with-internet-access).

> Notes:
> * Katalon Studio only supports **Chrome, Firefox, and Remote** options for console mode execution using the **Linux** version.
> * From version 7.9.0 onwards, you can upgrade the default JRE 8 to higher versions in console mode. You can refer to this document for further details: [Run tests with another JRE in the command line](https://docs.katalon.com/katalon-studio/how-to-guides/set-new-default-JRE.html#use-the-newly-added-jre-in-a-test-project).

## Execute Katalon Studio in console mode

> The Katalon launcher (`katalon.exe`) is replaced by `katalonc.exe`.

1. Open the command prompt and navigate to the folder of your Katalon Studio build: `katalonc.exe` (Windows), Applications folder (Mac OS), or `katalonc` (Linux) file.
2. Enter the following syntax to execute your test:

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

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/console-mode-execution/katalonc.png" width="80%" alt="Execute Katalon in console mode">

3. Press **Enter** to start execution.
4. **Exit Code**

   Below is the list of exit codes after console mode execution:

   * 0: the execution passed with no failed or error test case.
   * 1: the execution has failed test cases.
   * 2: the execution has error test cases.
   * 3: the execution has failed test cases and error test cases.
   * 4: the execution cannot start because of invalid arguments.

## Use Plugins in Console Mode

You can also continue using your plugins of choice with console commands. See this guide: [Use Plugins in Console Mode](https://docs.katalon.com/katalon-studio/docs/kse-use-plugins.html#use-plugins-in-console-mode).

## General Options

Here's the list of options supported for the `katalonc` commands for Katalon Studio version 7.0.0 onwards.

<table>
	<thead>
		<tr>
			<th>Katalonc Command-line Option</th>
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
			</td>
			<td>Y (<em>If -testSuitePath is not used. Otherwise it's optional</em>)</td>
		</tr>
		<tr>
			<td>-browserType=&lt;browser&gt;</td>
			<td>
				<p>Specify the browser type used for test suite execution.</p>
				<p>From version 7.6+, you can use this option in Test Suite Collection execution. The specified browser is used for all test suites in that collection.</p>
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
				<p><strong>Only Chrome, Firefox, and Remote</strong> are available for use in the Linux version.</p>
				<p><strong><code>Web Service</code> is used for Web Service test execution. </strong></p>
			</td>
		</tr>
		<tr>
			<td>-retry=&lt;number of retry times&gt;</td>
			<td>Number of times running test cases in the test suite.</td>
			<td>N</td>
		</tr>
		<tr>
			<td>-retryStrategy=&lt;allExecutions,failedExecutions,immediately&gt;</td>
			<td>
				<p>This option is supported in version 7.6 onwards. Specify which execution to be retried (this parameter overrides setting in test suite file):</p>
				<ul>
					<li><strong>allExecutions</strong>: Retry all executions when the Test Suite fails</li>
					<li><strong>failedExecutions</strong>: Retry only failed executions when the Test Suite fails</li>
					<li><strong>immediately</strong>: Retry a failed execution of a test case or test data immediately. (Only for Katalon Studio Enterprise users)</li>
				</ul>
			</td>
			<td>N</td>
		</tr>
		<tr>
			<td>-reportFolder=&lt;path&gt;</td>
			<td>Specify the destination folder for saving report files. You can use an absolute path or relative path (root being project folder).</td>
			<td>N</td>
		</tr>
		<tr>
			<td>-maxFailedTests=&lt;T&gt;</td>
			<td>
				<ul>
					<li><span data-preserver-spaces="true">From version 8.1.0, you can terminate a test suite/ test suite collection execution based on the number of test failures.</span></li>
					<li><span data-preserver-spaces="true">Set &lt;T&gt; as the maximum number of total test failures allowed in the execution. Reaching &lt;T&gt; terminates the test execution.</span></li>
					<li><span data-preserver-spaces="true">A test failure is counted when any of these type of tests fails: test case, retried test case, test iteration, or retried test iteration.</span></li>
				</ul>
			</td>
			<td>N&nbsp;</td>
		</tr>
		<tr>
			<td>-reportFileName=&lt;name&gt;</td>
			<td>Specify the name for report files (.html, .csv, .log). If not provided, the system uses the name "report" (report.html, report.csv, report.log). This option is only taken into account when being used with the "-reportFolder" option.</td>
			<td>N</td>
		</tr>
		<tr>
			<td>-sendMail=&lt;e-mail address&gt;</td>
			<td>Specify the e-mail address for receiving report files. If the e-mail address was not specified, the report files are not to be sent.</td>
			<td>N</td>
		</tr>
		<tr>
			<td>-remoteWebDriverUrl=&lt;remote web server url&gt;</td>
			<td>Specify the remote web driver URL.</td>
			<td>N</td>
		</tr>
		<tr>
			<td>-remoteWebDriverType=&lt;Selenium, Appium&gt;</td>
			<td>Remote web's driver type.</td>
			<td>Y <em>(If -remoteWebDriverUrl is used)</em></td>
		</tr>
		<tr>
			<td>-deviceId=&lt;device Id for Android/device UUID for ios&gt;</td>
			<td>Specify the device's ID to execute test scripts using this device.</td>
			<td>Y<em> (If -browserType=Android or -browserType=iOS is used)</em></td>
		</tr>
		<tr>
			<td>-executionProfile</td>
			<td>
				<p>Specify the execution profile that a test suite executes with</p>
				<p>From version 7.6+, you can use this option in Test Suite Collection execution. The specified execution profile is applied to all test suites in that collection.</p>
			</td>
			<td>N</td>
		</tr>
		<tr>
			<td>
				<p data-pm-slice="1 1 []">-delayBetweenInstances=&lt;value&gt;</p>
			</td>
			<td>
				<ul>
					<li>From Katalon version 8.2.0 onwards, you can set a delay between each test suite execution in a Test Suite Collection.</li>
				</ul>
				<ul>
					<li><code>Value</code> is a positive integer from 0-999 seconds.</li>
				</ul>
				<ul>
					<li>When a test suite is ready to start, KRE prints a message in Console Log: <code>Test suite ${testSuiteID} is ready to start at ${currentTimeStamp}</code><br />&nbsp;</li>
				</ul>
			</td>
			<td>N</td>
		</tr>
		<tr>
			<td>-g_XXX</td>
			<td>
				<p>Override Execution Profile variables.</p>
				<p>Example:</p>
				<p><code> -g_userName="admin"</code></p>
			</td>
			<td>N</td>
		</tr>
		<tr>
			<td>--info -buildLabel="text" -buildURL="text"</td>
			<td>
				<p>Pass the build's label and URL, which are displayed in Katalon TestOps.</p>
				<p>Example:</p>
				<p><code> --info -buildLabel="Build 1" -buildURL="http://192.168.35.52:8080/job/katalon-demo/job/master/179/"</code></p>
			</td>
			<td>N</td>
		</tr>
		<tr>
			<td>-testOpsBuildId</td>
			<td>
				<p>From version 8.0.0, you can specify the build ID to update the Test Suite/Test Suite Collection report.</p>
				<p>Example:</p>
				<p><code> -testOpsBuildId=24 </code></p>
			</td>
			<td>N</td>
		</tr>
		<tr>
			<td>-testSuiteCollectionQuery</td>
			<td>
				<p>From version 8.0.0, you can enable or disable Test Suite(s) in Test Suite Collection.</p>
				<p>Example:</p>
				<p><code> -testSuiteCollectionQuery=&rdquo;indexes=(1,3)&rdquo; </code></p>
			</td>
			<td>N</td>
		</tr>
		<tr>
			<td>-maxResponseSize</td>
			<td>
				<p>Override the maximum response size in project setting (available from version 7.6). <a href="https://docs.katalon.com/katalon-studio/docs/execution-settings.html#web-service-settings">Learn more about Web Service Settings.</a></p>
				<p>Example:</p>
				<p><code> -maxResponseSize=400</code></p>
			</td>
			<td>N</td>
		</tr>
		<tr>
			<td>
				<p>-licenseRelease</p>
				<p>-orgID=&lt;organization's id&gt;</p>
			</td>
			<td>
				<p>From version 8.0.0, you can release the previous execution session before checking the license.</p>
				<p>Example:</p>
				<p><code> -licenseRelease=true </code></p>
				<p><code> -orgID=89151</code></p>
			</td>
			<td>N</td>
		</tr>
	</tbody>
</table>

### Windows-Only Options

<table>
   <thead>
      <tr>
         <th style="width:40%">Katalonc Command-line Option</th>
         <th style="width:30%">Description</th>
         <th>Mandatory?</th>
      </tr>
   </thead>
   <tbody>
      <tr>
         <td>-consoleLog</td>
         <td>Display log in the console. Only use this option when running Katalon Studio in Windows Command Prompt. Do not use this option in other OSes or CI tools, for example Jenkins.</td>
         <td>N</td>
      </tr>
      <tr>
         <td>-noExit</td>
         <td>Keep the console open after the execution is completed. Only use this option when running Katalon Studio in Windows Command Prompt. Do not use this option in other OSes or CI tools, for example Jenkins.</td>
         <td>N</td>
      </tr>
   </tbody>
</table>

## Proxy Options

> Notes:
> * From version 7.5.0 onwards, there are two types of proxy configurations: Authentication and System proxies. To learn more about configuring different proxy preferences, you can refer to this document: [Proxy Preferences](https://docs.katalon.com/katalon-studio/docs/proxy-preferences.html) for further details.
> * From version 7.2.0 onwards, you can exclude a list of hosts from proxy in the **Manual proxy configuration**. To learn more about manually excluding domains from proxy, you can refer to this document: [Proxy settings](https://docs.katalon.com/katalon-studio/docs/katalon-studio-preferences.html#proxy-settings).
> * From version 7.0.0 onwards, you can pass proxy details via a request object in Web Service testing. To learn more about passing proxy details in script mode, you can refer to this document: [Override proxy details in the test script](https://docs.katalon.com/katalon-studio/docs/katalon-studio-preferences.html#override-proxy-details-in-the-test-script).

These proxy options must be used with `--config` parameter, for example `--config -proxy.auth.option=MANUAL_CONFIG`.

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

- For Katalon version 7.5.0 onwards, do as follows:

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

- For versions older than 7.5.0, do as follows:

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

## Integration Options

<table>
   <thead>
      <tr>
         <th style="width:40%">Katalonc Command-line Option</th>
         <th style="width:30%">Description</th>
         <th>Mandatory?</th>
      </tr>
   </thead>
   <tbody>
      <tr>
         <td>-testcloudEnvironmentId</td>
         <td>
            <p>The ID of the environment which corresponds to a combination of OS, browser type and browser version to execute (Available from 8.2.5 onwards).</p>
            <p><em>Note: This parameter already contains the information about browser type. So the browserType parameter is not generated in this integration.</em></p>
         </td>
         <td>Y</td>
      </tr>
      <tr>
         <td>-testcloudTunnel</td>
         <td>Allow the execution to be performed via a tunnel (Available from 8.2.5 onwards).</td>
         <td>N</td>
      </tr>
      <tr>
         <td>--config -kobiton.authentication.username=[yourKobitonusername] -kobiton.authentication.password=xxxxx</td>
         <td>Passing Kobiton username and password</td>
         <td>N</td>
      </tr>
      <tr>
         <td>--config -kobiton.authentication.serverUrl=[defaultKobitonServer] -kobiton.authentication.username=[yourKobitonUsername] -kobiton.authentication.apiKey=[yourKobitonAPIKey</td>
         <td>Passing Kobiton Server URL, username, and APIKey (Available in 7.8 and later)</td>
         <td>N</td>
      </tr>
      <tr>
         <td>-kobitonDeviceId=[yourKobitonDeviceId]</td>
         <td>Passing Kobiton Device ID (Available in 7.8 and later)</td>
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
      <tr>
         <td>--info -qTestBuildNumber="text" --qTestBuildURL="text"</td>
         <td>
         <p>Introduced in version 7.8.5. Pass the build's number and URL to Test Run properties on qTest.</p>
         <p>Example:</p>
         <p><code class="java plain"> Example: --info -qTestBuildNumber="Build 1" -qTestBuildURL="http://192.168.35.52:8080/job/katalon-demo/job/master/179/"</code></p>
         </td>
         <td>N</td>
      </tr>
      <tr>
         <td>-adoPlanId=&lt;testplan id&gt;</td>
         <td>
         <p>ID of the test plan used for submitting test run(s)(available from version 8.0.0).</p>
         </td>
         <td>N</td>
      <tr>
         <td>-adoTestRunName="text"</td>
         <td>
         <p>From version 8.0.0, you can create test run(s) on ADO with the specified name.</p>
         </td>
         <td>N</td>
      </tr>
      <tr>
	<td>--info -adoDefinitionID=&lt;DefinitionID&gt;</td>
	<td>
	<p>From version 8.0.0, you can get the latest completed Build ID of the specified Definition ID and pass it to Test Run properties on ADO.</p>
	</td>
	<td>N</td>
      </tr>
   </tbody>
</table>

## Automatically Updating WebDriver Option

<table>
   <thead>
      <tr>
         <th>Katalonc Command-line Option</th>
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

## Command Builder

We recommend using the Command Builder to generate commands quickly and precisely. Please do as follows:

1. Click on **Build CMD** from the main toolbar.
   
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/console-mode-execution/command%20builder.png" alt="Build CMD" width=70%>

2. The **Generate Command for Console Mode** is displayed. Configure your execution with the provided options:

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/console-mode-execution/generate-for-console-mode.png" alt="Generate Command for Console Mode" width=90%>

  * **Test Suite**: The Test Suite or Test Suite Collection to be executed.
  * **Executive Platform**:
   
      * **Run with** and **Profile**: Testing environment of the execution. 
      
         From version 8.2.5 onwards, you can integrate and run your test with TestCloud - a cloud-based test execution environment. To learn more about the configuration and execution with TestCloud in console mode, see [Run TestCloud with Katalon Runtime Engine](https://docs.katalon.com/katalon-studio/docs/testcloud-integration-kre.html).
     
         <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/console-mode-execution/select-environment.png" alt="select environment" width=70%>

      * **Profile**: Execution profile of the execution. 
      * **Override the execution profile and environment of all test suites**: Check if you want the specified `-BrowserType` and `-ExecutionProfile` in the command to override the browser type and execution profile of all test suites in the collection (available from version 7.6 onwards)

   * **Authentication**: 
   
     * **API Keys**: API Keys are used to represent a user's credentials. The command-line options of API Key, including `-apiKey=<Your_API_Key>` and `-apikey=<Your_API_Key>` are both accepted. To learn more about API keys, you can refer to this document: [API key](https://docs.katalon.com/katalon-studio/docs/katalon-apikey-70.html).
     * From version 7.7.0 onwards, if you belong to more than one Organization subscribing to Runtime Engine (RE) licenses, you can choose which Organization validates your license usage. Katalon retrieves and displays the Organizations your Katalon account is bound to, as well as which Organizations have made RE licenses available to you. Once selected, the Organization ID is passed to the generated command (`-orgID=<Katalon_OrgID>`).

   * **Execution Configurations** (Or **Other Options** in versions older than 7.7.0).
   
      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/console-mode-execution/condition%20to%20stop%20-%202.png" alt="execution configurations" width=60%>

      From version 8.1.0 onwards, you can terminate execution after T test failures (T is the failure threshold value) with the option: **Terminate the execution once the total number of test failures reaches the input threshold**. See also: [Terminate Execution Conditionally](https://docs.katalon.com/katalon-studio/docs/terminate-execution-conditionally.html).
   * **Katalon TestOps**: Override the Project ID in Katalon TestOps (available from version 7.8 onwards).

       <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/console-mode-execution/generate-testops-CI-command.png" alt="Katalon TestOps" width=90%>

3. Click **Generate Command** after completing the configuration.

4. You can **Copy to Clipboard** and paste to the Command Prompt/Terminal for execution.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/console-mode-execution/command1.png" alt="generate command" width=70%>

## Use the console.properties file

We support running console mode using the **console.properties** file where you can manually modify the content if needed.

1. Generate a **console.properties** file using our generator.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/console-mode-execution/console-properties.png" alt="Generate a console.properties" width=90%>

2. The **console.properties** file is generated at your preferred location. You can open and update the parameters manually as needed.

    For example:

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/console-mode-execution/console.properties-file.png" alt="console.properties" width=70%>

3. Run the **console.properties** file in console mode with the following syntax.

   ```groovy
   katalonc -propertiesFile="<absolute path to console.properties file>" -runMode=console -apiKey="<Your_API_Key>"
   ```

   For example:

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/console-mode-execution/property-apikey.png" alt="console.properties" width=100%> 

4. You can add additional `katalonc` command options if needed. Any option already defined in the **console.properties** file is overwritten by the one declared in the command line.  

    ```groovy
    katalonc -propertiesFile="<absolute path to console.properties file" -runMode=console -apiKey="<Your_API_Key>" -browserType=IE
    ```

    In the example above, since we also declare `browserType` option in the command line, the automation test is executed using IE instead of Chrome.
