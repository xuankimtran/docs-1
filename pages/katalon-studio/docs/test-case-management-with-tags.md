---
title: "Test Case Management With Tags" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/test-case-management-with-tags.html

description: 
---
**Easily manipulate tag properties for better test case management**

- Utilize existing tag values, separate tag tokens by comma or semicolon
-  View all tags in the project
- Easily append existing tags to test case without typo mistakes

**Append & manage tags**

Open a test case > Properties > input tag values; separate them by colon or semi-colon if applicable.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-case-management-with-tags/Tags_3.png)

In case the tag properties have already had value, the tag token will be automatically separated by colons and semi-colons.
Open a test case > Properties > Click Manage Tags > select tags to append > click Append Tags

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-case-management-with-tags/Tags_4.png)

Please note that the existing tags cannot be removed by unchecking the boxes, this feature is just for appending tags to test cases.


**Search For Test Cases With Multiple Tags**

This feature will be enabled in Query Provider of Dynamic Querying Test Suite after you successfully install Test Case Management With Tags plugins.

To search for test artifacts labeled with Multiple Tags, directly type on the search box follow this syntax: Tags = (NameOfTag1, NameOfTag2)

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-case-management-with-tags/tags-search.png)

**Execute only Test Cases that have certain tags in a Test Suite

You can execute only Test Cases with tags ```tag1``` and ```tag2``` in a Test Suite by including the argument ```testCaseTags="tag1, tag2"``` to your command line.

Example execution log when this feature is used, assuming the Test Suite being executed has three Test Cases.
```
----------------- TEST CASE TAGS PLUGIN START FILTERING -----------------
Test Cases/Test Case with tag 1 and tag 2 is a test case to be run
Test Case/Test Case with tag 1 only is filftered out
Test Case/Test Case with tag 2 only is filtered our
----------------- TEST CASE TAGS PLUGIN FINISH FILTERING -----------------
```

