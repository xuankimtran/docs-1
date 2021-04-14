---
title: "Upload Test to Katalon TestOps via Pytest" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/kt-upload-test-pytest.html
description: 
---

We can submit results from the Pytest test frameworks to Katalon TestOps. An example with the Pytest test can be download from [here](https://github.com/katalon-studio/testops-report-python).

On the **Visual Studio Code**, open a file Pytest.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-pytest/kt_open_file_pytest.png)

On the page Katalon TestOps, we do 5 steps as follow:
* Choose a project, which we want to upload the test results.
* Click the tab **Configurations**.
* Click the tab **Framework Integration**.
* On the board **Framework Integration**, choose the tab **Pytest**.
* Click the button **Copy** on the right of the item **Install dependency**. And now we copied the command line `pip3 install testops-pytest`.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-pytest/kt_bash_install_dependency.png)

On the **Visual Studio Code**, open file "testops-config.json".

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-pytest/kt_open_testops_config_json.png)

On the page Katalon TestOps, we click the button **Copy** on the right of the item **TestOps Credentials & Project** of **Configure TestOps plugin**. 

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-pytest/kt_copy_config_testops_credential.png)

On the **Visual Studio Code**, open file "testops-config.json", paste the terms which we have just copied from Katalon TestOps. We save this file.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-pytest/kt_paste_testops_config.png)

On the **Visual Studio Code**, open file "conftest.py".

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-pytest/kt_open_conftest_py.png)

On the page Katalon TestOps, we click the button **Copy** on the right of the item **Add Report**. 

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-pytest/kt_copy_conftest.png)

On the **Visual Studio Code**, paste the terms, which we have just copied from Katalon TestOps in file "conftest.py". We save this file.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-pytest/kt_paste_conftest_py.png)

On the **Visual Studio Code**, type the command `python -m pytest`, press **Enter**, and wait a few minutes for running.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-pytest/kt_command_python_test.png)

On the **Test Planning** of **Katalon TestOps**, the Test Run was uploaded.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-upload-test-pytest/kt_upload_pytest.png)