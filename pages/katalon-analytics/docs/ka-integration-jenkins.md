---
title: "Integration with Jenkins" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/ka-integration-jenkins.html 
description: How to integrate KT with Jenkins to execute TestOps Grid Plan
---
**Prerequisites:**
* Download and install [Jenkins](https://jenkins.io/download/)
* Start Jenkins (command : java -jar jenkins.war)
* Download and activate [Katalon Runtime Engine](https://www.katalon.com/download/) for your machine
* Install Katalon Studio plugin for Jenkins: Go to Manage Jenkins > Manage Plugins > Available tab and find Katalon plugin on the list. Select and click Install.

## Configuration in Katalon TestOps

You have to define a Grid Plan on TestOps before you can assign the Plan to Jenkins to run the job.

You can follow this [document](https://docs.katalon.com/katalon-analytics/docs/grid-local-agents.html) on how to set up Grid Plan on Local Agent.

## Configuration in Jenkins

1. Go to Jenkins Dashboard.

2. Click **New Item** to define a new **Freestyle Project** then clic OK.

![](https://github.com/katalon-studio/docs-images/blob/master/katalon-analytics/docs/jenkins-ka-integration/1-Create-New-Item-Project.JPG)


3. Select **Execute Katalon TestOps Plan** under **Build** section.

![](https://github.com/katalon-studio/docs-images/blob/master/katalon-analytics/docs/jenkins-ka-integration/2-Execute-TestOps_Plan.png)

4. Enter Server URL for Katalon TestOps.

5. Select your existing credential to retrive target Project and Test Plan. If you don't have credential, you can click **Add Jenkins Credentials** button and select **Secrete Text** option in **Kind** dropdown.

> Note: You can click Test Connection to see if you can connect to TestOps successfully.

![](https://github.com/katalon-studio/docs-images/blob/master/katalon-analytics/docs/jenkins-ka-integration/3-Define-Build-Step.JPG)

6. Click Save to go back to Jenkins project detail.

7. From here, you can click **Build Now** and let Jenkins run the job.
