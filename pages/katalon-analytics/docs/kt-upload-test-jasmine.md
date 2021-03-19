---
title: "Upload Test to Katalon TestOps via Jasmine." 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/kt-upload-test-jasmine.html
description: 
---

We can submit results from the Jasmine test frameworks to Katalon TestOps. An example with the Jasmine test can be download from [here](https://github.com/katalon-studio/testops-report-js.git).

On the **Visual Studio Code**, open a file Jasmine.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-jasmine/kt_vs_code_file_test_jasmine.png)

Open file "package.json".

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-mocha/kt_vs_code_package_json.png)

Type the command `npm install`, press **Enter**, and wait a few minutes for running.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-mocha/kt_vs_code_mocha_json_install.png)

On the page Katalon TestOps, we do 5 steps as follow:
* Choose a project, which we want to upload the test results.
* Click the tab **Configurations**.
* Click the tab **Framework Integration**.
* On the board **Framework Integration**, choose the tab **Mocha**.
* Click the button **Copy** on the right of the item **Install dependency**. And now we copied the command line `npm i -s @katalon/testops-mocha`.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-mocha/kt_bash_copy_mocha_npm.png)

On the **Visual Studio Code**, file "package.json", right-click for pasting the command `npm i -s @katalon/testops-jest` and press Enter. And we wait a few minutes for running.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-mocha/kt_vs_code_mocha_paste_bash.png)

Create a new files with the name "testops-config.json".

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-mocha/kt_vs_code_creat_testops_config.png)

On the page Katalon TestOps, we click the button **Copy** on the right of the item **Base** of **Configure**. 

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-mocha/kt_copy_configure_base.png)

On the **Visual Studio Code**, open file "testops-config.json
", paste the terms which we have just copied from Katalon TestOps. We save this file.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-mocha/kt_vs_code_paste_testops_config.png)

On the page Katalon TestOps, we click the button **Copy** on the right of the item **Import reports**. 

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-mocha/kt_npx_mocha.png)

On the **Visual Studio Code**, type the command `npm test`, press **Enter**, and wait a few minutes for running.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-mocha/kt_vs_code_npm_test.png)

On the **Test Planning** of **Katalon TestOps**, the Test Run was uploaded.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-mocha/kt_upload_test_planning.png)