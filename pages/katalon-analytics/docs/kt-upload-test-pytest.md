---
title: "Upload Test to Katalon TestOps via Pytest" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/kt-upload-test-pytest.html
description: 
---

You can submit test results from the Pytest framework to Katalon TestOps.

> Notes:
>
> You can download [Pytest sample project](https://github.com/katalon-studio-samples/testops-pytest-sample) to upload tests from Pytest.

Follow these steps:

1. Open the Pytest file in the file editor that it is compatible with (e.g., [Visual Studio Code](https://code.visualstudio.com)).

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-pytest/kt_open_file_pytest.png" width=100% alt="open pytest in vsc"> 

2. Sign in to [Katalon TestOps](https://testops.katalon.io/login) and go to your Project.

3. Go to **Configurations** > **Integrations**.

    The **Integrations** page appears.

4. Select **Pytest** in the dropdown list.

    The Pytest page appears as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-pytest/pytest-page-1.png" width=100% alt="pytest page 1"> 

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-pytest/pytest-page-2.png" width=100% alt="pytest page 2"> 

5. Copy the command line in the **Install dependency** section and paste it in the Pytest file's terminal in the file editor to install the Katalon TestOps plugin.

6. Create a new file named *testops-config.json* in your file editor.

7. Copy the command line in the **TestOps Credentials & Project** section on the Pytest page and paste it in the *testops-config.json* file in your file editor.

     <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-pytest/kt_paste_testops_config_1.png" width=100% alt="testops config in vsc"> 

8. Create a new file named *conftest.py*.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-pytest/kt_open_conftest_py_1.png" width=100% alt="conftest py file">

9. Copy the command in the **Add Report** section on the Pytest page and paste it in the *conftest.py* file in your file editor. Save this file.

     <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-pytest/kt_paste_conftest_py_1.png" width=100% alt="paste content to conftest file">

10. Type the `pytest` command and press *Enter* to run tests.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-pytest/kt_command_python_test_1.png" width=100% alt="run with pytest">

    You have run tests and uploaded their reports via Pytest.

11. Go to **Test Execution** > **Test Run Calendar**.

    Your uploaded Test Runs now display here.

