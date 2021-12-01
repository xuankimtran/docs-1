---
title: "Upload Test to Katalon TestOps via Mocha" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/kt-upload-test-mocha.html
description: 
---

You can submit Mocha framework's test results to Katalon TestOps.

> Notes:
>
> You can download a sample project [here]((https://github.com/katalon-studio-samples/testops-report-sample-js)) for upload testing via Mocha.

Follow these steps:

1. Open the Mocha file in [Visual Studio Code](https://code.visualstudio.com).

     <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-mocha/kt_vs_code_open_mocha.png" width=100% alt="open mocha in vsc"> 

2. Open the *package.json* file.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-mocha/kt_vs_code_package_json.png" width=100% alt="open json file"> 

3. Type `npm install` for command, then press *Enter* and wait for it to run.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-mocha/kt_vs_code_mocha_json_install.png" width=100% alt="run command"> 

    While waiting, go to Katalon TestOps website.
4. Sign in to [Katalon TestOps](https://testops.katalon.io/login) and go to your Project.

5. Go to **Configurations** > **Integrations**.

    The **Integrations** page appears.

6. Select **Mocha** in the dropdown list.

    The Mocha page appears as below.
    
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-mocha/mocha-page-1.png" width=100% alt="mocha page 1"> 

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-mocha/mocha-page-2.png" width=100% alt="mocha page 2"> 

7. Copy the command line in the **Install dependency** section and paste it in the *package.json* file, then press *Enter* to run.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-mocha/kt_vs_code_mocha_paste_bash.png" width=100% alt="install dependency command"> 

8. Create a new file with the name *testops-config.json* in Visual Studio Code (VSC).

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-mocha/kt_vs_code_creat_testops_config.png" width=100% alt="create vsc file"> 

9. Copy the content in the **Configure TestOps plugin** section in Katalon TestOps and paste it in the newly-created *testops-config.json* file in VSC. Save this file.

     <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-mocha/kt_vs_code_paste_testops_config.png" width=100% alt="configure testops in vsc"> 

10. Copy the command in the **Run tests and upload reports** section in Katalon TestOps and paste it in the *testops-config.json* file in VSC, then press *Enter* to run.

    You have uploaded reports.

11. Type the command `npm test` in the *testops-config.json* file in VSC, and press **Enter** to run tests.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-mocha/kt_vs_code_npm_test.png" width=100% alt="configure testops in vsc"> 

12. Go to **Test Execution** > **Test Run Calendar**.

    You can now see all Test Runs here.