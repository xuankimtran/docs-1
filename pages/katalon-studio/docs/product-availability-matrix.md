---
title: "Supported Technologies"
sidebar: katalon_studio_docs_sidebar
permalink: /katalon-studio/docs/product-availability-matrix.html
---

This document gives you information on the supported technologies and integrations. For the supported environments (including browsers and operating systems), see [this document](https://docs.katalon.com/katalon-studio/docs/supported-environments.html).

<table>
	<tbody>
		<tr>
			<td colspan="2"><strong> Supported Application Under Test</strong> (AUT)</td>
		</tr>
		<tr>
			<td><strong>Web UI </strong></td>
			<td><strong>Mobile </strong></td>
		</tr>
		<tr>
			<td>
				<ul>
					<li>Support all front-end frameworks: ReactJS, AngularJS, VueJS.</li>
					<li>Cross-browser compatibility: Chrome, Firefox, Safari, Edge</li>
				</ul>
			</td>
			<td>
				<ul>
					<li>Android &amp; iOS</li>
					<li>Native application</li>
					<li>Web mobile</li>
					<li>Hybrid <a href="#mobile-limit"> (*) </a></li>
				</ul>
			</td>
		</tr>
		<tr>
			<td><strong>API </strong></td>
			<td><strong>Windows</strong></td>
		</tr>
		<tr>
			<td>
				<ul>
					<li>REST: <a href="https://docs.katalon.com/katalon-studio/docs/import-rest-requests-from-swagger-20.html"> Swagger</a>, <a href="https://docs.katalon.com/katalon-studio/docs/import-openapi30.html"> OpenAPI 3.0 </a> &amp; <a href="https://docs.katalon.com/katalon-studio/docs/import-wadl.html"> WADL </a></li>
					<li>SOAP (SOAP 1.1 &amp; 1.2)</li>
					<li>Authentication: <a href="https://docs.katalon.com/katalon-studio/docs/authorization-basic.html"> Basic </a> , <a href="https://docs.katalon.com/katalon-studio/docs/authorization-oauth1.html"> OAuth 1.0 </a> &amp; <a href="https://docs.katalon.com/katalon-studio/docs/authorization-oauth2.html"> OAuth 2.0 </a></li>
				</ul>
			</td>
			<td>
				<ul>
					<li>Universal Windows Platform (UWP)</li>
					<li>Windows Forms (WinForms)</li>
					<li>Windows Presentation Foundation (WPF)</li>
					<li>Classic Windows (Win32) apps on Windows 10 PCs</li>
				</ul>
			</td>
		</tr>
		<tr>
			<td colspan="2"><strong> Programming Skill &amp; Language </strong></td>
		</tr>
		<tr>
			<td colspan="2">
				<ul>
					<li>Code-less: rich set of utilities to generate and maintain automated script without programming skills</li>
					<li>Groovy 2.4.7</li>
					<li>Java v8.0 - v14</li>
				</ul>
			</td>
		</tr>
		<tr>
			<td><strong> Testing Methodologies </strong></td>
			<td><strong> Testing Capabilities </strong></td>
		</tr>
		<tr>
			<td>
				<ul>
					<li><a href="https://github.com/katalon-studio-samples/katalon-bdd-cucumber-tests"> Behavior-driven development - BDD </a></li>
					<li><a href="https://github.com/katalon-studio-samples/data-driven-tests"> Data-driven testing - DDT </a></li>
					<li>Keyword-driven testing - KDT</li>
					<li>Page Object Model - POM</li>
				</ul>
			</td>
			<td>
				<ul>
					<li>Integration Testing</li>
					<li>Functional Testing</li>
					<li>E-2-E Testing</li>
					<li><a href="https://github.com/katalon-studio-samples/web-visual-testing-samples"> Visual Testing </a></li>
				</ul>
			</td>
		</tr>
		<tr>
			<td colspan="2"><strong> Report </strong></td>
		</tr>
		<tr>
			<td colspan="2">
				<ul>
					<li>Execution summary in HTML, PDF, CSV format</li>
					<li>Dynamic email configuration</li>
					<li>Release/build-based reports</li>
					<li>Performance, Trending &amp; Insights reports</li>
				</ul>
			</td>
		</tr>
		<tr>
			<td><strong> Cloud Device integration </strong></td>
			<td><strong> ALM integration </strong></td>
		</tr>
		<tr>
			<td>
				<ul>
					<li><a href="https://docs.katalon.com/katalon-studio/videos/introducing_kobiton_katalon_studio.html"> Kobiton </a></li>
					<li><a href="https://docs.katalon.com/katalon-studio/docs/saucelabs-plugin.html"> Sauce Labs </a></li>
					<li><a href="https://docs.katalon.com/katalon-studio/docs/browserstack-integration.html"> Browserstack </a></li>
					<li><a href="https://docs.katalon.com/katalon-studio/docs/lambdatest-integration.html"> LambdaTest </a></li>
					<li><a href="https://docs.katalon.com/katalon-studio/docs/introduction-to-desired-capabilities.html#remote-server"> Custom integration </a></li>
				</ul>
			</td>
			<td>
				<ul>
					<li><a href="https://docs.katalon.com/katalon-studio/docs/jira-integration.html"> Jira </a></li>
					<li><a href="https://docs.katalon.com/katalon-studio/docs/qtest-integration.html"> qTest </a></li>
					<li><a href="https://docs.katalon.com/katalon-studio/docs/testrail-integration.html"> TestRail </a></li>
					<li><a href="https://docs.katalon.com/katalon-studio/docs/rally-integration.html"> Rally </a></li>
					<li><a href="https://docs.katalon.com/katalon-studio/docs/testlink-integration.html"> TestLink </a></li>
					<li><a href="https://docs.katalon.com/katalon-store/docs/publisher/example-plugin-testrail.html"> Custom ALM integration </a></li>
				</ul>
			</td>
		</tr>
		<tr>
			<td><strong> CI/CD integration </strong></td>
			<td><strong> Migration from other tools </strong></td>
		</tr>
		<tr>
			<td>
				<ul>
					<li><a href="https://docs.katalon.com/katalon-studio/docs/jenkins-plugin-windows.html"> Jenkins </a></li>
					<li><a href="https://docs.katalon.com/katalon-studio/docs/azure-devops-extension.html"> Azure DevOps Pipeline </a></li>
					<li><a href="https://docs.katalon.com/katalon-studio/docs/integration-circleci.html"> CircleCI </a></li>
					<li><a href="https://docs.katalon.com/katalon-studio/docs/bamboo-addon.html"> Bamboo </a></li>
					<li><a href="https://docs.katalon.com/katalon-studio/docs/teamcity-plugin.html"> TeamCity </a></li>
					<li><a href="https://docs.katalon.com/katalon-studio/docs/intro-RE.html"> Custom CI/CD integration </a></li>
				</ul>
			</td>
			<td>
				<ul>
					<li>From <a href="https://docs.katalon.com/katalon-studio/docs/selenium-testng-junit-migration.html"> Selenium </a> &amp; <a href="https://docs.katalon.com/katalon-studio/docs/import-selenium-ide.html"> Selenium IDE </a></li>
					<li>From Katalon Recorder</li>
					<li>From <a href="https://docs.katalon.com/katalon-studio/docs/import-postman.html"> Postman </a></li>
					<li>From <a href="https://docs.katalon.com/katalon-studio/docs/import-soapui.html"> SoapUI </a></li>
				</ul>
			</td>
		</tr>
		<tr>
			<td><strong> Offering </strong></td>
			<td><strong> Support </strong></td>
		</tr>
		<tr>
			<td>
				<ul>
					<li>Community package ( <a href="https://www.katalon.com/pricing/"> Comparison </a> )</li>
					<li>Enterprise packages</li>
				</ul>
			</td>
			<td>
				<ul>
					<li><a href="https://forum.katalon.com/"> Katalon forum </a></li>
					<li><a href="https://www.katalon.com/pricing/"> Exclusive Support Service </a></li>
				</ul>
			</td>
		</tr>
	</tbody>
</table>
<p>(*) <em> Limitation: Elements inside embedded web views cannot be captured automatically by Record&amp;Spy utilities. </em><a href="#top"> Back to top </a></p>

> Leave a comment below to propose any technologies you need Katalon Studio to support.
