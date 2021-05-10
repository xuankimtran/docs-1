---
title: "Upload Test to Katalon TestOps via Jest" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/kt-upload-test-jest.html
description: 
---

We can submit results from the Jest test frameworks to Katalon TestOps. An example with the Jest test can be download from [here](https://github.com/katalon-studio/testops-report-js).

On the **Visual Studio Code**, open a file Jest.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-jest/kt_vs_code_open_jest.png)

Open file "package.json".

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-jest/kt_vs_code_open_package_json.png)

Type the command `npm install`, press **Enter**, and wait a few minutes for running.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-jest/kt_vs_code_json_install.png)

On the page Katalon TestOps, we do 5 steps as follow:
* Choose a project, which we want to upload the test results.
* Click the tab **Configurations**.
* Click the tab **Framework Integration**.
* On the board **Framework Integration**, choose the tab **Jest**.
* Click the button **Copy** on the right of the item **Install dependency**. And now we copied the command line `npm i -s @katalon/testops-jest`.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-jest/kt_bash_copy_npm.png)

On the **Visual Studio Code**, file "package.json", right-click for pasting the command `npm i -s @katalon/testops-jest` and press Enter. And we wait a few minutes for running.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-jest/kt_vs_code_paste_bash.png)

Create two new files with the name "testops-config.json" and "jest.config.js".

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-jest/kt_create_file_json_js.png)

On the page Katalon TestOps, we click the button **Copy** on the right of the item **Base** of **Configure**. 

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-jest/kt_copy_configure_base.png)

On the **Visual Studio Code**, open file "testops-config.json
", paste the terms which we have just copied from Katalon TestOps. We save this file.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-jest/kt_paste_testops_json.png)

On the page Katalon TestOps, we click the button **Copy** on the right of the item **Add Report** of **Configure**.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-jest/kt_copy_configure_add_report.png)

On the **Visual Studio Code**, open file "jest.config.js", paste the terms which we have just copied from Katalon TestOps. We save this file.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-jest/kt_paste_js_vs_code.png)

On the **Visual Studio Code**, type the command `npx jest`, press **Enter**, and wait a few minutes for running.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-jest/kt_npx_jest.png)

On the **Test Planning** of **Katalon TestOps**, the Test Run was uploaded.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-jest/kt_upload_test_plan.png)