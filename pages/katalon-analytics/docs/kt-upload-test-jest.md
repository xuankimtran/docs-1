---
title: "Upload Test to Katalon TestOps via Jest" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/kt-upload-test-jest.html
description: 
---

You can submit test results from the Jest framework to Katalon TestOps.

> Notes:
>
> You can download [Jest sample project](https://github.com/katalon-studio-samples/testops-report-sample-js) to upload tests from Jest.

Follow these steps:

1. Open the Jest file in the file editor that it is compatible with (e.g., [Visual Studio Code](https://code.visualstudio.com)).

     <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-jest/kt_vs_code_open_jest.png" width=100% alt="open jest in vsc"> 

2. Open the *package.json* file.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-jest/kt_vs_code_open_package_json.png" width=100% alt="open json file"> 

3. Type the `npm install` command, then press *Enter* and wait for it to run.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-jest/kt_vs_code_json_install.png" width=100% alt="run command"> 

    While waiting, go to the Katalon TestOps website.

4. Sign in to [Katalon TestOps](https://testops.katalon.io/login) and go to your Project.

5. Go to **Configurations** > **Integrations**.

    The **Integrations** page appears.

6. Select **Jest** in the dropdown list.

    The Jest page appears as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-jest/jest-page-1.png" width=100% alt="jest page 1"> 

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-jest/jest-page-2.png" width=100% alt="jest page 2"> 
     
7. Copy the command line in the **Install dependency** section and paste it in the *package.json* file, then press *Enter* to run.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-jest/kt_vs_code_paste_bash.png" width=100% alt="install dependency command"> 

8. Create two new files: *testops-config.json* and *jest.config.js* in your file editor.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-jest/kt_create_file_json_js.png" width=100% alt="create json file"> 

9. Copy the content in the **Configure TestOps plugin** section in Katalon TestOps and paste it in the newly-created *testops-config.json* file. Save this file.

     <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-jest/kt_paste_testops_json.png" width=100% alt="configure testops in vsc"> 

10. Copy the command in the **Add Report** section in Katalon TestOps and paste it in the *jest.config.js* file. Save this file.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-jest/kt_paste_js_vs_code.png" width=100% alt="jest config"> 

11. Type the `npx jest` command and press *Enter* to run.

     <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-jest/kt_npx_jest.png" width=100% alt="run jest"> 

    You have uploaded tests to Katalon TestOps via Jest.

12. Go to **Test Execution** > **Test Run Calendar**.

    Your uploaded Test Runs now display here.

