---
title: "How to use self-healing" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-recorder/docs/how-to-use-self-healing.html 
description: 
---

On some websites, automation scripts can fail because the default locator fails to find an element. In that case, self-healing will automatically try out other locators. If it finds a valid locator, it will continue the automation script using that locator and records the broken and valid locators for later use.

## Enabling and Disabling self-healing

**By default, self-healing is enabled, so there’s nothing you have to do to use it.**

You can disable it by following these steps:

1.  Go to Settings > Self-healing.    
2.  Uncheck **Enable self-healing execution**.    
3.  Save and close.
    


## Prioritizing locator methods in self-healing

Self-healing comes pre-configured with three types of locator methods: **id**, **css**, **xpath**, in that particular order which follows the industry's best practices. However, depending on your websites, the best locator methods may vary case by case.

You can change the order of locator methods that self-healing will use during playback:

1.  Go to Settings > Self-healing.    
2.  Make sure self-healing is enabled.    
3.  Drag and drop the locator methods to prioritize them.    
4.  Save and close.
    

## Excluding certain commands from self-healing

There are some commands that validates the existence of a particular element. You do not want to trigger self-healing on these commands because the risk of validating a wrong element outweighs any benefit.

You can choose to exclude certain commands from self-healing:

1.  Go to Settings > Self-healing.
2.  Make sure self-healing is enabled.    
3.  Add the commands you want to exclude to the list.    
4.  Save and close.
    

By default, **verifyElementPresent**, **verifyElementNotPresent**, **assertElementPresent** and **assertElementNotPresent** commands are excluded from self-healing.

Regex is also supported for excluding commands. For example, you can exclude all command starting with the keyword **waitFor** by adding **^waitFor** to the list.

## Approving self-healing proposals

After automation scripts are finished, you can go to the Self-healing tab to see the self-healing proposals. A self-healing proposal consists of a broken locator, the script in which the broken locator is found, the script's status and a proposed locator.


> Self-healing tab will be refreshed on every new execution

To approve self-healing proposals:

1.  Go to Self-healing tab.    
2.  Select the proposed locators using the status filter.    
3.  Press **Approve**.