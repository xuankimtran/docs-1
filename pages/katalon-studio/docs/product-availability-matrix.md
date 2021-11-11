--- 
title: "Supported Technologies" 
sidebar: katalon_studio_docs_sidebar 
permalink: /katalon-studio/docs/product-availability-matrix.html 
redirect_from:

	- "/katalon-studio/docs/unique-capabilities.html"
--- 

This document gives you information on the supported technologies and integrations. For the supported environments (including browsers and operating systems), see [supported environments](https://docs.katalon.com/katalon-studio/docs/supported-environments.html). 

### Supported Application Under Test (AUT)

<table id="top" class="top-vertical-align-table" width="100%">
<tbody>
<tr>
<td style="width: 50%;"><strong>Web UI</strong>
<ul>
<li>Support all front-end frameworks: ReactJS, AngularJS, VueJS.</li>
<li>Cross-browser compatibility: Chrome, Firefox, Safari, Edge</li>
</ul>
</td>
<td><strong>Mobile</strong>
<ul>
<li>Android &amp; iOS</li>
<li>Native application</li>
<li>Web mobile</li>
<li>Hybrid (*)</li>
</ul>
</td>
</tr>
<tr>
<td style="width: 50%;"><strong>API</strong>
<ul>
<li>REST: <a href="https: //docs.katalon.com/katalon-studio/docs/import-rest-requests-from-swagger-20.html"> Swagger</a>,<a href="https://docs.katalon.com/katalon-studio/docs/import-openapi30.html"> OpenAPI 3.0</a> &amp;<a href="https://docs.katalon.com/katalon-studio/docs/import-wadl.html"> WADL</a></li>
<li>SOAP (SOAP 1.1 &amp; 1.2)</li>
<li>Authentication: <a href="https://docs.katalon.com/katalon-studio/docs/authorization-basic.html">Basic</a>, <a href="https://docs.katalon.com/katalon-studio/docs/authorization-oauth1.html">OAuth 1.0</a> &amp;<a href="https://docs.katalon.com/katalon-studio/docs/authorization-oauth2.html"> OAuth 2.0</a></li>
</ul>
</td>
<td style="width: 50%;"><strong>Windows</strong>
<ul>
<li>Universal Windows Platform (UWP)</li>
<li>Windows Forms (WinForms)</li>
<li>Windows Presentation Foundation (WPF)</li>
<li>Classic Windows (Win32) apps on Windows 10 PCs</li>
</ul>
</td>
</tr>
</tbody>
</table>
(*) <em> Limitations: Elements inside embedded web views cannot be captured automatically by Record&amp;Spy utilities. </em>

### Programming Skill & Language

<table width="100%">
<tbody>
<tr>
<td>
<p>Low-code</p>
</td>
<td>
<p>Rich set of utilities to generate and maintain automated script without programming experience.</p>
</td>
</tr>
<tr>
<td>
<p>Groovy</p>
</td>
<td>
<p>v2.4.x+</p>
</td>
</tr>
<tr>
<td>
<p>Java</p>
</td>
<td>
<p>From Java 8 (Java 1.8) onwards</p>
</td>
</tr>
</tbody>
</table>

### Testing Methodologies

<table width="100%">
	<tbody>
		<tr>
			<td rowspan="4">
				<p><a href="https://docs.katalon.com/katalon-studio/docs/ddt.html">Data-driven testing - DDT</a></p>
			</td>
			<td>
				<p><strong>Built-in Database</strong></p>
			</td>
			<td>
				<p><strong>Version</strong></p>
			</td>
			<td>
				<p><strong>Katalon Studio Versions</strong></p>
			</td>
			<td>
				<p><strong>Katalon Studio Enterprise Versions</strong></p>
			</td>
		</tr>
		<tr>
			<td>
				<p>PostgreSQL</p>
			</td>
			<td>
				<p data-pm-slice="1 1 [&quot;bulletList&quot;,null,&quot;listItem&quot;,null,&quot;bulletList&quot;,null,&quot;listItem&quot;,null]">v42.2.17</p>
			</td>
			<td>
				<p>v7.0.0+</p>
			</td>
			<td>
				<p>v7.0.0+</p>
			</td>
		</tr>
		<tr>
			<td>
				<p>Oracle SQL</p>
			</td>
			<td>
				<p data-pm-slice="1 1 [&quot;bulletList&quot;,null,&quot;listItem&quot;,null,&quot;bulletList&quot;,null,&quot;listItem&quot;,null]">v12.1.0.2</p>
			</td>
			<td>Not supported</td>
			<td>
				<p>v7.0.0+</p>
			</td>
		</tr>
		<tr>
			<td>
				<p data-pm-slice="1 1 [&quot;bulletList&quot;,null,&quot;listItem&quot;,null,&quot;bulletList&quot;,null,&quot;listItem&quot;,null]">SQL Server</p>
			</td>
			<td>
				<p data-pm-slice="1 1 [&quot;bulletList&quot;,null,&quot;listItem&quot;,null,&quot;bulletList&quot;,null,&quot;listItem&quot;,null]">v6.2.2</p>
			</td>
			<td>Not supported</td>
			<td>
				<p>v7.0.0+</p>
			</td>
		</tr>
		<tr>
			<td colspan="3">
				<p><a href="https://docs.katalon.com/katalon-studio/docs/cucumber-features-file.html">Behavior-driven development - BDD</a></p>
			</td>
			<td>
				<p>v7.0.0+</p>
			</td>
			<td>
				<p>v7.0.0+</p>
			</td>
		</tr>
		<tr>
			<td colspan="3">
				<p>Keyword-driven testing - KDT</p>
			</td>
			<td>
				<p>v7.0.0+</p>
			</td>
			<td>
				<p>v7.0.0+</p>
			</td>
		</tr>
		<tr>
			<td colspan="3">
				<p>Page Object Model - POM</p>
			</td>
			<td>
				<p>v7.0.0+</p>
			</td>
			<td>
				<p>v7.0.0+</p>
			</td>
		</tr>
	</tbody>
</table>

### Testing Capabilities

<table>
	<tbody>
		<tr>
			<td><strong>Testing Capabilities</strong></td>
			<td><strong>Supported Katalon Studio versions</strong></td>
		</tr>
		<tr>
			<td>
				<p>Integration Testing</p>
			</td>
			<td>v7.8.0+</td>
		</tr>
		<tr>
			<td>
				<p>Functional Testing</p>
			</td>
			<td>v7.8.0+</td>
		</tr>
		<tr>
			<td>
				<p>E-2-E Testing</p>
			</td>
			<td>v7.8.0+</td>
		</tr>
		<tr>
			<td>
				<p><a href="https://github.com/katalon-studio-samples/web-visual-testing-samples">Visual Testing</a></p>
			</td>
			<td>v7.8.0+</td>
		</tr>
	</tbody>
</table>

### Unique Capabilities

<table style="width: 797.875px;">
	<tbody>
		<tr>
			<td style="width: 132px;"><strong>Unique Capabilities</strong></td>
			<td style="width: 521px;"><strong>Description</strong></td>
			<td style="width: 121.875px;"><strong>Supported Katalon Studio versions</strong></td>
		</tr>
		<tr>
			<td style="width: 132px;">
				<p>Application Under Test (AUT) Testing Combination</p>
			</td>
			<td style="width: 521px;">Katalon Studio allows combining multiple application types (Web UI, API, Mobile &amp; Desktop) in one project and execution flow. You can test this capability with our Github sample project <a title="https://github.com/katalon-studio-samples/api-web-combination-sample/tree/master" href="https://github.com/katalon-studio-samples/api-web-combination-sample/tree/master" data-renderer-mark="true">here</a>.</td>
			<td style="width: 121.875px;">v7.0.0+</td>
		</tr>
		<tr>
			<td style="width: 132px;">
				<p>Dual-editor interface</p>
			</td>
			<td style="width: 521px;">Katalon Studio test scripts are interchangeable between two interfaces: manual and scripting editors. This enables a team with a mixed level of automation testing skills to work effectively and efficiently in the same project.</td>
			<td style="width: 121.875px;">v7.0.0+</td>
		</tr>
		<tr>
			<td style="width: 132px;">
				<p>Self-healing</p>
			</td>
			<td style="width: 521px;">The <strong>Self-healing</strong> mechanism is to tackle the issue of broken locators during execution to reduce the test maintenance effort.&nbsp;<a title="Self-healing" href="https://docs.katalon.com/katalon-studio/docs/self-healing.html">Learn more</a>.</td>
			<td style="width: 121.875px;">v7.6.0+</td>
		</tr>
		<tr>
			<td style="width: 132px;">
				<p>Smart Wait</p>
			</td>
			<td style="width: 521px;">The <strong>Smart Wait</strong> function tells the WebDriver to wait for the web page to become static before performing any operations. This reduces the risks of test failures caused when the page hasn't fully loaded. <a href="https://docs.katalon.com/katalon-studio/docs/webui-smartwait.html#sample-tests">Learn more</a>.</td>
			<td style="width: 121.875px;">v7.0.0+</td>
		</tr>
		<tr>
			<td style="width: 132px;">
				<p>Time Capsule</p>
			</td>
			<td style="width: 521px;">This capability enables users to restore the Application Under Test to the state when the test fails due to locators not finding Web UI objects. <a href="https://docs.katalon.com/katalon-studio/docs/time-capsule.html">Learn more</a>.</td>
			<td style="width: 121.875px;">v7.8.0+</td>
		</tr>
	</tbody>
</table>


### Report

<table>
	<tbody>
		<tr>
			<td><strong>Types of Reports</strong></td>
			<td><strong>Supported Katalon Studio versions</strong></td>
		</tr>
		<tr>
			<td>
				<p><a href="https://docs.katalon.com/katalon-studio/docs/test-suite-report.html#export-reports-to-other-formats">HTML, PDF, CSV</a></p>
			</td>
			<td>v7.0.0+</td>
		</tr>
		<tr>
			<td>
				<p><a href="https://docs.katalon.com/katalon-studio/docs/execution-settings.html#emails-settings">Dynamic email configuration</a></p>
			</td>
			<td>v7.5.0+</td>
		</tr>
		<tr>
			<td>
				<p><a href="https://docs.katalon.com/katalon-studio/docs/record-screen-based-videos.html#configure-screen-based-recorder">Release/build-based reports</a></p>
			</td>
			<td>v7.8.0+</td>
		</tr>
		<tr>
			<td>
				<p><a href="https://docs.katalon.com/katalon-studio/docs/view-execution-list.html#prerequisites">Performance, Trending &amp; Insights reports</a>&nbsp;(*)</p>
			</td>
			<td>v7.6.2+</td>
		</tr>
	</tbody>
</table>
(*) <em> Requirements: Katalon TestOps integration. </em>

### Cloud Device Integration

<table>
	<tbody>
		<tr>
			<td><strong>Product</strong></td>
			<td><strong>Supported Katalon Studio versions</strong></td>
		</tr>
		<tr>
			<td>
				<p><a href="https://docs.katalon.com/katalon-studio/docs/integrate_with_kobiton.html#enable-kobiton-integration">Kobiton</a></p>
			</td>
			<td>v7.0.1+</td>
		</tr>
		<tr>
			<td>
				<p><a href="https://docs.katalon.com/katalon-studio/docs/saucelabs-plugin.html">Sauce Labs</a></p>
			</td>
			<td>v7.0.0+</td>
		</tr>
		<tr>
			<td>
				<p><a href="https://docs.katalon.com/katalon-studio/docs/browserstack-integration.html">Browserstack</a></p>
			</td>
			<td>v7.0.0+</td>
		</tr>
		<tr>
			<td>
				<p><a href="https://docs.katalon.com/katalon-studio/docs/lambdatest-integration.html">LambdaTest</a></p>
			</td>
			<td>v7.8.0+</td>
		</tr>
		<tr>
			<td>
				<p><a href="https://docs.katalon.com/katalon-studio/docs/introduction-to-desired-capabilities.html#remote-server">Custom integration</a></p>
			</td>
			<td>v7.0.0+</td>
		</tr>
	</tbody>
</table>

### ALM Integration

<table>
	<tbody>
		<tr>
			<td><strong>Products</strong></td>
			<td>
				<p><strong>Supported Katalon Studio versions</strong></p>
			</td>
		</tr>
		<tr>
			<td>
				<p><a href="https://docs.katalon.com/katalon-studio/docs/jira-integration.html">Jira</a></p>
			</td>
			<td>v7.0.0+</td>
		</tr>
		<tr>
			<td>
				<p><a href="https://docs.katalon.com/katalon-studio/docs/git-integration.html">Git</a></p>
			</td>
			<td>v7.0.0+</td>
		</tr>
		<tr>
			<td>
				<p><a href="https://docs.katalon.com/katalon-studio/docs/qtest-integration.html">qTest</a></p>
			</td>
			<td>v7.0.0+</td>
		</tr>
		<tr>
			<td>
				<p><a href="https://docs.katalon.com/katalon-studio/docs/testrail-integration.html">TestRail</a></p>
			</td>
			<td>v7.6.5+</td>
		</tr>
		<tr>
			<td>
				<p><a href="https://docs.katalon.com/katalon-studio/docs/rally-integration.html">Rally</a></p>
			</td>
			<td>v7.0.0+</td>
		</tr>
		<tr>
			<td>
				<p><a href="https://docs.katalon.com/katalon-studio/docs/testlink-integration.html">TestLink</a></p>
			</td>
			<td>v7.0.0+</td>
		</tr>
		<tr>
			<td>
				<p><a href="https://docs.katalon.com/katalon-store/docs/publisher/example-plugin-testrail.html">Custom ALM integration</a></p>
			</td>
			<td>v7.0.0+</td>
		</tr>
	</tbody>
</table>

### CI/CD Integration

<table width="70%">
	<tbody>
		<tr>
			<td><strong>Products</strong></td>
			<td>
				<p><strong>Versions</strong></p>
			</td>
			<td>
				<p><strong>Supported Katalon Studio versions</strong></p>
			</td>
		</tr>
		<tr>
			<td>
				<p><a href="https://docs.katalon.com/katalon-studio/docs/jenkins-integration-overview.html">Jenkins</a></p>
			</td>
			<td>
				<p></p>
			</td>
			<td>
				<p>v7.8.0+</p>
			</td>
		</tr>
		<tr>
			<td>
				<p><a href="https://docs.katalon.com/katalon-studio/docs/azure-devops-integration.html">Azure DevOps Pipeline</a></p>
			</td>
			<td></td>
			<td>v8.0.0+</td>
		</tr>
		<tr>
			<td>
				<p><a href="https://docs.katalon.com/katalon-studio/docs/integration-circleci.html#setup-and-configuration">CircleCI</a></p>
			</td>
			<td>
				<p></p>
			</td>
			<td>
				<p>v7.8.0+</p>
			</td>
		</tr>
		<tr>
			<td>
				<p><a href="https://marketplace.atlassian.com/apps/1220235/katalon-testops-for-bamboo/version-history">Bamboo</a></p>
			</td>
			<td>
				<p>Bamboo Server v6.0.0+</p>
			</td>
			<td>
				<p>v7.8.0+</p>
			</td>
		</tr>
		<tr>
			<td>
				<p><a href="https://plugins.jetbrains.com/plugin/12653-katalon-studio-runner/versions">TeamCity</a></p>
			</td>
			<td>
				<p></p>
			</td>
			<td>
				<p>v7.8.0+</p>
			</td>
		</tr>
		<tr>
			<td>
				<p><a href="https://docs.katalon.com/katalon-studio/docs/katalon-studio-github-action.html">Katalon Studio Github Action</a></p>
			</td>
			<td>
				<p></p>
			</td>
			<td>
				<p>v7.8.0+</p>
			</td>
		</tr>
	</tbody>
</table>

### Integration with other Katalon products and extensions

<table width="70%">
	<tbody>
		<tr>
			<td>
				<p><strong>Products</strong></p>
			</td>
			<td>
				<p><strong>Supported Katalon Studio versions</strong></p>
			</td>
		</tr>
		<tr>
			<td>
				<p><a href="https://docs.katalon.com/katalon-recorder/docs/export-test-project-to-ks.html#export-to-katalon-studio">Katalon Recorder</a></p>
			</td>
			<td>v7.8.0+</td>
		</tr>
		<tr>
			<td>
				<p><a href="https://docs.katalon.com/katalon-studio/docs/katalon-analytics-beta-integration.html#upload-test-results-automatically">Katalon TestOps</a></p>
			</td>
			<td>v7.0.0+</td>
		</tr>
	</tbody>
</table>

### Migration from other tools

<table>
	<tbody>
		<tr>
			<td>
				<p><strong>Tools</strong></p>
			</td>
			<td>
				<p><strong>Supported Katalon Studio versions</strong></p>
			</td>
		</tr>
		<tr>
			<td>
				<p><a href="https://docs.katalon.com/katalon-studio/docs/selenium-testng-junit-migration.html">Selenium</a></p>
			</td>
			<td>v7.4.0+</td>
		</tr>
		<tr>
			<td>
				<p><a href="https://docs.katalon.com/katalon-studio/docs/import-selenium-ide.html">Selenium IDE</a></p>
			</td>
			<td>v7.5.10+</td>
		</tr>
		<tr>
			<td>
				<p><a href="https://docs.katalon.com/katalon-studio/docs/import-postman.html">Postman</a></p>
			</td>
			<td>v7.8.0+</td>
		</tr>
		<tr>
			<td>
				<p><a href="https://docs.katalon.com/katalon-studio/docs/import-soapui.html">SoapUI</a></p>
			</td>
			<td>v7.8.0+</td>
		</tr>
	</tbody>
</table>

### Offering

<table width="70%">
	<tbody>
		<tr>
			<td>&nbsp;</td>
			<td><strong>Supported Katalon Studio versions</strong></td>
		</tr>
		<tr>
			<td>
				<p>Community package (<a href="https://www.katalon.com/pricing/">Comparison</a>)</p>
			</td>
			<td>
				<p>v7.0.0+</p>
			</td>
		</tr>
		<tr>
			<td>
				<p>Enterprise packages</p>
			</td>
			<td>
				<p>v7.0.0+</p>
			</td>
		</tr>
	</tbody>
</table>
<p>&nbsp;</p>

### Support

<table>
	<tbody>
		<tr>
			<td><strong></strong></td>
			<td><strong>Supported Katalon Studio versions</strong></td>
		</tr>
		<tr>
			<td>
				<p><a href="https://forum.katalon.com/">Katalon forum</a></p>
			</td>
			<td>
				<p>v7.0.0+</p>
			</td>
		</tr>
		<tr>
			<td>
				<p><a href="https://www.katalon.com/pricing/">Exclusive Support Service</a></p>
			</td>
			<td>
				<p>v7.0.0+</p>
			</td>
		</tr>
	</tbody>
</table>
<a href="#top"> Back to top </a>