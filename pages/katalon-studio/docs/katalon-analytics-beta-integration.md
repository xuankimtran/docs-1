---
title: "Katalon TestOps Integration" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/katalon-analytics-beta-integration.html 
redirect_from:
    - "/display/KD/Katalon+Analytics+%28Beta%29+Integration/"
    - "/display/KD/Katalon%20Analytics%20%28Beta%29%20Integration/"
    - "/x/KRhO/"
    - "/display/KA/Integration+with+Katalon+Studio/"
    - "/display/KA/Integration%20with%20Katalon%20Studio/"
    - "/katalon-analytics/docs/integration-with-katalon-studio/"
    - "/katalon-analytics/docs/ka-integration-katalon-studio/"
    - "/katalon-analytics/docs/integration-with-katalon-studio.html"
    - "/katalon-analytics/docs/ka-integration-katalon-studio.html"
    - "/x/mw3R/"
---
Katalon TestOps (Beta) is an application that provides an in-depth view of test execution reports through powerful visualization including charts, graphs, and metrics. Currently, Katalon TestOps supports integration with Katalon Studio for better test report management.

Currently, there are two versions of Katalon TestOps. One is a [cloud-based application](https://docs.katalon.com/katalon-analytics/docs/overview.html) and the other is on-premise software that's called [Katalon TestOps OnPremise (KTOP)](https://docs.katalon.com/katalon-analytics/docs/ktop-overview.html) working in network-restricted environments

Starting in **Katalon Studio version 7.0**, you need to specify the organization you're working on to log in to Katalon Studio. If you want to switch to another organization, you have to deactivate and reactivate Katalon Studio.

To configure the Katalon TestOps Integration, right after logging in:

* Select a team in the configured organization that you have permission to access.

* Select a project under that team you’d like to work on or create your own one if you have permission.

## Settings

In Katalon Studio, go to **Project > Settings > Katalon TestOps**.

### Authentication

This section is for integrating Katalon Studio with Katalon TestOps OnPremise. If you currently use Katalon TestOps, the Server URL: `https://analytics.katalon.com` and all the credentials required for authentication have been auto-filled right after your Katalon Studio activation. Hence, skip this part and go to [**Integration**](https://docs.katalon.com/katalon-studio/docs/katalon-analytics-beta-integration.html#integration).

> **Requirements**:
>
> You have set up Katalon TestOps OnPremise successfully.
> You have an active Katalon Runtime Engine license for remote execution with Katalon TestOps OnPremise.

1. Check the **Override authentication** checkbox to enable this feature.
2. Enter required credentials of your KTOP account, including:

  * **Server URL**: the local server of your KTOP.
  * **Email** and **Password**: your KTOP account.

3. Click **Fetch Organizations** to retrieve all the available organizations to which your account belongs.
4. Select an organization to work on.

### Integration

You must enable **Katalon TestOps Integration** to submit test execution reports to Katalon TestOps. Follow the below steps to set up the integration properly:

1. Check the **Enable Katalon TestOps Integration** checkbox to retrieve all teams and projects that you have permission to access in the organization you're working on.

   > In case you want to switch to another organization, on the top right corner of the app, select you account > select **Deactivate** > activate again.

   Once Katalon Studio is **successfully connected** to Katalon TestOps, all relevant Katalon TestOps the **Teams** and **Projects** will be retrieved and displayed in the Teams and Projects drop-down menu. You can also **create a  new project** in Katalon TestOps if you're a team owner or admin, simply click the **New Project** button and enter a name for it.

2. Select a team and project to which you will upload your test results. Here you can reload this part by clicking **Fetch Projects**.

   > Starting in **Katalon Studio version 7.0**, [Katalon API Keys](/katalon-studio/docs/katalon-apikey-70) must be used for enabling Katalon TestOps in console mode.

3. Click **Apply** and then **OK** to finish your configurations.

To verify if you have overridden the authentication successfully, on the top right corner, select your account > **View Dashboard**. You should be navigated to the project having been configured above.

## Remote execution with Katalon TestOp OnPremise

### Activation

Katalon Studio support reading `apiKey` and `serverURL` from the **licenseServer.properties** file for online activation.

You have to create a **{user.home}/.katalon/licenseServer.properties** (**.katalon** is a hidden folder). The **licenseServer.properties** must contain the following properties for Katalon Studio to authenticate:

* `serverURL=https://analytics.katalon.com`
* `apiKey=xxxxxxxx`.

Go to your profile page > Select **API Key** > Copy an existing API Key for this purpose or create a new one.

For online activation, first Katalon Studio will check the `-apiKey` in the generated command; if it fails, the properties in the **licenseServer.properties** file will be read next.

### Reports Sending

In **Project > Settings > Katalon TestOps > Authentication**, the ENABLED **Override authentication** requires you to generate a command with `-apiKeyOnPremise=””` using the Command Generator to execute a project and send reports.

> Both `-apiKeyOP` and `-apiKeyOnPremise` are supported.

Go to your profile page in KTOP > Select **API Key** > Copy an existing API Key for this purpose or create a new one.

For example:

```groovy
katalonc -noSplash -runMode=console -projectPath="~\Sample.prj" -retry=0 -testSuitePath="Test Suites/Sample Test Suite" -executionProfile="default" -browserType="Chrome" -apiKey="19d******" -apiKeyOnPremise="xxxx"
```

You have to configure your project in GUI before running in Katalon Runtime Engine.

## Upload Reports

Once Katalon Studio is integrated with Katalon TestOps successfully, test results of a Test Suite/Test Suite Collection will be uploaded to Katalon TestOps automatically.

View the detailed documents of uploading test results from [Katalon Studio](https://docs.katalon.com/katalon-analytics/docs/project-management-import-KS.html) and the [command line](https://docs.katalon.com/katalon-analytics/docs/project-management-import-cli.html).

Starting in **Version 7.0**, the reports with pdf, HTML, CSV formats automatically generated by [Basic Report Plugin](https://store.katalon.com/product/59/Basic-Report) can be uploaded from Katalon Studio to Katalon TestOps. Remember to [configure your preferred report formats](https://docs.katalon.com/katalon-studio/docs/basic-report.html#features).

## Access Katalon TestOps

### View Reports

In the **Result** Tab of a Test Suite, click the **Katalon TestOps** button, then select **Access TestOps** to access the **Execution** tab. You can also view more reports in the **Reports** tab in Katalon TestOps.

### View Execution History of a specific Test Case or Test Suite

You can also view a specific Test Case or Test Suite entire execution history in Katalon TestOps by clicking the **View Execution History** button on the Test Case or Test Suite Views.  

### Create Test Plan in Katalon TestOps right from Katalon Studio

Starting in **version 7.0**, on the test suite collection view, click the **Create Test Plan** button to:

* Zip and upload the current Project code.
* Create a corresponding Test Plan on Katalon TestOps with the above Test Project.

### Store Katalon Studio's project code in Katalon TestOps

Starting in **version 7.0**, to store your Katalon Studio's Project Code in Katalon TestOps, from any screens of your project in Katalon Studio, click <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/katalon-analytics-beta-integration/upload-project-code.png" width="28" height="20.6"> icon, select the preferred Katalon TestOps team and project to store the Katalon Studio project code, then enter a Code Repo name and click **Upload**.
