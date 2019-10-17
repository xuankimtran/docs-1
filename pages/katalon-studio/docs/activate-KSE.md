---
title: "Activate Katalon Studio Enterprise"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/activate-KSE.html
redirect_from:
    - "/katalon-studio/docs/katalon-studio-activation-since-70.html#activating-katalon-studio-enterprise"
    - "/katalon-studio/docs/katalon-studio-activation-since-70.html#other-options"
    - "/katalon-studio/docs/katalon-studio-activation-since-70.html#activating-katalon-studio-enterprise-trial-license"
description:
---
You need a license to activate Katalon Studio Enterprise that can work without an Internet connection. A machine ID is required for generating a license. In Katalon Studio Activation pop-up window, click **Activate Katalon Studio Enterprise**:

1. Generate a license: To generate a license in Katalon TestOps, access your organization, navigate to the **License** tab, insert a **Machine ID**, then click **Create**.

2. Locate the generated license: To use a license, click the **Download** button, the license will be downloaded as a `license.lic` file. Then click **Choose file** in **Product Offline Activation** to locate the downloaded license file.

3. Click **Activate**.

### Other options

After activating Katalon Studio Enterprise, there will be a pop-up window requiring you to log in to your Katalon account for connecting to [Katalon TestOps](https://docs.katalon.com/katalon-studio/docs/katalon-analytics-beta-integration.html) and [Store](https://docs.katalon.com/katalon-store/docs/overview.html).

Currently, the Katalon Studio Enterprise users can use [private plugins](https://docs.katalon.com/katalon-studio/docs/private-plugins.html) as an alternative option of using plugins from Katalon Store.

Regarding TestOps, there is no on-premises version; hence, the automatically generated [JUnit reports](https://docs.katalon.com/katalon-studio/docs/export-test-results-in-junit-format.html), and the [basic report plugin](https://docs.katalon.com/katalon-studio/docs/basic-report.html) can be a substitute for TestOps.

### Activating Katalon Studio Enterprise with a trial license

You need to generate a trial license for Katalon Studio Enterprise before activating it. Each trial license of Katalon Studio Enterprise  is bound to each machine.

1. Navigate to your [Katalon TestOps profile](https://analytics.katalon.com/organization/18274/license_keys).

> Notes: Only the organizational owner can access an organizational profile.

2. Select the **License** tab, enter a machine ID to create a trial license for it. Download the newly created license.

> Notes: **Machine ID** is granted for each computer installing Katalon Studio. In Katalon Studio Activation pop-up window, click **Activate Katalon Studio Enterprise**, you can view and copy your machine ID.

3. In **Activate Katalon Studio Enterprise** pop-up dialog,  locate the license file you have just downloaded in step 2. Click **Activate**.

### Activating in Console mode

You need a license key that grants you permission to run Katalon Studio from the command line. Before executing Katalon Studio, call the license key by the command-line argument as follows: `licenseFile= [the path to the license key file]`.

For example:
`licenseFile=C:\Users\demokatalon\licensefile\license-window.lic`.
