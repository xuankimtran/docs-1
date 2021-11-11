---
title: "Katalon Docker Image" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/docker.html 
redirect_from:
    - "/display/KD/Docker/"
    - "/x/swTR/"
    - "/katalon-studio/docs/docker/"
description: 
---

> Requirements:
> * Docker installed. You can refer to the instructions in the Docker document here: [Get Docker](https://docs.docker.com/get-docker/).
> * An active Katalon Runtime Engine floating license. To learn more about types of licenses, you can refer to this document: [Types of licenses](https://docs.katalon.com/katalon-studio/docs/license.html).

This tutorial shows you how to run the Katalon Studio test with Katalon Docker Image (KDI). This image contains up-to-date browsers, including Google Chrome, Mozilla Firefox, and Katalon Studio. Hence when running your Katalon Project with Katalon Studio Docker Image, the pre-installed Katalon Studio and Katalon Runtime Engine in your local machine are not required. 

Docker Image for Katalon Studio is available here at Docker Hub: [katalonstudio/katalon](https://hub.docker.com/r/katalonstudio/katalon/).

> You can download our Github sample project for CI configurations using Docker Image: [CI samples](https://github.com/katalon-studio/docker-images-samples).
## Pull Katalon Docker Image

To pull KDI, open **Terminal** in your local machine, copy and paste the following command line:

``` groovy
docker pull katalonstudio/katalon
```
After successfully pulling KDI, you should see the **katalonstudio/katalon** image in your Docker application.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/katalon-docker-image/KS-DOCKER-Katalon-docker-image.png" width="70%" alt="KDI in the Docker app">

If you want to check which version of Google Chrome and Mozilla Firefox the KDI supports, copy and paste the following command in the **Terminal**: 

``` groovy
docker run -t --rm katalonstudio/katalon cat /katalon/version
```
## Execute Katalon Studio tests with Katalon Docker Image

> Requirements:
> * Katalon Docker Image version 7.2.1 onwards
> * Make sure you have Docker open while running the test.

1. Open **Terminal**, then go to the test project directory you wish to run. For example, we want to run the **CI sample** test project, we will direct to our **CI sample** project in our local machine.

2. Inside your test project directory, input the following command:

    ``` groovy
    docker run -t --rm -v "$(pwd)":/tmp/project katalonstudio/katalon katalonc.sh -projectPath=/tmp/project [Option1] [Option2] ... [OptionN]
    ```
    > Notes:
    >
    > * The `katalonc.sh` command starts Katalon Studio and other necessary components. 
    > * All Katalon Studio console mode arguments are accepted except `-runMode`. You can find more command-line options at [Command Syntax](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#general-options).

    For example, we want to run the **TS_RegressionTest** test suite from the **CI sample** project with the Chrome browser in Katalon Docker Image. We enter the command as follows:

    ``` groovy
    docker run -t --rm -v "$(pwd)":/tmp/project katalonstudio/katalon katalonc.sh -projectPath=/tmp/project -browserType="Chrome" -testSuiteCollectionPath="Test Suites/TS_RegressionTestCollection" -apiKey="<your_API_key>"
    ```

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/katalon-docker-image/KS-DOCKER-Run-test-with-Docker.png" width="70%" alt="Run test with Docker">

    > Notes:
    >
    > * To avoid syntax errors, you can use the Command Builder to generate commands quickly and precisely. To learn more about the command builder, you can refer to this document: [Command Builder](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#command-builder).
    >
    > * <your_API_Key>: the API key verifies your credentials. The command-line options of API Key, including -apiKey=<Your_API_Key> and -apikey=<Your_API_Key> are both accepted. To learn more about API keys, you can refer to this document: [API key](https://docs.katalon.com/katalon-analytics/docs/ka-api-key.html#katalon-api-keys-usage).

3. You can view the console log in Docker during the test.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-docker/docker-log.png" alt="docker log" width=70%>

4. To view your report files, you can go to this directory: `<your-project-folder>/Reports` or your third-party integration like Katalon TestOps, Azure DevOps, or qTest. Katalon Studio supports exporting test reports in **HTML**, **CSV**, **PDF**, and **JUnit**.

## Proxy Configuration

If you need to configure proxies for Katalon Studio, you can refer to this document: [Proxy Options](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#proxy-options).

These proxy options must be used with the `--config` parameter, for example:

```groovy
docker run -t --rm -v "$(pwd)":/tmp/project katalonstudio/katalon katalonc.sh -projectPath=/tmp/project -browserType="Chrome" -retry=0 -statusDelay=15 -testSuitePath="Test Suites/TS_RegressionTest" -apikey="<your_API_key>" --config -proxy.option=MANUAL_CONFIG -proxy.server.type=HTTP -proxy.server.address=192.168.1.221 -proxy.server.port=8888
```
## Prevent user permissions issue on your machine

You can also run the test under the current user ID using the `KATALON_USER_ID` environment variable. This helps avoid permission issues when accessing artifacts generated after the test execution. Follow these steps:

1. Open **Terminal**, then run `id -u $USER`. The result will tell you the current user ID. Here, the user ID is: 502
   
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/katalon-docker-image/KS-DOCKER-userID.png" width="70%" alt="Current userID">

2. To execute the test with the current user ID, enter the following command line:

    ```groovy
    docker run -t --rm -e KATALON_USER_ID=<the-current-userID> -v "$(pwd)":/tmp/project katalonstudio/katalon katalonc.sh -projectPath=/tmp/project [Option1] [Option2] ... [OptionN]
    ```

<details><summary>For Katalon Docker Image below 7.2.1</summary>

## Execute Katalon Studio tests with Katalon Docker Image

> Requirements:
> * Make sure you have Docker open while running the test.

Inside your test project directory, input the following command:

```groovy
docker run -t --rm -v "$(pwd)":/katalon/katalon/source katalonstudio/katalon katalon-execute.sh [Option1] [Option2] ... [OptionN]
```
> Notes:
> * All Katalon Studio console mode arguments are accepted except `-runMode`, `-reportFolder`, and `-projectPath`. You can find more command line options at [Command Syntax](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#general-options).

<table>
	<tbody>
		<tr>
			<td><strong>KDI Command-line option</strong></td>
			<td><strong>Description</strong></td>
		</tr>
		<tr>
			<td>
				<p dir="auto"><code>katalon-execute.sh</code></p>
			</td>
			<td>This command starts Katalon Studio and other necessary components.</td>
		</tr>
		<tr>
			<td>
				<p dir="auto"><code>/katalon/katalon/source</code></p>
			</td>
			<td>
				<p>The <code>katalon-execute.sh</code> command looks for the test project inside this directory.</p>
				<p>If you don't want to use this command line, define the test project directory with the&nbsp;<code>docker run -w</code>&nbsp;argument as follows:</p>
				<p><code>docker run -t --rm -v "$(pwd)":/tmp/source -w /tmp/source katalonstudio/katalon katalon-execute.sh [Option1] [Option2] ... [OptionN]</code></p>
			</td>
		</tr>
	</tbody>
</table>

</details>

## See also
- [Integrate Jenkins on Docker hosted in Ubuntu](https://docs.katalon.com/katalon-studio/docs/jenkins-docker-ubuntu.html)
- [Integrate Jenkins Pipeline (Jenkinsfile) with Katalon Studio Docker Image](https://docs.katalon.com/katalon-studio/docs/jenkins-pipeline-docker.html)