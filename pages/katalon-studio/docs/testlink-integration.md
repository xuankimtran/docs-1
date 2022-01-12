---
title: "TestLink Integration" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/testlink-integration.html

description: Documentation for TestLink Integration plugin 
---

### TestLink Installation

* Download XAMPP from the below link.
[https://www.apachefriends.org/download.html](https://www.apachefriends.org/download.html)

* Upon successful installation, Tomcat will be started by default.

* Start the Apache and MySQL services from XAMPP Control Panel.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/Testlink/1-XAMPP-control-panel.png" width="100%" alt="TestLink Installation">

* Download the TestLink from the below link. Currently, the latest version of TestLink is 1.9.19. You can use the latest version for the Integration.
[https://sourceforge.net/projects/testlink/files/TestLink%201.9/](https://sourceforge.net/projects/testlink/files/TestLink%201.9/) 

* Extract TestLink and place it on XAMPP’s “htdocs” directory. 

* Hit the below URL in any browser. 
[http://localhost/phpmyadmin/](http://localhost/phpmyadmin/) 

* Create a new database called “testlink” from the database menu. 

* Add a user account from the “Privileges” tab under “More” options for “testlink” database.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/Testlink/2-Add-user-1.png" width="100%" alt="Add user account in TestLink">

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/Testlink/3-Add-user-2.png" width="100%" alt="Add user account in TestLink">

* Hit the below URL in any browser to open the testlink installation setup. 
[http://localhost/testlink-1.9.16/install/index.php](http://localhost/testlink-1.9.16/install/index.php) 

* Check the “I agree to the terms set out in this license” checkbox and click “Continue” button.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/Testlink/4-Agree-term.png" width="100%" alt="Agree terms in TestLink">


* The below permissions will be failed.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/Testlink/5-Testlink-package.png" width="100%" alt="Failed terms in the TestLink package">

* Navigate to the testlink package and open the “config.inc.php” file. 

* Update the parameters as below 

**$tlCfg->log_path = ‘D:/xampp/htdocs/testlink-1.9.16/logs/’; (Path of testlink package)** 

**$g_repositoryPath = ‘D:/xampp/htdocs/testlink-1.9.16/upload_area/’; (Path of testlink package)** 

* Refresh the page and the above “failed” status will be resolved.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/Testlink/6-Failed-permission.png" width="100%" alt="Resolve failed terms in the TestLink package">

* Click the “Continue” button. 

* Enter the Database name as “testlink”. 

* Enter the Database admin login and password as “admin”. 

* Enter your database username and password for “TestLink DB login and password”.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/Testlink/7-Process-testlink-setup.png" width="100%" alt="Set up Testlink">

* Click the  “Process TestLink Setup!” button. 

* Once the installation is completed, a window will be displayed to notify that the Installation was successful.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/Testlink/8-Successful.png" width="100%" alt="Successfully install Testlink">

### TestLink Login

* Hit the below URL to login to TestLink. 
[http://localhost/testlink-1.9.16/](http://localhost/testlink-1.9.16/) 

* Enter the Login Name and Password as “admin” to login as admin.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/Testlink/9-Testlink-login.png" width="70%" alt="Login Testlink">

* Once you login to TestLink, it prompts to create a Test Project. 

* Create a Test Plan, Build, Test suite with Test cases by selecting the corresponding links from the Dashboard.


### Test Project Creation

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/Testlink/10-Test-project-creation.png" width="100%" alt="Create test project in Testlink">

### Test Plan Creation

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/Testlink/11-Test-plan-creation.png" width="100%" alt="Create test plan in Testlink">

### Build Creation

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/Testlink/12-Build-creation.png" width="100%" alt="Build creation in Testlink">

### Test Suite Creation

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/Testlink/13-Test-suite-creation.png" width="100%" alt="Test suite creation in Testlink">

### Test Case Creation

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/Testlink/14-Test-case-creation.png" width="100%" alt="Test case creation in Testlink">

### API Key Generation and Execution Type Changes on TestLink


1. Generate the API Key on TestLink as below.

• Click the “My Settings” icon next to logout.

• Personal API access Key will be “none” under the “API Interface” section. 

• Click “Generate a new key” button.

• Key will be generated from “Personal API access key”.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/Testlink/15-API-key.png" width="100%" alt="Create API key in Testlink">

2. After generating a key, update the test execution status as “Automated” as below.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/Testlink/16-Automated-status.png" width="100%" alt="Create API key in Testlink">

### Integration of Katalon test scripts with TestLink

Make a note of the TestLink Key, Testlink Url, Project Name, Test Plan Name, and Build Name created on TestLink. These details need to be used in our configuration in below:

Go to **Project > Settings > Plugins > TestLink Integration** and setup these following configurations:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/Testlink/KS-TESTLINK-Enable-Testlink.png" width="70%" alt="Enable TestLink Integration">

This plugin provides the only custom keyword updateResults to update the test results on Testlink.

### Test Execution Results update on TestLink
Before execution, the test status will be “Not Run” on Testlink.
If the test case is passed, the status will be updated as “Passed”.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/Testlink/18-Passed.png" width="100%" alt="View test results in Testlink">

If the test case is failed, the status will be updated as “Failed”.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/Testlink/19-Failed.png" width="100%" alt="View test results in Testlink">


