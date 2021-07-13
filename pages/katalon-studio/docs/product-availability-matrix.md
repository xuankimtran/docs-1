---
title: "Supported Technologies"
sidebar: katalon_studio_docs_sidebar
permalink: /katalon-studio/docs/product-availability-matrix.html
---

This document gives you information on the supported technologies and integrations. For the supported environments (including browsers and operating systems), see [this document](https://docs.katalon.com/katalon-studio/docs/supported-environments.html).

<table id="top" class="top-vertical-align-table">
    <tr>
        <td colspan="2"><strong>Supported Application Under Test (AUT)</strong>
        </td>
    </tr>
    <tr>
        <td style="width:50%"><strong>Web UI</strong>
            <ul>
                <li>Support all front-end frameworks: ReactJS, AngularJS, VueJS.
                <li>Cross-browser compatibility: Chrome, Firefox, Safari, Edge
                </li>
            </ul>
        </td>
        <td><strong>Mobile</strong>
            <ul>
                <li>Android & iOS
                <li>Native application
                <li>Web mobile
                <li>Hybrid <a href="#mobile-limit">(*)</a>
                </li>
            </ul>
        </td>
    </tr>
    <tr>
        <td style="width:50%"><strong>API</strong>
            <ul>
                <li>REST: <a href="https://docs.katalon.com/katalon-studio/docs/import-rest-requests-from-swagger-20.html"> Swagger</a>, <a href="https://docs.katalon.com/katalon-studio/docs/import-openapi30.html"> OpenAPI 3.0</a> &amp;<a href="https://docs.katalon.com/katalon-studio/docs/import-wadl.html"> WADL</a></li>
                <li>SOAP (SOAP 1.1 & 1.2)
                <li>Authentication: <a
                        href="https://docs.katalon.com/katalon-studio/docs/authorization-basic.html">Basic</a>, <a
                        href="https://docs.katalon.com/katalon-studio/docs/authorization-oauth1.html">OAuth 1.0</a> &<a
                        href="https://docs.katalon.com/katalon-studio/docs/authorization-oauth2.html"> OAuth 2.0</a>
                </li>
            </ul>
        </td>
        <td style="width:50%"><strong>Windows</strong>
            <ul>
                <li>Universal Windows Platform (UWP)
                <li>Windows Forms (WinForms)
                <li>Windows Presentation Foundation (WPF)
                <li>Classic Windows (Win32) apps on Windows 10 PCs
                </li>
            </ul>
        </td>
    </tr>
    <tr>
        <td colspan="2"><strong>Programming Skill & Language</strong>
        </td>
    </tr>
    <tr>
        <td colspan="2">
            <ul>
                <li>Code-less: rich set of utilities to generate and maintain automated script without programming
                    skills
                <li>Groovy 2.4.7
                <li>Java v8.0 - v14
                </li>
            </ul>
        </td>
    </tr>
    <tr>
        <td style="width:50%"><strong>Testing Methodologies</strong>
        </td>
        <td><strong>Testing Capabilities</strong>
        </td>
    </tr>
    <tr>
        <td>
            <ul>
                <li><a href="https://github.com/katalon-studio-samples/katalon-bdd-cucumber-tests">Behavior-driven
                        development - BDD</a>
                <li><a href="https://github.com/katalon-studio-samples/data-driven-tests">Data-driven testing - DDT</a>
                <li>Keyword-driven testing - KDT
                <li>Page Object Model - POM
                </li>
            </ul>
        </td>
        <td>
            <ul>
                <li>Integration Testing
                <li>Functional Testing
                <li>E-2-E Testing
                <li><a href="https://github.com/katalon-studio-samples/web-visual-testing-samples">Visual Testing</a>
                </li>
            </ul>
        </td>
    </tr>
    <tr>
        <td colspan="2"><strong>Report</strong>
        </td>
    </tr>
    <tr>
        <td colspan="2">
            <ul>
                <li>Execution summary in HTML, PDF, CSV format
                <li>Dynamic email configuration
                <li>Release/build-based reports
                <li>Performance, Trending & Insights reports
                </li>
            </ul>
        </td>
    </tr>
    <tr>
        <td style="width:50%"><strong>Cloud Device integration</strong>
        </td>
        <td><strong>ALM integration</strong>
        </td>
    </tr>
    <tr>
        <td>
            <ul>
                <li><a
                        href="https://docs.katalon.com/katalon-studio/videos/introducing_kobiton_katalon_studio.html">Kobiton</a>
                <li><a href="https://docs.katalon.com/katalon-studio/docs/saucelabs-plugin.html">Sauce Labs</a>
                <li><a
                        href="https://docs.katalon.com/katalon-studio/docs/browserstack-integration.html">Browserstack</a>
                <li><a href="https://docs.katalon.com/katalon-studio/docs/lambdatest-integration.html">LambdaTest</a>
                <li><a
                        href="https://docs.katalon.com/katalon-studio/docs/introduction-to-desired-capabilities.html#remote-server">Custom
                        integration</a>
                </li>
            </ul>
        </td>
        <td>
            <ul>
                <li><a href="https://docs.katalon.com/katalon-studio/docs/jira-integration.html">Jira</a>
                <li><a href="https://docs.katalon.com/katalon-studio/docs/qtest-integration.html">qTest</a>
                <li><a href="https://docs.katalon.com/katalon-studio/docs/testrail-integration.html">TestRail</a>
                <li><a href="https://docs.katalon.com/katalon-studio/docs/rally-integration.html">Rally</a>
                <li><a href="https://docs.katalon.com/katalon-studio/docs/testlink-integration.html">TestLink</a>
                <li><a href="https://docs.katalon.com/katalon-store/docs/publisher/example-plugin-testrail.html">Custom
                        ALM integration</a>
                </li>
            </ul>
        </td>
    </tr>
    <tr>
        <td style="width:50%"><strong>CI/CD integration</strong>
        </td>
        <td><strong>Migration from other tools</strong>
        </td>
    </tr>
    <tr>
        <td>
            <ul>
                <li><a href="https://docs.katalon.com/katalon-studio/docs/jenkins-plugin-windows.html">Jenkins</a>
                <li><a href="https://docs.katalon.com/katalon-studio/docs/azure-devops-extension.html">Azure DevOps
                        Pipeline</a>
                <li><a href="https://docs.katalon.com/katalon-studio/docs/integration-circleci.html">CircleCI</a>
                <li><a href="https://docs.katalon.com/katalon-studio/docs/bamboo-addon.html">Bamboo</a>
                <li><a
                        href="https://docs.katalon.com/katalon-studio/docs/teamcity-plugin.html">TeamCity</a>
                <li><a href="https://docs.katalon.com/katalon-studio/docs/intro-RE.html">Custom CI/CD integration</a>
                </li>
            </ul>
        </td>
        <td>
            <ul>
                <li>From<a href="https://docs.katalon.com/katalon-studio/docs/selenium-testng-junit-migration.html">
                        Selenium</a> &<a href="https://docs.katalon.com/katalon-studio/docs/import-selenium-ide.html">
                        Selenium IDE</a>
                <li>From Katalon Recorder
                <li>From<a href="https://docs.katalon.com/katalon-studio/docs/import-postman.html"> Postman</a>
                <li>From<a href="https://docs.katalon.com/katalon-studio/docs/import-soapui.html"> SoapUI</a>
                </li>
            </ul>
        </td>
    </tr>
    <tr>
        <td style="width:50%"><strong>Offering</strong>
        </td>
        <td><strong>Support</strong>
        </td>
    </tr>
    <tr>
        <td>
            <ul>
                <li>Community package (<a href="https://www.katalon.com/pricing/">Comparison</a>)
                <li>Enterprise packages
                </li>
            </ul>
        </td>
        <td>
            <ul>
                <li><a href="https://forum.katalon.com/">Katalon forum</a>
                <li><a href="https://www.katalon.com/pricing/">Exclusive Support Service</a>
                </li>
            </ul>
        </td>
    </tr>
</table>

<p id="mobile-limit">(*) <i>Limitation: Elements inside embedded web views cannot be captured automatically by Record&Spy utilities. </i><a href="#top">Back to top</a></p>

> Leave a comment below to propose any technologies you need Katalon Studio to support.
