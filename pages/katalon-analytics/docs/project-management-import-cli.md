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

Katalon Report Uploader is a utility to upload reports to Katalon TestOps. At this moment it supports JUnit, Katalon Studio, and Katalon Recorder report format. It can be used with CLI, Docker, and Github Action.

## CLI usage

1. Download [Reports Uploader](https://github.com/katalon-studio/report-uploader/releases) and install [Java JRE](https://www.java.com/en/download/manual.jsp) and [Java JDK](https://www.oracle.com/technetwork/java/javase/downloads/index.html).

2. Get the path to your Katalon Report folders, e.g. `C:\Users\alex\Katalon Studio\Web Sample\Reports\Test Suite\20190523_143946`.

3. Start Command Prompt and use the following command to upload Katalon Report:

```
java -jar katalon-report-uploader-0.0.5.jar --projectId=3 --path="d:\katalon-reports" --email=admin@mail.me --password=admin --type=katalon
```
* `projectId`: your project ID in Katalon Analytics.
* `path`: a local path of Katalon Studio Reports folder identified in step 2.
* `email`: the email registered for your Katalon account.
* `password`: the password used for signing in Katalon Analytics or an API Key.
* `type`: one of the values including "katalon", "JUnit", or "katalon_recorder".

## Docker usage

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

### Examples

```
docker run -t --rm -v c:\users\alex\data\report-uploader\junit-report-sample:/katalon/report -e PASSWORD=<KATALON_API_KEY> -e PROJECT_ID=72642 -e TYPE=junit -e REPORT_PATH=/katalon/report katalonstudio/report-uploader:0.0.7.11
```

## Github Action usage

Marketplace Listing: https://github.com/marketplace/actions/katalon-report-uploader.

### Environment variables

Inputs can also be provided as environment variables.

`SERVER`
The URL of Katalon TestOps. Default `https://analytics.katalon.com`.

`EMAIL`
The email registered for your Katalon account. Not required if API Key is used instead of password.

`PASSWORD`
The password used for signing in Katalon TestOps or an API Key.

`PROJECT_ID`
Your project ID in Katalon TestOps.

`TYPE`
One of the values including "katalon", "junit", or "katalon_recorder".

`REPORT_PATH`
The path of the report folder.

### Examples

```yaml
  - name: Katalon Report Uploader
    uses: katalon-studio/report-uploader@v0.0.7.11
    env:
      PASSWORD: ${{ secrets.KATALON_API_KEY }}
      PROJECT_ID: 50236
      TYPE: junit
      REPORT_PATH: ${{ github.workspace }}/junit-report-sample
```
