---
title: "Integration with Jenkins" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/ka-integration-jenkins.html 
description: How to integrate KT with Jenkins to execute TestOps Grid Plan
---
**Prerequisites:**

* Download and install [Jenkins](https://jenkins.io/download/)
* Start Jenkins (command : `java -jar jenkins.war`)
* Download and activate [Katalon Runtime Engine](https://www.katalon.com/download/) for your machine
* Install Katalon Studio plugin for Jenkins: Go to **Manage Jenkins > Manage Plugins > Available** tab > find and select the Katalon plugin > **Install**.

## Configuration in Katalon TestOps

You have to define a Grid Plan on TestOps before assigning the Plan to Jenkins to run the job. Learn more about how to set up Grid Plan on Local Agent in this [document](https://docs.katalon.com/katalon-analytics/docs/grid-local-agents.html).

## Configuration in Jenkins

1. Go to Jenkins Dashboard.
2. Click **New Item** > create a **Freestyle Project** > click **OK**.
   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/jenkins-ka-integration/1-Create-New-Item-Project.JPG)

3. Select **Execute Katalon TestOps Plan** under the **Build** section.
   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/jenkins-ka-integration/2-Execute-TestOps_Plan.png)

4. Enter **Server URL** of Katalon TestOps.
5. Select one of the existing credentials to connect to TestOps. Or you can add new ones by selecting **Add**. In the **Add Credentials** dialog, enter required information and click **Add**. Please remember to select **Secret Text** in the **Kind** dropdown.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/jenkins-ka-integration/secret-text.png" width="" height="">

6. Click **Test Connection** to retrieve Projects and Test Plans.

   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/jenkins-ka-integration/3-Define-Build-Step.JPG)

7. Click **Save** to go back to the Jenkins project's details.
8. Click **Build Now** to run the job.
