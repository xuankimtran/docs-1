---
title: "How to transfer an online Node-locked Runtime Engine license from one machine to another"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/transfer-license.html
description:
---
An online Node-locked Runtime Engine license, when activated, binds to a machine until expired or manually removed from that machine. For other members in your organization to use an online Node-locked Runtime Engine, you must remove it from your machine.

> Only **online licenses** are transferable.
>
> **Offline licenses** cannot be transferred until expired (60 days).

## Get the ID of your machine

Open **Katalon Studio** on your machine, and deactivate (log out). 

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/transfer-license/1-deactivate.png)

You should see the **Activation Dialog**. 

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/transfer-license/2-machine-id.png)

Click on **Offline Activation**, you will be directed to a dialog where you click on copy to copy your **Machine ID** into clipboard.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/transfer-license/3-license-file.png)

Store this **Machine ID** somewhere (text editor). You can now safely log in back into **Katalon Studio**.


## Verify that the machine does not have an offline license

Visit **Katalon TestOps** > **Organization** > **License**, navigate to tab **Runtime Engine**. You should not see your Machine ID in step 1 listed under **Offline Licenses**. 


If you do see it, then it means this machine already has an offline license. You won’t be able to remove an offline license from the machine until the license is expired or 60 days have passed. In this case, this guide is not for you. 

If you do not see your **Machine ID** listed there, then please continue.


## Remove an online Node-locked Runtime Engine license from a machine

At the bottom of the same page, you should see under Registered Machines, the **Machine ID** (step 1) There is a button to remove it from the list.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/transfer-license/4-delete-machine-id.png)

You will be asked to provide confirmation.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/transfer-license/5-confirm.png)

Once you confirm, the **Machine ID** will be removed from the Registered Machines.

> As soon as you remove the **Machine ID** from **Katalon TestOps**, **Katalon Studio** will be deactivated in that machine.


## Use the online Node-locked Runtime Engine license on another machine

Now you can use the license for Runtime Engine on another machine.