---
title: "Configure Proxy"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/configure-proxy.html
redirect_from:
description:
---

In this tutorial, you can learn how to configure a proxy if you are behind a proxy server.

To learn more about how to activate Katalon licenses, see [Activate Katalon License](https://docs.katalon.com/katalon-studio/docs/activate-KSE.html).

### Configure proxy

If you are behind a proxy server, before activating Katalon licenses, you need to configure the Authentication proxy settings.

1. Open Katalon Studio. In the toolbar, click on the _Profile_ button and select **Deactivate**. You will be logged out of your current account, and the **Katalon Studio Activation** dialog appears.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/activate-KSE/activation.png" alt="activation" width=70%>

    > Notes:
    >
    > If you download Katalon Studio for the first time or are not logged in to any account in Katalon Studio, when you open Katalon Studio, the **Katalon Studio Activation** automatically pops up.

2. Click **Configure Authentication Proxy** at the bottom of the Activation dialog box.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/proxy-preferences/config-proxy-activation.png" width="">

    In the Proxy Settings dialog box, you can select one of the three options below.

    * **Use system proxy configuration**: Katalon Studio automatically syncs with the proxy server behind your system.
    * **No proxy**: There's no proxy.
    * **Manual proxy configuration**: You can manually set up your proxy.

> Notes:
>
> If you are using a private network, you might encounter a situation where you fail to execute test scripts or integrate Katalon Studio due to the network security error. To fix this problem, whitelist the following domains:
>
> * store.katalon.com
> * update.katalon.com
> * analytics.katalon.com
> * testops.katalon.io
> * admin.katalon.com
> * katalon-test.s3-accelerate.amazonaws.com (used for uploading reports to [Katalon TestOps](https://analytics.katalon.com))