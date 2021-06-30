---

title: "Use the Self-Healing function"
sidebar: katalon_studio_docs_sidebar
permalink: /katalon-recorder/docs/self-healing.html
redirect_from:
description:
---
On some websites, automation scripts can fail because the default locator fails to find an element. In that case, Self-Healing will automatically try out other locators. If it finds a valid locator, it will continue the automation script using that locator and records the broken and valid locators for later use.

## Enabling and disabling Self-Healing

Self-healing is enabled by default.

You can disable it by following these steps:

1. Go to **Settings > Self-Healing**.

2. Uncheck **Enable Self-Healing execution**.

3. Save and close.

Screenshot placeholder. Use html syntax.

## Prioritizing locator methods in Self-Healing

Self-Healing uses 3 locator methods, in this priority order: **id**, **css**, **xpath**. However, the best locator methods may vary depending on your websites under test.

You can change the order of locator methods by following these steps:

1. Go to **Settings > Self-Healing**.

2. Make sure Self-Healing is enabled.

3. Drag and drop the locator methods in the order of your choosing.

4. Save and close.

## Excluding certain commands from Self-Healing

>Notice:
>
>Some commands validate that a particular element exists on a certain page. We advise you to not trigger Self-Healing on these commands, as it encurs the risk of validating elements incorrectly.
>
>By default, `verifyElementPresent`, `verifyElementNotPresent`, `assertElementPresent` and `assertElementNotPresent` commands are excluded from Self-Healing.

You can choose to exclude certain commands from Self-Healing by following these steps:

1. Go to **Settings > Self-Healing**.

2. Make sure Self-Healing is enabled.

3. Add the commands you want to exclude to the list.

4. Save and close.

>Notes:
>
>Regex is also supported for excluding commands. For example, you can exclude all command starting with the keyword **waitFor** by adding **^waitFor** to the list.

## Approving Self-Healing proposals

When the default locator fails, Self-Healing finds alternative locators to complete the test execution. After the test execution is completed, you can choose to replace failing locators by approving Self-Healing suggestions.

Screenshot placeholder

The Self-Healing tab is refreshed on every new execution.

To approve Self-healing suggestions, folow these steps:

1. Go to the Self-Healing tab.

2. Select the suggested locators using the status filter.

3. Press **Approve**.

Screenshot placeholder
