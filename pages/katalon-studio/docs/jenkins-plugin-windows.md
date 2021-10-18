---
title: "Jenkins Intergation on Window/MacOS"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/jenkins-plugin-windows.html 
description: 
---

This tutorial shows you how to execute Katalon Studio tests in Jenkins on Window and MacOS with: 

-  The **Katalon TestOps** plugin for Jenkins
-  Jenkins Pipeline script
-  Jenkins Pipeline (Jenkinsfile) with Docker

> Requirements:
> * An active Katalon Runtime Engine license. To learn more about activating Katalon Runtime Engine license, you can refer to this document: [Activate Katalon License](https://docs.katalon.com/katalon-studio/docs/activate-license.html#activate-trial-license).
> * In case you use Katalon Studio Docker Image, you need an active Katalon Runtime Engine floating license. To learn more about types of licenses, you can refer to this document: [Types of license](https://docs.katalon.com/katalon-studio/docs/license.html).
## Installation

Install Jenkins. Follow the instructions in the following Jenkins documents:
   - For Windows: [Windows](https://www.jenkins.io/doc/book/installing/windows/)
   - For MacOS: [MacOS](https://www.jenkins.io/doc/book/installing/macos/) 

## Execute Katalon Studio tests in Jenkins with the Katalon TestOps plugin
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

## Execute Katalon Studio with Jenkins Pipeline (Jenkinsfile)

Jenkins Pipeline (Jenkinsfile) provides an extensible set of tools for modeling simple-to-complex delivery pipelines "as code". To learn more about creating a Jenkinsfile, you can refer to this Jenkins document: [Using a Jenkinsfile](https://www.jenkins.io/doc/book/pipeline/jenkinsfile/).
### Install Katalon Runtime Engine

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

<details><summary>For MacOS/Linux</summary>

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

> You can find more command line options at [Command Syntax](https://docs.katalon.com/katalon-studio/docs/jenkins-docker-ubuntu.html#build-your-project).

4. After the configuration, click **Save**, then click **Build Now** to run the project.
## Run Jenkins Pipeline (Jenkinsfile) with Katalon Studio Docker Image

Your Katalon Project is run with Katalon Studio Docker Image; hence pre-installed Katalon Studio and Katalon Runtime Engine in your local machine are not required. Docker Image for Katalon Studio is available here at Docker Hub: [katalonstudio/katalon](https://hub.docker.com/r/katalonstudio/katalon/).
### Install Docker and plugins

1. Download and install Docker. Follow the instructions in the Docker document here: [Get Docker](https://docs.docker.com/get-docker/). 
   
2. Install the **Docker** plugin and **Docker Pipeline** plugin. Go to **Manage Jenkins > Manage Plugins > Available tab** and search for the **Docker** plugin and **Docker Pipeline** plugin. 
2. Select the plugin and click **Install without restart**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-docker/plugins.png" alt="plugins" width=70%>

### Add an environment path

<details><summary>For Window</summary>

This step is not required for Window users, you can now skip to [Upload your project](https://docs.katalon.com/katalon-studio/docs/jenkins-plugin-windows.html/#upload-your-project)

</details>

<details><summary>For MacOS/Linux</summary>

When running jobs with Docker from a Jenkinsfile with Pipeline syntax, you need to add an environment path to Jenkins. This `PATH` helps Jenkins point to the correct Docker installation path. Do as follows:

1. To find the correct Docker installation path, open **Terminal**, copy and paste the following command line: `which docker`. The result tells you where the Docker is.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-plugin-windows/KS-JENKINS-Docker%20installation%20path.png" alt="Docker installation path" width=70%>

2. Go to **Dashboard > Manage Jenkins > Configure System > Global properties**. Select the **Environment variables** to add a global variable named `PathExtra` with this value: `$PATH:<the correct Docker installation path>`

    <img src="https://github.com/katalon-studio/docs-images/blob/master/katalon-studio/docs/jenkins-plugin-windows/KS-JENKINS-add%20env-path-to-jenkins.png" alt="Add environment path to Jenkins pipline" width=70%>


</details>

### Upload your project

> Notes: 
> Make sure you have Docker open, with **Docker Plugin** and **Docker Pipeline** activated on Jenkins.

1. In the Jenkins Dashboard, go to **New Item** and create a **Jenkins Pipeline** project.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-plugin-windows/create-pipeline.png" width=70%>

2. In the **Definition** dropdown list, you can either choose **Pipeline Script** or **Pipeline Script from SCM** depending on where you store the Pipeline project. The **Pipeline Script from SCM** instructs Jenkins to obtain your Pipeline from Source Control Management (SCM), which will be your locally cloned Git repository. To learn more about defining a Pipeline, you can refer to this Jenkins document: [Getting started with Pipeline](https://www.jenkins.io/doc/book/pipeline/getting-started/#defining-a-pipeline-in-scm).

Here, since we have our Pipeline project stored in Git, we select **Pipeline Script from SCM**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-plugin-windows/git.png" width="70%" alt="Choose Pipeline Script from SCM">

3. In the **SCM** field, select **Git**. Enter your repository URL, select branches to build, repository browser, and additional behaviours, if any. You can clone the following sample project here: [CI samples](https://github.com/katalon-studio-samples/ci-samples).

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-plugin-windows/KS-JENKINS-Add-Git-url-in-pipline-from-SCM.png" width="70%" alt="Enter Git repository url">

4. Specify the Jenkinsfile path from your Git project in the **Script Path** box.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-plugin-windows/KS-JENKINS-Add-Jenkinspath.png" width="70%" alt="Jenkinsfile path">

   > Notes:
   > To quickly copy the Jenkinsfile path in your Git project, go to your Jenkinsfile, click *More* (...), then click **Copy Path**. 
   > <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-plugin-windows/KS-JENKINS-Quickly-go-to-Jenkins-file-in-Git.png" width="70%" alt="Quickly Jenkinsfile path in Git project">

    You can see our sample Jenkinsfile for MacOS/Linux here: [Jenkinsfile](https://github.com/katalon-studio-samples/ci-samples/blob/master/Jenkinsfile). In case you are using Window, replace the `sh` command in this sample Jenkinsfile with the `bat` command: 

    ``` groovy
    steps {
    bat '''
    '''
    }
    ```

    > Notes: 
    > Make sure to add your API key to verify your credentials. The command-line options of API Key, including `-apiKey=<Your_API_Key>` and `-apikey=<Your_API_Key>` are both accepted. To learn more about API keys, you can refer to this document: [API key](https://docs.katalon.com/katalon-analytics/docs/ka-api-key.html#katalon-api-keys-usage).


5. Enter your Git credentials. 

   > Notes:
   > * To add credentials to Jenkins, you need the **Credentials** plugin, which is usually installed in the Jenkins installation. To check whether you have installed the plugin, go to **Dashboards > Manage Jenkins > Manage plugins**, then find the **Credentials** plugin. You can refer to this Jenkins document: [Using credentials](https://www.jenkins.io/doc/book/using/using-credentials/) for further information about managing credentials in Jenkins.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-plugin-windows/KS-JENKINS-Choose-creadentials.png" width="70%" alt="Quickly Jenkinsfile path in Git project">

6.  Click **Save** then click **Build Now** to run the Jenkinsfile. 
    When the test is being run, you can also view the console log in Docker.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-docker/docker-log.png" alt="docker log" width=100%>

## See also

* [Jenkins Intergration on Ubuntu](https://docs.katalon.com/katalon-studio/docs/jenkins-plugin-ubuntu.html).
* [Integrate Jenkins on Docker hosted in Ubuntu](https://docs.katalon.com/katalon-studio/docs/jenkins-docker-ubuntu.html#install-plugins)