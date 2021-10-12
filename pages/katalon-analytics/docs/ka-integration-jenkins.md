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

2. Select **Manage Jenkins** on the left sidebar.

   The **Manage Jenkins** page appears as below.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-oct-jenkins-integration/jk-manage-jenkins.png"  width=100% alt="manage jenkins page">

3. Click **Manage Plugins**.

   The **Plugin Manager** page appears as below.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-oct-jenkins-integration/jk-manage-jenkins-available.png" width=100% alt="jenkins plugin page">
   
4. Click on the **Available** tab.

5. Search for the Katalon plugin.

   You will find **Katalon TestOps**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-oct-jenkins-integration/jk-manage-jenkins-search-testops-plugin.png" width=100% alt="jenkins search katalon plugin">
   
6. Select this Katalon plugin, then choose between **Install without restart** and **Download now and install after restart** to install it.

You have installed the Katalon plugin on Jenkins.

## Configure Test Runs in Katalon TestOps

You must schedule test runs in Katalon TestOps before assigning this schedule to Jenkins for test executions. See: [Schedule Test Runs](https://docs.katalon.com/katalon-analytics/docs/create-plan.html).

> Notes:
>
> Choose the **Save Configurations** option in the **Schedule Test Run** dialog to schedule Test Runs for Jenkins.

## Integrate Katalon TestOps with Jenkins

1. Sign in to Jenkins.

   The Jenkins's **Dashboard** page appears.
   
2. Select **New Item** on the left sidebar.

   The page appears as below.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-oct-jenkins-integration/jk-s1-create-free-style-project.png" width=100% alt="jenkins new item page">
   
3. Select **Freestyle project**, then enter a name for your project.

4. Click **OK**.

   You will be navigated to your project's page as below.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-oct-jenkins-integration/jk-s2-create-build.png"  width=100% alt="jenkins create project">

4. Click on the **Build** tab.

   You will be navigated to the **Build** section.

5. Click **Add build step**, then select **Execute Katalon TestOps Plan** from the dropdown menu.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-oct-jenkins-integration/jk-build-execute-kto-plan.png"  width=100% alt="jenkins build">

   The new **Execute Katalon TestOps Plan** dialog will appear under **Build**.
   
6. Fill in the required information.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-oct-jenkins-integration/jenkins-credentials-highlight.png" width=100% alt="jenkins build">

   * In the **Server URL** section, enter `https://testops.katalon.io`.

   * In the **Credentials** section, click **Add** > **Jenkins** to add a new credential.
   
      The **Add Credentials** dialog appears as below.

       <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/jenkins-ka-integration/secret-text.png" width="" height="" alt="jenkins add credentials">

      * In the **Kind** section, select **Secret Text** from the dropdown list.
      * In the **Secret** section, enter a Katalon TestOps API Key. See: [API Keys](https://docs.katalon.com/katalon-analytics/docs/ka-api-key.html).
      * In the **ID** section, give a name for the new credential (e.g., **katalon-api-key-test**).
      * Click **Add** to finish.

         You have added a new credential.
      
         You will be automatically navigated back to the **Credentials** section, where you can select the newly-added credential in the **- none -** box.

8. Click **Test Connection** for Jenkins to retrieve Projects and Test Runs from Katalon TestOps.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-oct-jenkins-integration/jenkins-project-plans-retrieval.png" width="" height="" alt="jenkins add credentials">

   > Notes:
   >
   > If the test connection is successful, you will see *Success!* on the screen (highlighted in the image above).

9. Select your Project and the schedule you have created earlier. See: [Configure Test Runs in Katalon TestOps](https://docs.katalon.com/katalon-analytics/docs/ka-integration-jenkins.html#configuration-a-test-plan-in-Katalon-TestOps).

10. Click **Save**.

    You will be navigated back to the Jenkins's **Dashboard** page.

11. Select **Build Now** on the left sidebar to run the job.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-oct-jenkins-integration/jk-build-now.png" width="" height="" alt="jenkins add credentials">
