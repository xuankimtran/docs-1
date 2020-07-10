---
title: "Katalon Studio Github Action" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/katalon-studio-github-action.html
---
> Katalon TestOps CI is an easier way to execute Katalon Studio tests remotely or schedule remote Katalon Studio execution. [Learn more](https://docs.katalon.com/katalon-analytics/docs/kt-remote-execution.html)

Actions on GitHub is a new way to automate your development workflow. Katalon Studio Github Action that is available on Marketplace, allows you to automate Katalon Studio projects execution. [Access it here!](https://github.com/marketplace/actions/katalon-studio)

**Prerequisites**

* An active Katalon Runtiem Engine license
* Katalon Studio version 7.0 and later
* Set up [Katalon API Keys](https://docs.katalon.com/katalon-analytics/docs/ka-api-key.html#katalon-api-keys-usage) using [GitHub Encrypted Secret](https://docs.github.com/en/actions/configuring-and-managing-workflows/creating-and-storing-encrypted-secrets) named `API_KEY`

## Variables

```java
name: 'Katalon-Studio'
description: 'Execute Katalon Studio projects'
inputs:
      version:
            description: 'Which version of Katalon Studio to run'
            required: true
            default: ''
            
      projectPath:
            description: 'Where the Katalon Studio project is checked out'
            required: true
            default: ''
            
      args:
            description: 'What arguments to run Katalon Studio project'
            required: true
            default: ''

runs:
      using: 'node12'
      main: 'index.js'
```

## Usage Example

```java
name: CI
on:
  push:
    branches: [ master ]
  pull_request:
    branches: [ master ]

jobs:
  build:
    runs-on: windows-latest
    steps:
    - name: Checkout
      uses: actions/checkout@v2.1
    - name: Katalon Studio Github Action
      uses: katalon-studio/katalon-studio-github-action@v2
      with:
          version: '7.5.5'
          projectPath: '${{ github.workspace }}'
          args: '-noSplash -retry=0 -testSuiteCollectionPath="Test Suites/Simple Test Suite Collection" -apiKey= ${{ secrets.API_KEY }} --config -webui.autoUpdateDrivers=true'
```

Our team provides CI Samples for macOS and Windows [here](https://github.com/katalon-studio-samples/ci-samples/tree/master/.github/workflows)
