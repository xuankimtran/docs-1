---
title: "JMeter Integration (Deprecated) "
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/jmeter-integration.html
---

> Discontinued support of this plugin in version 7.0.0

You can integrate Katalon Studio with Apache JMeter for API/Web Service testing in 2 ways:

### Use JMeter Integration plugin

Visit our [Store](https://store.katalon.com/product/139/JMeter-Integration) to download the plugin and learn more about its details.

Learn [how to install a plugin](https://docs.katalon.com/katalon-store/docs/user/getting-started.html).

### Manually integrate JMeter with Katalon Studio

You can integrate JMeter with Katalon Studio yourself by following this tutorial.

1. Install Gradle. Please follow the [official instruction](https://gradle.org/install/) by Gradle.

2. Pull JMeter dependency.

* Create a `build.gradle` file in your project
* Run the following command to download Jmeter dependencies: `gradle katalonCopyDependencies`.

3. Create JMeter Runner.

* Download [JMeter](https://jmeter.apache.org/download_jmeter.cgi) > Extract the bin folder in the **Include** directory of a Katalon Studio project.
* In **Include/scripts/groovy**, create `JMeterRunner` (JMeter Runner configuration class) and `KatalonSamplerClient`, which will execute Katalon test cases and return test results.

4. Once JMeter is ready, you can run your project.

* Define a custom Jmeter keyword, which will create a new JMeterRunner when the keyword is called.
* Create a test case.
* Call the Jmeter keyword then wait for the results.

You can download a [sample project](https://github.com/thongmgnguyen/katalon-jmeter-sample) using JMeter to perform API testing in Katalon Studio.
