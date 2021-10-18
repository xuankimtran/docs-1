---
title: "Intergrate Jenkins Pipeline with Katalon Studio Docker Image"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/jenkins-plugin-windows.html 
description: 
---

This tutorial shows you how to execute Katalon Studio tests in Jenkins with Jenkins Pipeline (Jenkinsfile) and Katalon Studio Docker Image.
Your Katalon Project is run with Katalon Studio Docker Image; hence pre-installed Katalon Studio and Katalon Runtime Engine in your local machine are not required. Docker Image for Katalon Studio is available here at Docker Hub: [katalonstudio/katalon](https://hub.docker.com/r/katalonstudio/katalon/).

> Requirements:
> * Jenkins installed. Follow the instructions in this Jenkins document for installation: [Getting started](https://www.jenkins.io/doc/book/installing/).
> * Docker installed. You can refer to the instructions in the Docker document here: [Get Docker](https://docs.docker.com/get-docker/). 
> * An active Katalon Runtime Engine floating license. To learn more about types of licenses, you can refer to this document: [Types of license](https://docs.katalon.com/katalon-studio/docs/license.html).


## Intergrate Jenkins with Docker

### Install plugins
   
1. Install the **Docker** plugin and **Docker Pipeline** plugin. Go to **Manage Jenkins > Manage Plugins > Available tab** and search for the **Docker** plugin and **Docker Pipeline** plugin. 
2. Select the plugin and click **Install without restart**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-docker/plugins.png" alt="plugins" width=70%>

### Add an environment path

<details><summary>For Window</summary>

This step is not required for Window users, you can now skip to [Upload your project](https://docs.katalon.com/katalon-studio/docs/jenkins-plugin-windows.html/#upload-your-project)

</details>

<details><summary>For MacOS/Linux</summary>

When running jobs with Docker from a Jenkinsfile with Pipeline syntax, you need to add an environment path to Jenkins. This `PATH` helps Jenkins point to the correct Docker installation path. Do as follows:

1. To find the correct Docker installation path, open **Terminal**, copy and paste the following command line: `which docker`. The result will tell you where the Docker is.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-plugin-windows/KS-JENKINS-Docker%20installation%20path.png" alt="Docker installation path" width=70%>

2. Go to **Dashboard > Manage Jenkins > Configure System > Global properties**. Select the **Environment variables** to add a global variable named `PathExtra` with this value: `$PATH:<the correct Docker installation path>`

    <img src="https://github.com/katalon-studio/docs-images/blob/master/katalon-studio/docs/jenkins-plugin-windows/KS-JENKINS-add%20env-path-to-jenkins.png" alt="Add environment path to Jenkins pipline" width=70%>


</details>

### Upload your project

> Notes: 
> Make sure you have Docker open, with **Docker Plugin** and **Docker Pipeline** activated on Jenkins.

1. In the Jenkins Dashboard, go to **New Item** and create a **Jenkins Pipeline** project.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-plugin-windows/create-pipeline.png" width=70%>

2. In the **Definition** dropdown list, you can either choose **Pipeline Script** or **Pipeline Script from SCM** depending on where you store your Pipeline project. The **Pipeline Script from SCM** instructs Jenkins to obtain your Pipeline from Source Control Management (SCM), which will be your locally cloned Git repository. To learn more about defining a Pipeline, you can refer to this Jenkins document: [Getting started with Pipeline](https://www.jenkins.io/doc/book/pipeline/getting-started/#defining-a-pipeline-in-scm).

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

* [Integrate Jenkins on Docker hosted in Ubuntu](https://docs.katalon.com/katalon-studio/docs/jenkins-docker-ubuntu.html#install-plugins)