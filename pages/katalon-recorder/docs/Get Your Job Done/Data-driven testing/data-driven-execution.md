---
title: "Data-driven execution"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-recorder/docs/data-driven-execution.html
description:
---

Data-driven execution is the ability to execute a test with multiple data set. For example, when inputting patient information from a CSV file to your website, you would develop one test case and use data-driven execution to execute it with the prepared data set.

## Data-driven execution sample
Since version 5.4.0, a data-driven execution sample is available for all users. You can adapt it to your own purposes as needed.

**How to add the data-driven execution sample**

The sample will be automatically visible to new users when they first go through the Product Tours. Existing users can go to *Extended Feature > Essential Product Tours* to trigger the Product Tours which will add the sample to KR.

<img src="https://raw.githubusercontent.com/katalon-studio/docs-images/master/katalon-recorder/docs/jtbd/data-driven/KR-5-4-0-how-to-add-data-driven-sample-test-case.png" width="100%">

**Anatomy of the data-driven execution sample**

The data-driven execution sample contains of a test case named *Book many healthcare appointments* and a data file named *sample_data.csv*. 

<img src="https://raw.githubusercontent.com/katalon-studio/docs-images/master/katalon-recorder/docs/jtbd/data-driven/KR-5.4.0-sample-data-driven-execution-sample-test-case.png" width="100%">


The test case uses two variables `visit_date` and `comment`, which correspond to the column names specified in the data file:

```
visit_date,comment
26/10/1984,some text 1
1/10/1996,some text 2
```

When executed, the test case will book two appointments using on the information in the data file.


## Tutorial
The following video (2:29 to 5:26) demonstrates how to use data-driven testing with Katalon Recorder and a JSON file. It walks you through how to prepare a JSON file and how to convert a normal test case into a data-driven one.

<iframe width="560" height="315" src="https://www.youtube.com/embed/sgzFkQ-0Ta8" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
