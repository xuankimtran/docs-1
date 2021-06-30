---
title: "How to execute tests from command-line" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-recorder/docs/how-to-execute-tests-from-cli.html 
description: 
---

You can now execute KR tests from the command-line using Katalon Recorder Command-Line runner (KR CLI).

## Prerequisites
-   node version 8 or 10.    
-   npm.    
-   kr-cli.
    

If you are using Homebrew to manage dependencies, do the following:

```
brew install node
npm install kr-cli
```

## Using KR CLI as a tester

If you are a tester, you can integrate KR tests into the CI/CD pipeline to execute them regularly or on specific conditions without manual interventions.

### Executing a test suite

`kr-cli run <browser> <pathToHtmlFile> --report=<pathToReportFolder>`

1.  Replace pathToHtmlFile with the absolute path to your KR test suite.    
2.  Replace browser with either chrome or firefox.    
3.  Replace pathToReportFolder with the absolute path an existing folder.    
4.  Execute the command.
    

A report file with .csv extension and a log file with .log extension will be generated at the specified report folder.

### Executing a test suite with data files

`kr-cli run <browser> <pathToHtmlFile> --report=<pathToReportFolder> --data=<pathToData1>`

1.  Replace pathToHtmlFile with the absolute path to your KR test suite.    
2.  Replace browser with either chrome or firefox.    
3.  Replace pathToReportFolder with the aboluste path to an existing folder.    
4.  Replace pathToData1 with the absolute path to your data file.    
5.  Execute the command.
    
If your test suite use multiple data files, separate the paths with a comma. A report file with .csv extension and a log file with .log extension will be generated at the specified report folder.

## Using KR CLI as a developer

If you are a developer, you can integrate KR tests into your development process to ensure that your code doesn't break important user experiences.

### Executing all test suites in a project

`kr-cli dev <browser> --lg`

1.  Place all KR test suites under folder /tests/kr-test in your NodeJS project.    
2.  Replace browser with chrome or firefox.     
3.  Execute the command.
    
When you run in development mode, by default no report or log files are going to be generated. An overview of the execution will be printed directly to your command-line tool. When --lg is specified, the logs will also be printed to your command-line tool as the tests are being executed.