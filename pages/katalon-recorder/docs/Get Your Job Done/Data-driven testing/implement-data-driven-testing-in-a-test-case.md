---
title: "How to implement data-driven testing in a test case"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-recorder/docs/implement-data-driven-testing-in-a-test-case.html
redirect_from: 
description: "A tutorial for implementing data-driven testing in a test case in Katalon Recorder."
---

Whenever you want to execute a test case repeatedly with different data, you can implement data-driven testing (DDT). Katalon Recorder facilitates DDT with DDT commands and several data formats. See: [Data-driven testing in Katalon Recorder](https://docs.katalon.com/katalon-recorder/docs/data-driven-testing.html).

This tutorial shows you how to implement DDT in a test case.

In our example, we follow the test case with the scenario "log in and book a healthcare appointment," which consists of these steps:

1. Log in to the application under test (AUT) - Katalon CURA Healthcare Service: `https://katalon-demo-cura.herokuapp.com`.
2. Book an appointment by filling in a form with visit date and comment.
3. On the confirmation page, verify that the text "Appointment Confirmation" is visible.
4. Log out.

To demonstrate implementing DDT in Katalon Recorder, we create a test case that uses data from a CSV data file to book three appointments. The process is as follows:

1. Record the test case: we record the test case to log in and book an appointment manually.
2. Implement DDT in the test case: we bind the test case with a data file and modify it with DDT commands.

## Record the test case

We record a test case according to the presented scenario.

Follow these steps:

1. In Katalon Recorder, create a new test case, then click on the **Record** button to start recording.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/implement-ddt-in-a-test-case/KR-new-test-case.png" width=70% alt="Katalon Recorder new test case">

2. In an active browser tab, navigate to the AUT.

    Here the URL for the AUT is `https://katalon-demo-cura.herokuapp.com`.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/implement-ddt-in-a-test-case/KR-AUT-overview.png" width=70% alt="Katalon Recorder AUT overview">

3. Log in to the AUT.

    On the top-right corner of the homepage, click on the *menu* button and select **Login**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/implement-ddt-in-a-test-case/KR-AUT-login-button.png" width=70% alt="Katalon Recorder AUT login button">

    On the opened Login page, type in the sample username and password, then click **Login**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/implement-ddt-in-a-test-case/KR-AUT-login-page.png" width=70% alt="Katalon Recorder AUT login page">

4. On the **Make Appointment** page, input the visit date and comment, then click **Book Appointment**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/implement-ddt-in-a-test-case/KR-AUT-make-appointment-page.png" width=70% alt="Katalon Recorder AUT make appointment page">

5. On the **Appointment Confirmation** page, right-click on the displayed text "Appointment Confirmation" and select **Katalon Recorder > verifyText**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/implement-ddt-in-a-test-case/KR-AUT-appointment-confirmation-page.png" width=70% alt="Katalon Recorder AUT appointment confirmation page">

6. Log out of the AUT. Click on the *menu* button and select **Logout**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/implement-ddt-in-a-test-case/KR-AUT-logout-button.png" width=70% alt="Katalon Recorder AUT logout button">

7. In Katalon Recorder, click on the **Stop** button to stop the recording

The recorded test case is as follows:

<a class="pop">
<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/implement-ddt-in-a-test-case/KR-recorded-test-case.png" width=70% alt="Katalon Recorder recorded test case">
</a>
<p style="text-align: center;"><em>Click the image to enlarge</em></p>

## Implement data-driven testing

In Katalon Recorder, there are three steps to implement DDT in a test case:

1. Prepare the data file.
2. Add the data file to your workspace.
3. Configure data-driven commands and variables in the test case to use data from the data file.

### Prepare the data file

Katalon Recorder supports two data file formats: CSV and JSON. To learn more about the supported formats and their specifications, refer to this document: [Data-driven testing in Katalon Recorder](https://docs.katalon.com/katalon-recorder/docs/data-driven-testing.html#data-file-formats).

In our example, we use the following CSV file:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/implement-ddt-in-a-test-case/KR-prepared-CSV-file.png" width=70% alt="Katalon Recorder recorded test case">

This CSV data file has two columns, "Date" and "Comment", corresponding to the two data types required to book an appointment.

### Add the data file to the workspace

Follow these steps:

1. In the **Workspace** sidebar, click on the *more* icon in the **Test Data** section.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/implement-ddt-in-a-test-case/KR-add-test-data.png" width=30% alt="Katalon Recorder add test data">

2. In the opened file explorer, select the CSV file.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/implement-ddt-in-a-test-case/KR-file-explorer.png" width=70% alt="Katalon Recorder select the CSV file">

3. Katalon Recorder should display the selected file under the **Test Data** section.

### Configure data-driven commands and variables in the test case

The manual steps to configure data-driven commands and variables are as follows:

1. Add the `loadVars` command to the beginning of your test case.
2. Type in the name of the loadVars target file, e.g. `Sample-CSV.csv`.
3. In the test case, use variables with the same names as the columns in the data file.
4. Add the `endLoadVars` command to the end of your test case.

Katalon Recorder also provides a simple user interface to configure data-driven commands and variables.

Follow these steps to configure using the interface:

1. Select the data file. Right-click on the data file and select **Use this in a test case**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/implement-ddt-in-a-test-case/KR-use-this-in-a-test-case-button.png" width=30% alt="Katalon Recorder use test data file">

2. Select the test case. In the displayed menu, select the desired test case. Click **Next** to continue.

    Here we select the test case that we previously recorded.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/implement-ddt-in-a-test-case/KR-select-test-case-for-DDT.png" width=70% alt="Katalon Recorder select test case">

3. Use the data from the data file. In the displayed test case, select the commands and specify the desired variables. Click **Add** when done.

    Katalon Recorder specifies a variable using the `${<variable_name>}` syntax as a placeholder in the **Value** field. When executing the test case, Katalon Recorder expands the variable into its value.

    In our case, we want to use the visit date and comment from the CSV file, so we replace the current values with the variables `Date` and `Comment`.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/implement-ddt-in-a-test-case/KR-DDT-configure-variable-visit-date.png" width=70% alt="Katalon Recorder configure visit date variable">

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/implement-ddt-in-a-test-case/KR-DDT-configure-variable-comment.png" width=70% alt="Katalon Recorder configure comment variable">

4. Verify that the values in the test case are replaced with the correct variables.

    <a class="pop">
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/implement-ddt-in-a-test-case/KR-DDT-configured-test-case.png" width=70% alt="Katalon Recorder configure comment variable">
    </a>
    <p style="text-align: center;"><em>Click the image to enlarge</em></p>

5. Play the test case and verify the results in the **Log** view. The log message should indicate that Katalon Recorder expands the specified variables into test data.

    <a class="pop">
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/implement-ddt-in-a-test-case/KR-DDT-results.png" width=70% alt="Katalon Recorder DDT results">
    </a>
    <p style="text-align: center;"><em>Click the image to enlarge</em></p>

**See also**:
* The Katalon Academy course: [Data-Driven Testing with Katalon Recorder](https://academy.katalon.com/courses/katalon-recorder-data-driven-testing/).