---
title: "What's new in v5.5?"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-recorder/docs/whats-new.html
description:
toc: true
---
**June, 2021**

In this release, we aim to help you increase the pace of your development and testing. We introduced new and streamlined execution capabilities so that you can automate more often and with less errors. We also made it possible to import your scripts from Selenium IDE, so you can preserve your existing tests while benefiting from all that Katalon Recorder has to offer.

## More robust executions with Self-healing
When you interact with an element on a website, Katalon Recorder generates multiple locators associated with that element before selecting one by default for your tests. If there are changes made to a website by the developers, or if the elements are designed in such a way that they automatically change over time, your scripts may not locate that element, causing your tests to fail. You can usually fix this by manually picking a different, more robust locator. But this process can be daunting for an automation novice, and introduces a manual component to an otherwise automated system.

With this update, we introduced a feature called Self-healing which is automatically triggered when the default locator fails. The feature will then try out other locators for the same element, and use the first one that works to complete the test execution. Afterwards, you will be offered options to seamlessly replace the failing locators with working ones.

## Execute more often with Command-Line Runner
After talking to users, we were excited to see that many people use the product on a daily basis. To help you accelerate your working cycle, we introduced the Katalon Recorder Command-Line Runner (CLR). With the CLR, you can now trigger KR tests directly without even opening the app manually.

As a tester or a team leader, the CLR opens up new and exciting possibilities to integrate tests developed in KR to your CI/CD pipeline, whether they are set up to execute at regular time intervals or with custom, conditional triggers. 

As a developer, you can use the CLR to ensure your code does not break any critical paths, before easily generating end-to-end tests with KR and running them as part of your development process. 

Overall, the CLR is a force multiplier for your testing needs, enabling you to deliver high quality software faster. 

## Migrate from Selenium IDE
Selenium IDE is a very popular record and playback tool for authoring functional tests without the need to learn a test scripting language. Despite its popularity, there are good reasons to switch from Selenium IDE to Katalon Recorder, particularly if you want to use a continually improved product (we release almost weekly!). 

However, some of you may have built up many tests in Selenium IDE - and abandoning all your work is definitely not a viable solution. With this update, users can now smoothly migrate their tests from Selenium IDE to Katalon Recorder, and benefit from the full suite of KR features, time-to-value, and multiple integration points with other testing frameworks.
