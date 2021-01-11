---
title: "View BDD Test Results in Katalon TestOps"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/bdd-test-results.html
---
Starting from Katalon Studio 7.8, if a BDD-enabled Katalon Studio project is integrated with **Katalon TestOps**, you can see native BDD Test Results with Features and Scenarios instead of Test Cases.

## Prerequisites

- You have enabled **Katalon TestOps** integration with **Katalon Studio**. [Learn more](https://docs.katalon.com/katalon-studio/docs/katalon-analytics-beta-integration.html#settings)
- You have a BDD project in **Katalon Studio**. [Learn more](https://docs.katalon.com/katalon-studio/docs/cucumber-features-file.html)


## Upload and view BDD Test Results

### Configure BDD Settings 

In your project, go to *Project Settings* by clicking the gear icon on the top right corner > in the *Configurations* tab, check an *"Enable BDD reports"* box.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/bdd-test-results/configure-bdd-settings.png" width="" height="">


### View BDD Test Results in Katalon TestOps

After you have configure BDD Settings, **Katalon TestOps** will recognize and process BDD-based Test Execution Results. There will be icons next to those BDD Test Results.

To view BDD Test Results, in your project, go to *Test Management* > *Requirements*.

Features of your BDD tests will be displayed as Requirements, whereas Scenarios will be displayed as Test Cases.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/bdd-test-results/bdd-features.png" width="" height="">

Scenario content is also shown on *Test Run* page. This will help you capture the logic of each Test Case easily.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/bdd-test-results/bdd-scenarios.png" width="" height="">

### View BDD Test Results in the Traceability Matrix

BDD Test Results can also be displayed in the Traceability Matrix for you to better manage the relationship across Requirements (BDD Features), Test Cases (BDD Scenarios), Defects.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/bdd-test-results/bdd-traceability.png" width="" height="">

