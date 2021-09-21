---
title: "Roles and permissions" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/testops-roles-privileges.html 
description: 
---

In Katalon TestOps, each role's privileges vary at the organization level.
 
You can find the detailed permissions for each role in the following table:

<table>
	<tbody>
		<tr>
			<td rowspan="2">
				<p><strong>Roles</strong></p>
			</td>
			<td colspan="4">
				<p><strong>Permissions</strong></p>
			</td>
		</tr>
		<tr>
			<td>
				<p><strong>Organization Management</strong></p>
			</td>
			<td>
				<p><strong>Subscription Management</strong></p>
			</td>
			<td>
				<p><strong>User Management</strong></p>
			</td>
			<td>
				<p><strong>License Management</strong></p>
			</td>
		</tr>
		<tr>
			<td>
				<p><strong>Owner</strong></p>
			</td>
			<td rowspan="2">
				<ul>
					<li>Set Organization Name</li>
					<li>Customize Domain Name</li>
					<li>Enable and configure SSO Settings</li>
					<li>Configure IP Address Restrictions</li>
					<li>Configure Session Timeout</li>
					<li>Enable Katalon Studio Integration for reports upload</li>
					<li>Enable Strict Domain</li>
					<li>Delete Organization</li>
				</ul>
			</td>
			<td>
				<ul>
					<li>Get Quote</li>
					<li>Checkout on Katalon TestOps</li>
				</ul>
			</td>
			<td>
				<ul>
					<li>Invite new users</li>
					<li>Remove users</li>
					<li>Set roles &amp; product access for:&nbsp;</li>
					<ul>
						<li>Admin</li>
						<li>User</li>
						<li>Billing Manager&nbsp;</li>
					</ul>
					<li>Transfer Organization ownership to another member</li>
				</ul>
			</td>
			<td rowspan="2">
				<ul>
					<li>View subscription information</li>
					<li>Add/remove users from licenses</li>
					<li>View/delete the Online Licenses list</li>
					<li>Create/view/delete the Offline Licenses list</li>
					<li>View/delete the registered machines</li>
				</ul>
			</td>
		</tr>
		<tr>
			<td>
				<p><strong>Admin</strong></p>
			</td>
			<td>
				<ul>
					<li>Checkout on Katalon TestOps if there is no predefined Payment Method from Get Quote email</li>
				</ul>
			</td>
			<td>
				<ul>
					<li>Invite new users</li>
					<li>Remove users</li>
					<li>Set roles &amp; product access for:</li>
					<ul>
						<li>Admin</li>
						<li>User</li>
					</ul>
				</ul>
			</td>
		</tr>
		<tr>
			<td>
				<p><strong>Billing Manager</strong></p>
			</td>
			<td>
				<p>No access</p>
			</td>
			<td>
				<ul>
					<li>Get Quote</li>
					<li>Checkout on Katalon TestOps</li>
					<li>Checkout via Recurly</li>
				</ul>
			</td>
			<td>
				<p>No access</p>
			</td>
			<td>
				<ul>
					<li>View subscription information</li>
				</ul>
			</td>
		</tr>
		<tr>
			<td>
				<p><strong>User</strong></p>
			</td>
			<td>
				<p>No access</p>
			</td>
			<td>
				<p>No access</p>
				<br />
				<p>* Notes: If a user receives the Get Quote email (from Owner for example), the user can still have access to the link to subscribe and checkout on Katalon TestOps. However, this is only applicable if there is no predefined Payment Method.</p>
			</td>
			<td>
				<p>No access</p>
			</td>
			<td>
				<p>No access</p>
			</td>
		</tr>
	</tbody>
</table>