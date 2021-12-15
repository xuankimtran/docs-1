---
title: "Configure Key Bindings"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/configure-keyboard-shortcuts.html
redirect_from:
description: "How to configure keybinding (keyboard shortcuts) in Katalon Studio"
---

Katalon Studio provides different key binding schemes that contain predefined keyboard shortcuts. You can select a scheme and customize the shortcuts to optimize your workflow.

This guide shows you how to configure a key binding scheme and export the scheme into an external file.

## Configure a Key Binding Scheme

To configure a key binding scheme, follow these steps:

1. Open Katalon Studio. From the main menu, go to **Window > Katalon Studio Preferences > General > Keys**.

    The **Keys** dialog displays details about commands and the associated keyboard shortcuts of a scheme as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/configure-keybinding/KS-Keys-dialog.png" alt="Keys dialog" width=70%>

2. To select a key binding scheme, click on the **Scheme** dropdown button and select a scheme. 

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/configure-keybinding/KS-Scheme-dropdown-button.png" alt="Select a scheme" width=70%>

    Katalon Studio supports the following schemes:

    <table>
        <thead>
            <tr>
                <th><b>Key binding Scheme</b></th>
                <th><b>Description</b></th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td><b>Default</b></td>
                <td>The Katalon Studio's default key binding scheme.</td>
            </tr>
            <tr>
                <td><b>Emacs</b></td>
                <td>A key binding scheme that includes Emacs editor's keyboard shortcuts.</td>
            </tr>
        </tbody>
    </table>

3. To edit the key binding of a command, select the command, then specify the details in the section below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/configure-keybinding/KS-edit-a-command.png" alt="Select a command and edit" width=70%>

    <table>
        <thead>
            <tr>
                <th><b>Section</b></th>
                <th><b>Description</b></th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td><b>Description</b></td>
                <td>The description about the command.</td>
            </tr>
            <tr>
                <td><b>Binding</b></td>
                <td>The key binding (keyboard shortcut) for the command.</td>
            </tr>
            <tr>
                <td><b>When</b></td>
                <td>The context when the command can be executed.</td>
            </tr>
            <tr>
                <td><b>Conflicts</b></td>
                <td>Commands that have the same combination of key binding and context.</td>
            </tr>
        </tbody>
    </table>

    > **Notes**:
    >
    > To avoid conflicts with keyboard shortcuts, verify that the configured command's combination of key binding and context is unique.

4. Click on the **Apply** button to save and apply the configuration.

## Export the Key Binding Scheme

Katalon Studio supports exporting a key binding scheme into a CSV file for better viewing.

To export a scheme, in the **Keys** dialog, click on the **Export CSV** button.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/configure-keybinding/KS-Export CSV.png" alt="Select a command and edit" width=70%>

The selected key binding scheme is then exported into a CSV file.
