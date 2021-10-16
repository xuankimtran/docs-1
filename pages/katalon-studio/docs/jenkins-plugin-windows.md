---
title: "Jenkins Intergation on Window/MacOS"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/jenkins-plugin-windows.html 
description: 
---

This tutorial shows you how to execute Katalon Studio Tests in Jenkins on Window and MacOS with: 

-  The **Katalon TestOps** plugin for Jenkins
-  Jenkins pipeline script
-  Jenkins Pipeline (Jenkinsfile) with Docker Image

> Requirements:
> * An active Katalon Runtime Engine license. To learn more about activating Katalon Runtime Engine license, you can refer to this document: [Activate Katalon License](https://docs.katalon.com/katalon-studio/docs/activate-license.html#activate-trial-license).
> * In case you use Katalon Docker Image, you need an active Katalon Runtime Engine floating license. To learn more about types of licenses, you can refer to this document: [Types of license](https://docs.katalon.com/katalon-studio/docs/license.html).
## Installation

Install Jenkins. Follow the instructions in the following Jenkins documents:
   - For Windows: [Windows](https://www.jenkins.io/doc/book/installing/windows/)
   - For MacOS: [MacOS](https://www.jenkins.io/doc/book/installing/macos/) 

## Execute Katalon Studio Tests with the Katalon TestOps plugin
### Install the Katalon TestOps plugin

1. Install the **Katalon TestOps** plugin. Go to **Manage Jenkins > Manage Plugins > Available tab** and search for the **Katalon TestOps** plugin.

2. Select the plugin and click **Install without restart**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-plugin-windows/KS-JENKINS-Download-Katalon-Testops-plugin.png" width=70% alt="Install Katalon TestOps plugin">
### Upload your Katalon project on Jenkins

After installing the **Katalon TestOps** plugin, you can now start Katalon Studio test in Jenkins. 

1. In the Jenkins Dashboard, go to **New Item** and create a **Freestyle project**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-plugin-windows/KS-JENKINS-Create-a-freestyle-project.png" width=70% alt="Create a new Freestyle project">

2. To upload your Katalon project on Jenkins, you can either upload your Katalon project from a Git repository or your local workspace. Here, we use a Git repository. 

   - In the **Source Code Management** section, choose **Git**.
   - Enter your repository URL, then select branches to build, repository browser, and additional behaviours, if any.

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-plugin-windows/Picture4.png" width=70% alt="Upload Katalon project">
### Build your project

1. In the **Build** section, click **Add build step** and choose **Execute Katalon Studio Tests**. The **Execute Katalon Studio Tests** box opens, asking you to input Katalon Runtime Engine version and command arguments.
   
2. Specify the Katalon Studio version you wish to execute with:

   - If you haven't downloaded Katalon Runtime Engine (KRE), you can input the KRE version you wish to execute with in the **Download Katalon Studio version** box. KRE will be downloaded and deployed automatically. You can retrieve the list of all releases on Github repository: [Releases](https://github.com/katalon-studio/katalon-studio/releases).
   - If you want to use a pre-installed version, manually input the KRE version you have installed in the **Use pre-installed Katalon Studio** box with the following command line: ```<KRE stored folder>-<KRE pre-installed version>```. For example: ```/Users/yen.nguyen/Downloads/Katalon_Studio_Engine_MacOS-8.1.0```.
   
3. Input your command in the **Command arguments** box, for example:

   ``` groovy

   -browserType="Chrome" -retry=0 -statusDelay=15 -testSuitePath="Test Suites/TS_RegressionTest" -apikey=<YOUR_API_KEY>

   ```
   > Notices:
   >
   > When you use the **Katalon TestOps** plugin, you do not need to mention ```-noSplash``` and ```-runMode=console```.

   > Notes:
   > * From version 7.7.0 onwards, if you belong to more than one Organization subscribing to Runtime Engine licenses, you can choose which Organization validates your license usage with the following command line: `-orgID=<Katalon_OrgID>`.
   > * Make sure your current browser version is compatible with the KRE Webdriver version. To learn more about upgrading or downgrading Webdrivers, you can refer to this document: [Update or Downgrade WebDrivers](https://docs.katalon.com/katalon-studio/docs/update-or-downgrade-webdrivers.html#replace-a-webdriver).

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-plugin-windows/KS-JENKINS-Enter-command-line-in-freestyles-project.png" width=60% alt="Input command arguments">

4. After you are done with the configuration, click **Save**, then click **Build Now** to run the project.
   
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-plugin-windows/KS-JENKINS-Build-now.png" width=60% alt="Build your Jenkins project">

5. To view the console log, click on your current build on Jenkins and select **Console Output**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-plugin-windows/KS-JENKINS-console-output.png" width=60% alt="View console output">
### Troubleshoot empty videos recorded after running tests on Window

If you encounter an issue of having empty videos recorded after running your tests in Jenkins on Window, it is because the WebDriver hasn't launched during test execution. To fix this issue, please uninstall Jenkins of Windows services, and replace it by a DOS batch file containing the following codes:

```groovy
cd D:\Tools\Jenkins //path to Jenkins folder
java -jar --webroot=jenkins.war
```

_Credit to Sébastien Taniere and his [original topic](https://forum.katalon.com/t/video-is-empty-when-scenario-is-launched-by-katalon-runtime-trough-jenkins-windows-instance/43974)._

## Execute Katalon Studio Tests with Jenkins Pipeline (Jenkinsfile)

Jenkins Pipeline (Jenkinsfile) provides an extensible set of tools for modeling simple-to-complex delivery pipelines "as code". To learn more about creating a Jenkinsfile, you can refer to this Jenkins document: [Using a Jenkinsfile](https://www.jenkins.io/doc/book/pipeline/jenkinsfile/).
### Installation

Download and install Katalon Runtime Engine (KRE). You can download Katalon Runtime Engine here: [Katalon products](https://www.katalon.com/download/).
### Build your project

1. In the Jenkins Dashboard, go to **New Item** and create a **Jenkins Pipeline** project.
2. In the **Definition** dropdown list, select **Pipeline Script**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-plugin-windows/KS-JENKINS-Choose-pipeline-script.png" width=70% alt="Select Pipeline script">

3. Copy and paste the following command-line argurements in the **Script** box:

<details><summary>For Windows</summary>

```groovy
pipeline {
    agent any
    stages {
        stage('Test') {
            steps {
                bat '''
                cd  <KRE installed folder>
                katalonc  -projectPath="<projectpath>" -browserType="<browser>" -retry=<number of retry times> 
                -statusDelay=<seconds> -testSuitePath="<path>" -apiKey="<user API key>" -orgID=<Katalon_OrgID>
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
                katalonc  -projectPath="C:\Users\NAH\Desktop\ci-samples-master\test.prj" -browserType="Chrome" -retry=0 
                -statusDelay=15 -testSuitePath="Test Suites/TS_RegressionTest" -apiKey="<user API key>" -orgID=<Katalon_OrgID>
                '''
                
            }
            
        }
        
    }
    
}
```

</details>

<details><summary>For MacOS/Linux</summary>

```groovy
pipeline {
    agent any
    stages {
        stage('Test') {
            steps {
                sh '''
                cd  <KRE installed folder>
                ./katalonc  -projectPath="<projectpath>" -browserType="<browse" -retry=<number of retry time> 
                -statusDelay=<seconds> -testSuitePath="<path>" -apiKey="<user API key>" -orgID=<Katalon_OrgID>
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
                ./katalonc  -projectPath="/Users/yen.nguyen/Downloads/ci-samples-master/test.prj" -browserType="Chrome" -retry=0 
                -statusDelay=15 -testSuitePath="Test Suites/TS_RegressionTest" -apiKey="<user API key>" -orgID=<Katalon_OrgID>
                '''
                
            }
            
        }
        
    }
    
}
```

</details>

> You can find more command line options at [Command Syntax](https://docs.katalon.com/katalon-studio/docs/jenkins-docker-ubuntu.html#build-your-project).

4. After the configuration, click **Save**, then click **Build Now** to run the project.
## Run Jenkins Pipeline (Jenkinsfile) with Katalon Docker Image
### Installation

1. Download and install Docker. Follow the instructions in the Docker document here: [Get Docker](https://docs.docker.com/get-docker/). 

2. Pull Katalon Studio Docker Image. This image contains up-to-date browsers including Google Chrome, Mozilla Firefox, and Katalon Studio. Docker Image for Katalon Studio is available here: [katalonstudio/katalon](https://hub.docker.com/r/katalonstudio/katalon/).

3. Install the **Docker** plugin and **Docker Pipeline** plugin. Go to **Manage Jenkins > Manage Plugins > Available tab** and search for the **Docker** plugin and **Docker Pipeline** plugin. 
4. Select the plugin and click **Install without restart**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-docker/plugins.png" alt="plugins" width=70%>
### Upload your project

3. In the Jenkins Dashboard, go to **New Item** and create a **Jenkins Pipeline** project.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-plugin-windows/create-pipeline.png" width=70%>

4. In the **Definition** dropdown list, you can either choose **Pipeline Script** or **Pipeline Script from SCM** depending on where you store the Pipeline project. The **Pipeline Script from SCM** instructs Jenkins to obtain your Pipeline from Source Control Management (SCM), which will be your locally cloned Git repository.

Here, since we have our Pipeline project stored in Git, we select **Pipeline Script from SCM**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-plugin-windows/git.png" width="70%" alt="Choose Pipeline Script from SCM">

5. In the **SCM** field, select **Git**. Enter your repository URL, select branches to build, repository browser, and additional behaviours, if any. You can use the following sample project here: [CI samples](https://github.com/katalon-studio-samples/ci-samples).

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-plugin-windows/KS-JENKINS-Add-Git-url-in-pipline-from-SCM.png" width="70%" alt="Enter Git repository url">

6. Specify the Jenkinsfile path from your Git project in the **Script Path** box.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-plugin-windows/KS-JENKINS-Add-Jenkinspath.png" width="70%" alt="Jenkinsfile path">

   > Notes:
   > To quickly copy the Jenkinsfile path in your Git project, go to your Jenkinsfile, click *More* (...), then click **Copy Path**. 
   > <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-plugin-windows/KS-JENKINS-Quickly-go-to-Jenkins-file-in-Git.png" width="70%" alt="Quickly Jenkinsfile path in Git project">

You can see our sample Jenkinsfile for MacOS/Linux here: [Jenkinsfile](https://github.com/katalon-studio-samples/ci-samples/blob/master/Jenkinsfile). In case you are using Window, use `bat` instead: 

``` groovy
steps {
   bat '''
   '''
}
```

7. Enter your Git credentials. 

   > Notes:
   > * To add credentials to Jenkins, you need the **Credentials** plugin, which is usually installed in the Jenkins installation. To check whether you have installed the plugin, go to **Dashboards > Manage Jenkins > Manage plugins**.
   > * You can refer to this Jenkins document: [Using credentials](https://www.jenkins.io/doc/book/using/using-credentials/) for further information about managing credentials in Jenkins.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-plugin-windows/KS-JENKINS-Choose-creadentials.png" width="70%" alt="Quickly Jenkinsfile path in Git project">

8.  Click **Save** then click **Build Now** to run the Jenkinsfile. 
## See also

* [Jenkins Intergration on Ubuntu](https://docs.katalon.com/katalon-studio/docs/jenkins-plugin-ubuntu.html).
* [Integrate Jenkins on Docker hosted in Ubuntu](https://docs.katalon.com/katalon-studio/docs/jenkins-docker-ubuntu.html#install-plugins)