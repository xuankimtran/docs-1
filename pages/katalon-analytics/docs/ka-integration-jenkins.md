---
title: "Integration with Jenkins" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/ka-integration-jenkins.html 
description: How to integrate Katalon TestOps with Jenkins to execute TestOps plans.
---

> Requirements:
>
> * You have downloaded and installed [Jenkins](https://jenkins.io/download/).
> * You have downloaded and installed [Katalon Runtime Engine](https://docs.katalon.com/katalon-studio/docs/install-RE.html).

## Install the Katalon plugin on Jenkins

1. Sign in to Jenkins.
   
   The Jenkins's **Dashboard** page appears.

2. Select **Manage Jenkins** on the left sidebar, then select **Manage Plugins**.

   The **Plugin Manager** page appears as below.

3. Click on the **Available** tab.

4. Search for the Katalon plugin.

   You will find the **Katalon TestOps** plugin.
5. Choose between **Install without restart** and **Download now and install after restart** to install the plugin.

## Configure a test plan in Katalon TestOps

You have to create a test plan in Katalon TestOps before assigning this plan to Jenkins for test execution. See: [Schedule Test Runs](https://docs.katalon.com/katalon-analytics/docs/create-plan.html).

> Notes:
>
> Choose the **Save Configurations** option in the **Schedule Test Run** dialog to define a test plan for Jenkins.

## Integrate Katalon TestOps with Jenkins

1. Sign in to Jenkins.

   The Jenkins's **Dashboard** page appears.
   
2. Select **New Item** on the left sidebar, then choose **Freestyle Project**.

3. Enter a name for your project, then click **OK**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/jenkins-ka-integration/1-Create-New-Item-Project.JPG"  width=100% alt="jenkins create project">

4. Click on the **Build** tab.

5. Choose **Execute Katalon TestOps Plan**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/jenkins-ka-integration/2-Execute-TestOps_Plan.png"  width=100% alt="jenkins build">

6. In the **Server URL** section, enter `https://testops.katalon.io`.

7. Select one of the existing credentials OR add new credentials as follows:

   * Click **Add**.

      The **Add Credentials** dialog appears.

       <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/jenkins-ka-integration/secret-text.png" width="" height="" alt="jenkins testops integration">

      * In the **Kind** dropdown list, select **Secret Text**.
      * In the **Secret** section, enter a Katalon TestOps API Key. See: [API Keys](https://docs.katalon.com/katalon-analytics/docs/ka-api-key.html).
      * In the **ID** section, give a name for the credential (e.g., **katalon-api-key-test**).
      * Click **Add**.

          <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/jenkins-ka-integration/secret-text.png" width="" height="" alt="jenkins add credentials">

8. Click **Test Connection** for Jenkins to retrieve Projects and Test Plans from Katalon TestOps.

9. Select your Project and the Test Plan you have created earlier. See: [Configure a test plan in Katalon TestOps](https://docs.katalon.com/katalon-analytics/docs/ka-integration-jenkins.html#configuration-a-test-plan-in-Katalon-TestOps).

10. Click **Save**.

   You will be navigated back to the Jenkins's **Dashboard** page.

11. Select **Build Now** on the left sidebar to run the job.
