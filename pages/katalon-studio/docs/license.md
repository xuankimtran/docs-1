---
title: "Types of Licenses"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/license.html
description:
---

> Starting from **version 7.0.0**, you need a license to activate and use one of the Katalon Studio products, including Katalon Studio Enterprise (KSE), Katalon Studio (KS), and Katalon Runtime Engine (KRE).

This section provides information on the licensing system of Katalon. You will find a description of Katalon products and their available license types.

## Katalon Studio Enterprise

Katalon Studio provides free, basic tools suitable for the testing needs of individuals. For an advanced business solution, consider purchasing Katalon Studio Enterprise licenses. For feature comparison between KS and KSE, see [Katalon Studio vs Katalon Studio Enterprise Features](https://docs.katalon.com//katalon-studio/docs/katalon-studio-vs-katalon-studio-enterprise.html).

One KSE license is exclusively assigned to one Katalon account and can be activated/used on one machine at a time. Licenses are transferable. You need an internet connection to activate and validate licenses, although special rules apply to enable offline activation. See: [Create an offline license](https://docs.katalon.com/katalon-studio/docs/use-online-license.html#create#an#offline#license).

## Katalon Runtime Engine

Katalon Runtime Engine (KRE) is the test execution add-on of Katalon Studio. While the KSE license only supports you in generating test scripts and manually executing tests via the graphical user interface, the KRE license allows you to execute automation tests in the command-line interface (CLI) mode.

When running from the CLI, one working session accounts for one license. To learn more about the use cases of KRE, see [Introduction to Katalon Runtime Engine](https://docs.katalon.com/katalon-studio/docs/intro-RE.html).

## License types

There are two types of licenses for KSE and KRE: node-locked and floating. Depending on the size, composition, and work requirements of your team, you can choose to purchase node-locked licenses, floating licenses, or a mix of both.

<table>
	<tbody>
		<tr>
			<td><strong>Node-locked license</strong></td>
			<td><strong>Floating license</strong></td>
		</tr>
		<tr>
			<td>
				<p>One license is assigned to one machine ID.</p>
			</td>
			<td>One license is assigned to one parallel execution session and can be shared between 3 machines.</td>
		</tr>
		<tr>
			<td>
				<p>Licenses are transferable.</p>
			</td>
			<td>Licenses need to be assigned.</td>
		</tr>
		<tr>
			<td>
				<p>Applies to local desktops or workstations with fixed hardware specifications.</p>
			</td>
			<td>&nbsp;Applies to all types of execution environments.</td>
		</tr>
		<tr>
			<td>
				<p>Online subscription available.</p>
			</td>
			<td>Online subscription available.</td>
		</tr>
		<tr>
			<td>
				<p>Offline licenses can be generated from online node-locked licenses.</p>
			</td>
			<td>Offline licenses are available for on-premises licensing server only. For more information, <a href="https://www.katalon.com/book-a-demo/">contact sales</a>.</td>
		</tr>
	</tbody>
</table>

### Node-Locked License

This license type is applied to local desktops or workstations with fixed hardware specifications (machine-blocked license), such as:

* A virtual machine with a fixed machine ID
* A physical machine

With node-locked licenses, one machine running tests = one license.

* A license is tied to a single machine ID and only for one execution session at a time.
* A machine can be mapped to multiple licenses if needed.
* For machines connected to the internet, the licenses can be transferred to other machines at no cost and as many times as needed.
* For _annual licenses_ only: Licenses can be converted to be used in an offline environment. Once converted, the license cannot be transferred to another machine until it is expired.
* Licenses purchased on a monthly basis cannot be converted for use in an offline environment.

### Floating License

For scaling teams with dynamic usage, floating licenses reduce the management cost and optimize your workflow.

This license type is applied to all types of execution environments, including cloud or virtual machines with dynamic hardware specifications (to execute tests in Docker, Azure, AWS).

* One floating license can be shared across a maximum of 3 machines.
* One floating license is assigned to one parallel execution session at a time.

For instance, you have 1 floating Katalon Studio Enterprise license attached to the email example@katalon.com.

You can use example@katalon.com to log in to Katalon Studio and enjoy all of the Enterprise level features on 3 different machines. You will not be able to do so on additional machines.

However, this email represents only 1 floating Katalon Studio Enterprise license. This means you can only be active on 1 of those 3 machines at any time.