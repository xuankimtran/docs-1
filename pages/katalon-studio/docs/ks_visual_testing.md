---
title: "Visual Testing in Katalon TestOps" 
sidebar: katalon_studio_docs_sidebar
permalink: /katalon-analytics/docs/ks-visual-testing.html 
redirect_from:
description: This feature helps us compare screenshots between executions.
---

In Katalon TestOps, you can compare images captured during test executions with Visual Testing.

> Requirements:
>
> * You have enabled [Katalon Studio Integration](https://docs.katalon.com/katalon-studio/docs/katalon-analytics-beta-integration.html).

## Set up Visual Testing

Follow these steps:

1. Enable screenshot capture in Katalon Studio. See [Capture Screenshots](https://docs.katalon.com/katalon-studio/docs/capture-screenshots.html).

2. Run a Test Suite in Katalon Studio.

> Notes:
>
> If you have enabled Katalon Studio Integration, Katalon Studio automatically uploads Test Results to Katalon TestOps.

3. Sign in to [Katalon TestOps](https://testops.katalon.io/login) and go to your Project. 

4. Go to **Reports & Analytics** > **Visual Testing**.

    The **Visual Test Runs** page appears as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-july-visual-testing/visual-testing-page-testops.png" width=100% alt="visual test runs page in visual testing">

5. Click on the ID of a Test Run.

    The Test Run's **Results** page appears.

6. Select the **Checkpoints** tab.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-july-visual-testing/checkpoints-page.png" width=100% alt="test run #1 checkpoints page">

    You can see the screenshots captured during a test execution.

7. Select one of the screenshots to see the details.  

    > Notes:
    >
    > If you run a Test Suite for the first time, there is no baseline image.

## Configure a baseline image

You can set up a baseline image to compare it with the screenshot of the next Test Run.

Follow these steps:

1. Select a screenshot to see the details.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-july-visual-testing/id-1-sample-visual-testing.png" width=100% alt="id1 sample visual testing image">

2. Select the *Passed* or *Failed* icon at the top right corner of a screenshot, then close the screenshot.

    An *Unsaved* label now appears on the **Checkpoints** page.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-july-visual-testing/id-1-unsaved-appears.png" width=100% alt="id1 result page with save to baseline button">

3. Go to the **Results** page.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-july-visual-testing/id-1-save-to-base-line-button.png" width=100% alt="id4 highlight unresolved status">

4. Click **Save to baseline**.

> Notes:
>
> If you run a Test Suite for the first time and the Test Suite has passed, the screenshots are automatically marked as *Passed* and there is no **Save to baseline** button. You can open a screenshot and click on the *Failed* icon, then switch back to *Passed* so that the **Save to baseline** button appears.

### View baseline information

To see the baseline images you have saved, go to **Reports & Analytics** > **Visual Testing** > **Visual Baselines**, then select a screenshot for **Baseline information**.

### Unresolved images

If you run the Test Suite again and the new screenshots of this test execution are different from the baseline images, the status of this Test Run is then marked as *Unresolved*.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-july-visual-testing/visual-testing-page-id-4-unresolved.png" width=100% alt="id4 unresolved status">

To resolve the issues, follow these steps:

1. Click on the ID of the unresolved Test Run.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-july-visual-testing/test-run-id-4-result-page-1.png" width=100% alt="id4 results page">

2. Select a screenshot.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-july-visual-testing/show-diff-button.png" width=100% alt="id4 mismatch show diff button">

    For mismatched screenshots, the new screenshot (on the right) is compared with the baseline image (on the left). 

3. Click **Show diff** to see the differences between two images (the differences are highlighted in red).

4. Select the *Passed* or *Failed* icon to resolve.

    > Notes:
    >
    > * The *Unsaved* label appears whenever you change the status (*Passed* or *Failed*) of a screenshot. If you click **Save to baseline**, the new *Passed* screenshots replace the older baseline images. Katalon TestOps then compares between the new baseline images and screenshots of the next Test Runs.
