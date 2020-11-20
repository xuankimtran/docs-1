---
title: "Search Test Cases"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/search.html
redirect_from:
    - "/katalon-studio/docs/advanced-search/"
    - "/katalon-studio/docs/advanced+search/"
    - "/katalon-studio/docs/advanced%20search/"
    - "/katalon-studio/docs/advanced-search.html"
    - "/katalon-studio/docs/advanced+search.html"
    - "/katalon-studio/docs/advanced%20search.html"
    - "/katalon-studio/docs/dynamic-querying-test-suite.html"
description: 
---
> Query Builder applies ONLY to **built-in** advanced search function.

Searching manually for test artifacts can be time-consuming. The Query Builder in Katalon Studio helps reduce time on finding the desired test artifacts based on given criteria.

The search function is used for various test artifacts such as test case, test suite, and folder.
There are two ways to use the Search function in Katalon Studio: input search criteria directly on the **Search bar**, or use the **Query Builder** button.

The **Query Builder** button is located on the top right of the **Tests Explorer** area, next to the search bar. You may also find this Query Builder function while working with test suites. It can be used to find the desired test case based on certain criteria.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/search/Advance-Search-Button-Location.png)

To execute, please click on the Query Builder button and input search criteria.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/search/advance-search-box.png)

The fields on the Query Builder menu include:
- **ID**: to search by to the exact IDs of the test artifact
- **Name**: to search by the name of the test artifact
- **Description**: to search by the description associated with the test artifacts
- **Comment**: to search by the comments attached to the test artifacts
- **Tag**: to search by the tag linked to the test artifacts

***Note***: Every field in this Query Builder mode can be applied to search for all types of objects such as test case, test suite, folder, etc.

To get the ID of the object, follow the steps below:
Navigate to **Tests Explorer** > Find the object whose ID you want to get > Right click > **Copy ID** > Paste it into the ID text box.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/search/Copy-ID.png)

In case you want to get the tag name of the object (this method CANNOT be applied when searching for folders):

Navigate to **Tests Explorer** > Find the object whose ID you want to get > Right click > **Properties** > The Test Case Properties window will appear > Copy the text in the **Tag** box > Paste it into the **Query Builder** box.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/search/Test-Case-Properties.png)
  
***Note***: You can only search for only one tag name at a time. The same process applies with getting descriptions and comment keywords.

Another way to search for test objects is to directly type on the search box. For example:

id=(Test Cases/Jira sync with BDD) 

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/search/1.png)

All test cases associated with the ‘Advance Examples’ ID will be filtered and returned.
 
***Note***: To search for test artifacts labeled with multiple tags, follow this syntax: Tags = (NameOfTag1, NameOfTag2).




