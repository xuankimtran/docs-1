---
title: "Katalon Studio vs Katalon Studio Enterprise Features"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/katalon-studio-vs-katalon-studio-enterprise.html
---

This document reflects the comparison between free and Enterprise-exclusive features in the latest version of Katalon Studio.

<table>
  <tbody>
    <tr valign="top">
      <th>Component</th>
      <th>Features</th>
      <th>Description</th>
      <th>KS</th>
      <th>KSE</th>
    </tr>
    <tr>
      <td rowspan="9"><strong>Test Generation</strong></td>
      <td> <strong>Web UI</strong>: <a href="https://docs.katalon.com/katalon-studio/docs/create_test_case_using_record_playback.html">Record and Playback</a> with debugging options </td>
      <td> Quickly correct test failures on newly recorded test to make it reliable.</td>
      <td></td>
      <td><div data-align="center">
					<p>✔</p>
				</div></td>
    </tr>
    <tr valign="top">
      <td> <strong>Web UI</strong>: <a href="https://docs.katalon.com/katalon-studio/docs/web-image-based-testing.html">Image-based Testing</a> </td>
      <td> Find and interact with image objects. This feature is particularly helpful when objects retain the same appearance even if the underlying structures have changed.</td>
      <td></td>
      <td><div data-align="center">
					<p>✔</p>
				</div></td>
    </tr>
    <tr valign="top">
      <td> <strong>Web UI</strong>: <a href="https://docs.katalon.com/katalon-studio/docs/auto-healing-smart-xpath.html">Smart XPath Generator</a></td>
      <td> Auto-generate neighbor XPaths as alternative locators to find an object at runtime.</td>
      <td><div data-align="center">
					<p>✔</p>
				</div></td>
      <td><div data-align="center">
					<p>✔</p>
				</div></td>
    </tr>
    <tr valign="top">
      <td> <strong>Web UI</strong>: <a href="https://docs.katalon.com/katalon-studio/docs/web-selection-methods.html">Advanced Web Locator Settings</a></td>
      <td> Define if XPath, Attributes, or CSS is the default web locator when using Recorder and Spy.</td>
      <td></td>
      <td><div data-align="center">
					<p>✔</p>
				</div></td>
    </tr>
    <tr valign="top">
      <td> <strong>Web Service</strong>: <a href="https://docs.katalon.com/katalon-studio/docs/import-openapi30.html">Import OpenAPI Specification 3.0</a> </td>
      <td> Quickly create test objects by importing RESTful APIs with OpenAPI Specification version 3.0.</td>
      <td></td>
      <td><div data-align="center">
					<p>✔</p>
				</div></td>
    </tr>
    <tr valign="top">
      <td> <strong>Web Service</strong>: Customized Request Methods and Advanced Settings </td>
      <td>
        <ul>
          <li> Create and test requests with custom methods beside standard HTTP methods (GET, POST, PUT, DELETE..).</li>
          <li> Improve test performance by limiting connection timeout and response maximum size.</li>
        </ul>
      </td>
      <td></td>
      <td><div data-align="center">
					<p>✔</p>
				</div></td>
    </tr>
    <tr valign="top">
      <td> <strong>Web UI</strong> and <strong>Web Service</strong>: SSL Client Certificate </td>
      <td> Configure Katalon Studio to use client certificate for all requests. </td>
      <td></td>
      <td><div data-align="center">
					<p>✔</p>
				</div></td>
    </tr>
    <tr valign="top">
      <td> <strong>Mobile</strong>: <a href="https://docs.katalon.com/katalon-studio/docs/mobile-image-based-testing.html">Image-based testing</a></td>
      <td> Find and interact with image elements. This feature is particularly helpful for testing dynamic or canvas elements. </td>
      <td></td>
      <td><div data-align="center">
					<p>✔</p>
				</div></td>
    </tr>
    <tr valign="top">
      <td> <strong>Windows Desktop</strong>: <a href="https://docs.katalon.com/katalon-studio/docs/windows-native-record.html">Native Windows Recorder</a></td>
      <td> Seamless test recording experience that's similar to web recorder. </td>
      <td></td>
      <td><div data-align="center">
					<p>✔</p>
				</div></td>
    </tr>
    <tr valign="top">
      <td rowspan="5" ><strong>Data-driven testing</strong></td>
      <td> Excel, CSV, PostgreSQL, MySQL </td>
      <td> Read input values for test scripts from Excel files, CSV files, internal test data, and database.</td>
      <td><div data-align="center">
					<p>✔</p>
				</div></td>
      <td><div data-align="center">
					<p>✔</p>
				</div></td>
    </tr>
    <tr valign="top">
      <td> Oracle SQL, SQL Server </td>
      <td> Read input values for test scripts from Oracle SQL, and SQL Server.</td>
      <td></td>
      <td><div data-align="center">
					<p>✔</p>
				</div></td>
    </tr>
    <tr valign="top">
      <td> Combine multiple Data Files </td>
      <td> Read input values for test scripts from multiple data file combinations. </td>
      <td></td>
      <td><div data-align="center">
					<p>✔</p>
				</div></td>
    </tr>
    <tr valign="top">
      <td> External Database having JDBC Drivers </td>
      <td> Read input values for test scripts from other databases having JDBC drivers (e.g., MongoDB, SAP HANA DB).</td>
      <td></td>
      <td><div data-align="center">
					<p>✔</p>
				</div></td>
    </tr>
    <tr valign="top">
      <td><a href="https://docs.katalon.com/katalon-studio/docs/manage-checkpoints.html">Checkpoints</a></td>
      <td> Snapshots of test data taken at a specific time. These snapshots are used to verify if the current state of the data source is different from its previously taken state. </td>
      <td></td>
      <td><div data-align="center">
					<p>✔</p>
				</div></td>
    </tr>
    <tr valign="top">
      <td ><strong>Test Execution</strong></td>
      <td> Parallel Execution </td>
      <td> Run multiple test suites at the same time to reduce execution time. </td>
      <td><div data-align="center">
					<p>✔</p>
				</div></td>
      <td><div data-align="center">
					<p>✔</p>
				</div></td>
    </tr>
    <tr valign="top">
      <td ></td>
      <td><a href="https://docs.katalon.com/katalon-studio/docs/test-suite-collection-scheduler.html">Execution Scheduler</a></td>
      <td> Schedule the next run of a test suite collection at a specific time. </td>
      <td></td>
      <td><div data-align="center">
					<p>✔</p>
				</div></td>
    </tr>
    <tr valign="top">
      <td ></td>
      <td> Retry failed tests and consolidate reports </td>
      <td> Rerun failed test cases several times to identify flaky tests. </td>
      <td></td>
      <td><div data-align="center">
					<p>✔</p>
				</div></td>
    </tr>
    <tr valign="top">
      <td ></td>
      <td> <strong>Web UI</strong>: <a href="https://docs.katalon.com/katalon-studio/docs/webui-smartwait.html">Smart Wait</a></td>
      <td> Tackle Selenium waiting issues.</td>
      <td><div data-align="center">
					<p>✔</p>
				</div></td>
      <td><div data-align="center">
					<p>✔</p>
				</div></td>
    </tr>
    <tr valign="top">
      <td ></td>
      <td> <strong>Web UI</strong>: <a href="https://docs.katalon.com/katalon-studio/docs/self-healing.html">Self-healing</a></td>
      <td> Reduce maintenance effort by trying other alternative locators to find an object automatically when the default locator is broken. </td>
      <td></td>
      <td><div data-align="center">
					<p>✔</p>
				</div></td>
    </tr>
    <tr valign="top">
      <td ></td>
      <td> <a href="https://docs.katalon.com/katalon-studio/docs/dynamic-test-suite-ks.html">Dynamic Test Suite</a></td>
      <td> Add test cases to a test suite dynamically by search queries.</td>
      <td></td>
      <td><div data-align="center">
					<p>✔</p>
				</div></td>
    </tr>
    <tr valign="top">
      <td ></td>
      <td> Use Java Virtual Machine (JVM) arguments </td>
      <td> Modify the behavior of each Java process in terms of changing heap size, or handling out of memory issue. </td>
      <td></td>
      <td><div data-align="center">
					<p>✔</p>
				</div></td>
    </tr>
    <tr valign="top">
      <td rowspan="2" ><strong>Reporting</strong></td>
      <td>
        <ul>
          <li> Basic Report in HTML, PDF, CSV, JUnit, </li>
          <li> Screenshots </li>
          <li> Videos for browser with GUI </li>
          <li> Time Capsule (HTML snapshot) </li>
          <li> Send Test Suite report email </li>
        </ul>
      </td>
      <td>
        <ul>
          <li> View and share test execution results in HTML, PDF, CSV, or JUnit format. </li>
          <li> Diagnose test failures with screenshots and videos. </li>
          <li> Capture object again with Time Capsule, an HTML snapshot that restores the state of application under test when the test fails. </li>
          <li> Notify multiple users of test suite reports by email. </li>
        </ul>
      </td>
      <td><div data-align="center">
					<p>✔</p>
				</div></td>
      <td><div data-align="center">
					<p>✔</p>
				</div></td>
    </tr>
    <tr valign="top">
      <td>
        <ul>
          <li> Videos for headless browsers </li>
          <li> Report history and test suite collection reports </li>
          <li> Send test suite collection reports by email </li>
          <li> Customized execution log </li>
        </ul>
      </td>
      <td>
        <ul>
          <li> Diagnose test failures with videos when test runs and fails on headless browser. </li>
          <li> View previous reports of test suite, and test suite collection executions in Katalon Studio.</li>
          <li> View and share test suite collection report in JUnit format. </li>
          <li> Notify you and your colleagues of Test Suite Collection report by email.</li>
          <li> Improve your efficiency and performance with shortened execution log.</li>
        </ul>
      </td>
      <td></td>
      <td><div data-align="center">
					<p>✔</p>
				</div></td>
    </tr>
    <tr valign="top">
      <td rowspan="5" >
        <p align="center">
          <strong>Test Maintenance and Management</strong>
      </td>
      <td>
        <strong>Dual-mode Debugger</strong>
		</br>In Manual view <ul>
          <li>
            Run or Debug from here
          </li>
          <li>
            Debug: Enable or Disable test steps
          </li>
		  </ul>
		  In Script View
		  <ul>
          <li> Debug mode </li>
          <li> Attach source code for debugging </li>
          <li> Decompile Class file for debugging </li>
        </ul>
      </td>
      <td> Quickly correct test failures with multiple debugging features to ensure test script quality. </td>
      <td></td>
      <td><div data-align="center">
					<p>✔</p>
				</div></td>
    </tr>
    <tr valign="top">
      <td> <a href="https://docs.katalon.com/katalon-studio/docs/test-case-management-with-tags.html">Test Case Management with Tags</a> </td>
      <td> Append tags to test cases, then quickly search for or run test cases by tag.</td>
      <td></td>
      <td><div data-align="center">
					<p>✔</p>
				</div></td>
    </tr>
    <tr valign="top">
      <td><a href="https://docs.katalon.com/katalon-studio/docs/import-export-test-artifact.html">Import/Export Test Artifacts</a></td>
      <td> Quickly share test cases, test objects, execution profiles, and custom keywords across projects.</td>
      <td></td>
      <td><div data-align="center">
					<p>✔</p>
				</div></td>
    </tr>
    <tr valign="top">
      <td> <a href="https://docs.katalon.com/katalon-studio/docs/import-export-desired-capabilities.html">Import/Export Desired Capabilities</a></td>
      <td> Reuse desired capabilities across projects</br>
          <em>
		  <strong>Notes</strong>: Desired capabilities are key/value pairs that tell the browser properties such as browser name, browser version, and the path of the browser driver in the system to determine the browser behaviors at runtime.
		  </em>
      </td>
      <td></td>
      <td><div data-align="center">
					<p>✔</p>
				</div></td>
    </tr>
    <tr valign="top">
      <td><a href="https://docs.katalon.com/katalon-studio/docs/test-objects-refactoring.html">Test Objects Refactoring</a></td>
      <td> Keep Object Repository neat and clean by checking, exporting, and removing unused test objects. </td>
      <td></td>
      <td><div data-align="center">
					<p>✔</p>
				</div></td>
    </tr>
    <tr valign="top">
      <td rowspan="3" >
        <strong>Integration</strong>
      </td>
      <td> Application Lifecycle Management (ALM) tools: JIRA, Katalon TestOps, Azure Test Plans, qTest, TestRail, TestLink, Rally </td>
      <td> Integrate test projects with ALM tools to push and pull test artifacts, and test result information between Katalon Studio and the ALM tool. </td>
      <td></td>
      <td><div data-align="center">
					<p>✔</p>
				</div></td>
    </tr>
    <tr valign="top">
      <td> Cloud Provider: <a href="https://docs.katalon.com/katalon-studio/docs/testcloud-integration.html">Katalon TestCloud (Beta)</a>, Kobiton, Sauce Labs </td>
      <td> Connect to cloud providers to test your applications on multiple devices and browsers.</td>
      <td></td>
      <td><div data-align="center">
					<p>✔</p>
				</div></td>
    </tr>
    <tr valign="top">
      <td> Git-based source code management (SCM): GitHub, GitLab, Azure Repos, BitBucket, etc.</td>
      <td> Collaborate, store, manage change, and control version in test project repository with popular Git hosting services.</td>
      <td> <div data-align="center">via HTTPs</div></td>
      <td> <div data-align="center">via SSH</div></td>
    </tr>
    <tr valign="top">
      <td>
        <strong>CLI, CI, Docker Execution</strong>
      </td>
      <td colspan="2">Run your tests in the following environments:
		<ul>
		<li>Command-Line Interface CI Server: Jenkins, Bamboo, TeamCity.</li>
		<li>Cloud CI: CircleCI, Azure DevOps, BitBucket, GitLab, GitHub Action, WS CodeBuild, BuildKite, Circle CI, CodeShip, TravisCI.</li>
		<li>Katalon Docker Image.</li>
		<li>Cloud-based app testing infrastructure: Microsoft App Center Tests, AWS Device Farm.</li>
		</ul></td>
      <td colspan="2">
        <p align="center">
          <strong>With KRE</strong>
      </td>
    </tr>
  </tbody>
</table>