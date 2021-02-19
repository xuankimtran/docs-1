---
title: "Validate expected values"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-recorder/docs/validate-expected-values.html
description:
---

Validating expected values is important when you want to confirm that certain states are according to your expectation. For example, when you automate purchasing an item, you want to make sure that the name of the item reflects the one you actually want.

There are at least two ways to add verification statements to a scenario.

1.  Use context menu in a Recording session.
2.  Add verification statements manually.

## Use context menu in a Recording session

After recording a test case bases, but before , the last step is right-click on the element that you want to verify then select the corresponding command to do that.

1.  Record your test steps

2.  At the very last step, **right-click** on the **element** that you want to **verify**

3.  Click on **Katalon Recorder (Selenium tests generator)** on the context menu

![](../../images/katalon-recorder/docs/validate-expected-values/media/image1.jpeg)

Then you got a new verification command

![](../../images/katalon-recorder/docs/validate-expected-values/media/image2.jpeg)

## Add verification statements manually

You can also add a new verification statement manually.

1\. Record your teps

2\. Click on **+** button to add a new command

![](../../images/katalon-recorder/docs/validate-expected-values/media/image3.jpeg)

3\. In the **Command** combobox, type "**verify**"

Then you got the autocomplete list of verification commands

![](../../images/katalon-recorder/docs/validate-expected-values/media/image4.jpeg)

4\. Select the **command** that you are looking for, e.g. **verifyText**

5\. Click on the **icon** next to **Target** to select the element that you want to verify

![](../../images/katalon-recorder/docs/validate-expected-values/media/image5.jpeg)

You got the result as the below screenshot. You can change the address to other options such as xpath or **CSS Selectors**.

![](../../images/katalon-recorder/docs/validate-expected-values/media/image6.jpeg)

6\. Input the **value** that you want to verify

![](../../images/katalon-recorder/docs/validate-expected-values/media/image7.jpeg)

You should click on **Play** button to execute the test to see your result

![](../../images/katalon-recorder/docs/validate-expected-values/media/image8.png)
