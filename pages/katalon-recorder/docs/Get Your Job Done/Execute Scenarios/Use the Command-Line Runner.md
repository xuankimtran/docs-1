---
title: "Use the Commande-Line Runner"
sidebar: katalon_studio_docs_sidebar
permalink: url: /katalon-recorder/docs/command-line-runner.html 
redirect_from:
description:
---
You can now execute tests in Katalon Recorder directly from the command line using the *Command-Line runner* (KR CLI)

>Prerequisites:
>
>* ``node`` version ``8`` or ``10``.
>* ``npm``.
>* ``kr-cli``.

If you are using Homebrew to manage dependencies, run the following script:

> `1brew install node 2npm install -g kr-cli`

## Using KR CLI as a tester

If you are a tester, you can integrate KR tests into the CI/CD pipeline to execute them at specific time intervals, or by defining custom triggers.

### Executing a test suite

1. Copy the following command:

> `kr-cli run <browser> <pathToHtmlFile> --report=<pathToReportFolder>`

2. Replace:

* `pathToHtmlFile` with the absolute path to your KR test suite.

* `browser` with either chrome or firefox.

* `pathToReportFolder` with the absolute path to an existing folder

3. Execute the command.

After executing the command, a report file with a .csv extension and a log file with a .log extension will be generated at the specified report folder.

### Executing a test suite with data files

1. Copy the following command:

>`kr-cli run <browser> <pathToHtmlFile> --report=<pathToReportFolder> --data=<pathToData1>`

2. Replace:

* `pathToHtmlFile` with the absolute path to your KR test suite.

* `browser` with either chrome or firefox.

* `pathToReportFolder` with the aboluste path to an existing folder.

*  `pathToData1` with the absolute path to your data file.

3. Execute the command.

If your test suite uses multiple data files, separate the paths with a comma.

A report file with a .csv extension and a log file with a .log extension will be generated at the specified report folder.

## Using KR CLI as a developer

If you are a developer, you can integrate KR tests into your development process to ensure that your code doesn't break important user experiences.

### Executing all test suites in a project

1. Place all KR test suites under folder /tests/kr-test in your NodeJS project.

2. Copy the following command:

> `kr-cli dev <browser> --lg`

3. Replace browser with chrome or firefox.

3. Execute the command.

>Notes: By default, no report or log files are generated when running commands in development mode. Instead, An overview of test execution will be printed directly to your command line tool.
>
>Specify --lg to print the logs to your command line tool during test execution.