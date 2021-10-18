---
title: "Execute Katalon Studio tests with Jenkins Pipeline Script (Jenkinsfile)"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/execute-katalon-tests-with-jenkins-pipeline-script.html 
description: 
redirect from: 
---

Jenkins Pipeline (Jenkinsfile) provides an extensible set of tools for modeling simple-to-complex delivery pipelines. To learn more about creating a Jenkinsfile, you can refer to this Jenkins document: [Using a Jenkinsfile](https://www.jenkins.io/doc/book/pipeline/jenkinsfile/).

> Requirements:
> * Jenkins installed. Follow the instructions in this Jenkins document for installation: [Getting started](https://www.jenkins.io/doc/book/installing/).
> * Katalon Runtime Engine (KRE) installed. You can download Katalon Runtime Engine here: [Katalon products](https://www.katalon.com/download/).
> * An active Katalon Runtime Engine license. To learn more about activating the Katalon Runtime Engine license, you can refer to this document: [Activate Katalon License](https://docs.katalon.com/katalon-studio/docs/activate-license.html#activate-trial-license).

This tutorial shows you how to execute Katalon Studio tests in Jenkins with Jenkins Pipeline Script (Jenkinsfile). Follow these steps:


1. In the Jenkins Dashboard, go to **New Item** and create a **Jenkins Pipeline** project.
2. In the **Definition** dropdown list, select **Pipeline Script**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-plugin-windows/KS-JENKINS-Choose-pipeline-script.png" width=70% alt="Select Pipeline script">

3. Copy and paste the following command-line arguments in the **Script** box:

<details><summary>For Windows</summary>

```groovy
pipeline {
    agent any
    stages {
        stage('Test') {
            steps {
                bat '''
                cd  <KRE installed folder>
                katalonc  -projectPath="<projectpath>" -browserType="<browser>" -retry=<number of retry times> -statusDelay=<seconds> -testSuitePath="<path>" -apiKey="<user API key>" -orgID=<Katalon_OrgID>
                '''
                
            }
            
        }
        
    }
    
}

```
For example:

```groovy

pipeline {
    agent any
    stages {
        stage('Test') {
            steps {
                bat '''
                cd  C:\Users\NAH\Desktop\Katalon_Studio_Engine_Windows_64-8.1.0
                katalonc  -projectPath="C:\Users\NAH\Desktop\ci-samples-master\test.prj" -browserType="Chrome" -retry=0 -statusDelay=15 -testSuitePath="Test Suites/TS_RegressionTest" -apiKey="<user API key>" -orgID=<Katalon_OrgID>
                '''
                
            }
            
        }
        
    }
    
}
```

</details>

<details><summary>For macOS/Linux</summary>

```groovy
pipeline {
    agent any
    stages {
        stage('Test') {
            steps {
                sh '''
                cd  <KRE installed folder>
                ./katalonc  -projectPath="<projectpath>" -browserType="<browse" -retry=<number of retry time> -statusDelay=<seconds> -testSuitePath="<path>" -apiKey="<user API key>" -orgID=<Katalon_OrgID>
                '''
                
            }
            
        }
        
    }
    
}
```
For example: 

```groovy
pipeline {
    agent any
    stages {
        stage('Test') {
            steps {
                sh '''
                cd  /Users/yen.nguyen/Downloads/Katalon_Studio_Engine_MacOS-8.1.0/Katalon\\ Studio\\ Engine.app/Contents/MacOS
                ./katalonc  -projectPath="/Users/yen.nguyen/Downloads/ci-samples-master/test.prj" -browserType="Chrome" -retry=0 -statusDelay=15 -testSuitePath="Test Suites/TS_RegressionTest" -apiKey="<user API key>" -orgID=<Katalon_OrgID>
                '''
                
            }
            
        }
        
    }
    
}
```

</details>

> You can find more command-line options at [Command Syntax](https://docs.katalon.com/katalon-studio/docs/jenkins-docker-ubuntu.html#build-your-project).

4. After the configuration, click **Save**, then click **Build Now** to run the project.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-plugin-windows/KS-JENKINS-Build-now.png" width=60% alt="Build your Jenkins project">

5.  To view the console log, click on your current build on Jenkins and select **Console Output**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-plugin-windows/KS-JENKINS-console-output.png" width=60% alt="View console output">
## See also

* [Intergrate Jenkins Pipeline (Jenkinsfile) with Katalon Studio Docker Image](https://docs.katalon.com/katalon-studio/docs/jenkins-pipeline-docker.html)