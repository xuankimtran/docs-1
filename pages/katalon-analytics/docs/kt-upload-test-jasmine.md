---
title: "Upload Test to Katalon TestOps via Jasmine" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/kt-upload-test-jasmine.html
description: 
---

You can submit Jasmine framework's test results to Katalon TestOps.

> Notes:
>
> You can download a sample project [here](https://github.com/katalon-studio/testops-report-js.git) for upload testing via Jasmine.

Follow these steps:

1. Open the Jasmine file in [Visual Studio Code](https://code.visualstudio.com).

     <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-jasmine/kt_vs_code_open_pack_jasmine.png" width=100% alt="open jasmine in vsc"> 

2. Open the *package.json* file.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-jasmine/kt_vs_code_open_json.png" width=100% alt="open json file"> 

3. Type `npm install` for command, then press *Enter* and wait for it to run.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-jasmine/kt_vs_code_npm_install.png" width=100% alt="install npm"> 

    While waiting, go to Katalon TestOps website.

4. Sign in to [Katalon TestOps](https://testops.katalon.io/login) and go to your Project.

5. Go to **Configurations** > **Integrations**.

    The **Integrations** page appears.

6. Select **Jasmine** in the dropdown list.

    The Jasmine page appears as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-jasmine/jasmine-page-1.png" width=100% alt="jasmine page 1"> 

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-jasmine/jasmine-page-2.png" width=100% alt="jasmine page 2">

7. Copy the command line in the **Install dependency** section and paste it in the *package.json* file, then press *Enter* to run.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-jasmine/kt_vs_code_paste_npm_command.png" width=100% alt="install dependency command">

8. Create a new files named *testops-config.json* in Visual Studio Code (VSC).

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-jasmine/kt_vs_code_create_config_json.png" width=100% alt="create json file"> 

9. Copy the content in the **Configure TestOps plugin** section in Katalon TestOps and paste it in the newly-created *testops-config.json* file in VSC. Save this file.

     <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-jasmine/kt_vs_code_paste_testops_config.png" width=100% alt="configure testops in vsc"> 

10. Create a new file called *setup.js* on the *test* folder (the *./tests/setup.js* file) in VSC.

11. Copy the command in the **Add Report** section in Katalon TestOps and paste it in the *./tests/setup.js* file. Save this file.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-jasmine/kt_setup_js.png" width=100% alt="set up testops"> 

12. Copy the command in the **Run tests and upload reports** section in Katalon TestOps and paste it in VSC, then press *Enter* to run.

     <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-jasmine/kt_vs_code_npx_jas.png" width=100% alt="upload via Jasmine"> 

13. Type `npm test`, press **Enter** to run in VSC.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-jasmine/kt_vs_code_npm_test.png" width=100% alt="test via Jasmine"> 

    You have run tests and uploaded their reports via Jasmine.

14. Go to **Test Execution** > **Test Run Calendar**.

    You can now see all Test Runs here.