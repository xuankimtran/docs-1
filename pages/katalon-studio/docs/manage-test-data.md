---
title: "Manage Test Data" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/manage-test-data.html 
redirect_from:
    - "/display/KD/Manage+Test+Data/"
    - "/display/KD/Manage%20Test%20Data/"
    - "/x/W4Iw/"
    - "/katalon-studio/docs/manage-test-data/"
description: 
---
> Starting from Katalon Studio version 6.3.0, you can configure variable binding to read test data values as the intended data types. Refer to [this document](https://docs.katalon.com/katalon-studio/docs/bind-as-string.html) for an example of Variable binding for Test Data with option bind into test case as string enabled/disabled.

Create an Excel Test Data
-------------------------

1.  Select **File > New > Test Data** from the main menu. The **New Test Data** dialog is displayed. Enter the name for your test data and select **Data Type** as **Excel File**. Click **OK**.  
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/manage-test-data/image2017-1-24-153A593A35.png)

2.  Browse to the Excel file that you want to import into Katalon Studio.
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/manage-test-data/image2017-1-24-163A53A30.png)

3.  Data from the selected Excel file is populated into the **preview section** below.  
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/manage-test-data/image2017-1-24-163A173A6.png)

4.  Save the Test Data when you finish. The data set defined here can be utilized in other configurations. For example, you can use it to input data for keywords in [Manual View](/display/KD/Manual+View) or [data for Test Execution](/x/7AAM) when setting up test suites.

Create a CSV Test Data
----------------------

1.  Select **File > New > Test Data** from the main menu. The **New Test Data** dialog is displayed. Enter the name for your test data and select **Data Type** as **CSV File**. Click **OK**.  
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/manage-test-data/image2017-1-24-163A233A37.png)

2.  Browse to the CSV file that you want to import into Katalon Studio.
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/manage-test-data/image2017-1-24-163A283A34.png)

3.  Data from the selected CSV file is populated to the **preview section** below.  
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/manage-test-data/image2017-1-24-163A293A15.png)

4. Save the Test Data when you finish. The data set defined here can be utilized in other configurations. For example, you can use it to input data for keywords in [Manual View](/display/KD/Manual+View) or [data for Test Execution](/x/7AAM) when setting up test suites.

Create an Internal Test Data
----------------------------

With **Internal Data**, you can freely define the data in tabular format. It's up to you to decide how many columns, rows, and what value for each cell.

1.  Select **File > New > Test Data** from the main menu. The **New Test Data** dialog is displayed. Enter the name for your test data and select **Data Type** as **Internal Data**. Click **OK**.  
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/manage-test-data/image2017-2-6-103A293A29.png)

2.  In the Editor View, select the option to add a new column.  
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/manage-test-data/image2017-2-6-103A373A52.png)

3.  Select the option to add a new row.  
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/manage-test-data/image2017-2-6-103A413A42.png)

4.  Finally, click on each cell to input the value for them.  
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/manage-test-data/image2017-2-6-103A433A5.png)
      
    
5.  You can edit or delete the columns (or rows) by right-clicking to access the context menu.  
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/manage-test-data/image2017-2-6-103A443A41.png)

6. Save the Test Data when you finish. The data set defined here can be utilized in other configurations. For example, you can use it to input data for keywords in [Manual View](/display/KD/Manual+View) or [data for Test Execution](/x/7AAM) when setting up test suites.

Create a Database Data
----------------------

With **Internal Data**, you can freely define the data in tabular format. It's up to you to decide how many columns, rows, and what value for each cell.

1.  Select **File > New > Test Data** from the main menu. The **New Test Data** dialog is displayed. Enter the name for your test data and select **Database Data** as **Data Type**. Click **OK**.  
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/manage-test-data/image2017-2-6-103A583A56.png)

2.  Click **Edit Query** to open the **Database Connection and Query settings** dialog.  
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/manage-test-data/image2017-2-6-113A63A11.png)

3.  Enter the connection details as well as the data query then click **OK**.  

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/manage-test-data/newui.png" width="796" height="436">

    Starting from **Katalon Studio version 7.0.0 and later**, you can query data from additional database sources with the **JDBC Driver** field in the dialog. You can enter the ClassDriverName of the database that has a library support connection (JDBC).

    > You can check **Use global database connection settings** to use the connection defined in project settings. Refer to [Database Settings](/display/KD/Database+Settings) for more details.

4.  Queried data is fetched and loaded respectively into the **preview section** below.  
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/manage-test-data/image2017-2-6-113A193A41.png)

5. Save the Test Data when you finish. The data set defined here can be utilized in other configurations. For example, you can use it to input data for keywords in [Manual View](/display/KD/Manual+View) or [data for Test Execution](/x/7AAM) when setting up test suites.
