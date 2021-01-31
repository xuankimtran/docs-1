---
title: "Upload JUnit and Katalon Studio Test Results to Katalon TestOps using Katalon Report Uploader" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/project-management-import-cli.html 
redirect_from:
    - "/display/KA/From+Command+Line/"
    - "/display/KA/From%20Command%20Line/"
    - "/x/FhbR/"
    - "/katalon-analytics/docs/project-management-import-cli/"
description: How to import test results using CLI
---

Katalon Report Uploader is a utility to upload reports to Katalon TestOps. At this moment it supports JUnit, Katalon Studio, and Katalon Recorder report format. It can be used with CLI, Docker, Github Action, and other cloud CIs.

## Usage for CLI

1. Download [Reports Uploader](https://github.com/katalon-studio/report-uploader/releases) and install [Java JRE](https://www.java.com/en/download/manual.jsp) and [Java JDK](https://www.oracle.com/technetwork/java/javase/downloads/index.html).

2. Get the path to your Katalon Report folders, e.g. `C:\Users\alex\Katalon Studio\Web Sample\Reports\Test Suite\20190523_143946`.

3. Start Command Prompt and use the following command to upload Katalon Report:

```
java -jar katalon-report-uploader-0.0.5.jar --projectId=3 --path="d:\katalon-reports" --email=admin@mail.me --password=admin --type=katalon
```
* `projectId`: Your project ID in Katalon TestOps.
* `path`: The local path of Katalon Studio Reports folder identified in step 2.
* `email`: The email registered for your Katalon account. **If an API Key is used as `password`, this field is not required**.
* `password`: The password used for signing in Katalon TestOps or an API Key of that account. Using API Key is recommended as it will not expose your password.
* `type`: One of the values "katalon", "junit", or "katalon_recorder".
* `server`: (**Optional**) The Katalon TestOps server endpoint, by default it is `https://analytics.katalon.com`.

## Usage for Docker

### Environment variables

`SERVER`
The URL of Katalon TestOps. Default `https://analytics.katalon.com`.

`EMAIL`
The email registered for your Katalon account.

`PASSWORD`
The password used for signing in Katalon TestOps or an API Key.

`PROJECT_ID`
Your project ID in Katalon TestOps.

`TYPE`
One of the values including "katalon", "junit", or "katalon_recorder".

`REPORT_PATH`
The path of the report folder. The physical report folder should be mounted as a Docker volume first.

### Example

```
docker run -t --rm -v c:\users\alex\data\report-uploader\junit-report-sample:/katalon/report -e PASSWORD=<KATALON_API_KEY> -e PROJECT_ID=72642 -e TYPE=junit -e REPORT_PATH=/katalon/report katalonstudio/report-uploader:0.0.7.11
```

## Usage for Continuous Integration (CI) systems

### Jenkins Pipeline

Example: https://github.com/katalon-studio-samples/report-uploader-sample/blob/master/Jenkinsfile

### Github Action

Marketplace Listing: https://github.com/marketplace/actions/katalon-report-uploader.

Example:

```yaml
  - name: Katalon Report Uploader
    uses: katalon-studio/report-uploader@v0.0.7.11
    env:
      PASSWORD: ${{ secrets.KATALON_API_KEY }}
      PROJECT_ID: 50236
      TYPE: junit
      REPORT_PATH: ${{ github.workspace }}/junit-report-sample
```

### CircleCI

Example: https://github.com/katalon-studio-samples/report-uploader-sample/blob/master/.circleci/config.yml.

### Gitlab CI

Example: https://github.com/katalon-studio-samples/report-uploader-sample/blob/master/.gitlab-ci.yml.

### AWS Codebuild

Example: https://github.com/katalon-studio-samples/report-uploader-sample/blob/master/buildspec.yml.

### Azure DevOps Pipelines

Example: https://github.com/katalon-studio-samples/report-uploader-sample/blob/master/azure-pipelines.yml.
