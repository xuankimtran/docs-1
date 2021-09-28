---
title: "Troubleshoot common exceptions when executing web tests"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/troubleshoot-common-execution-exceptions-web-test.html
redirect_from:
    - "/display/KD/Troubleshooting+common+issues+related+to+interacting+with+an+element/"
    - "/display/KD/Troubleshooting%20common%20issues%20related%20to%20interacting%20with%20an%20element/"
    - "/x/awXR/"
    - "/katalon-studio/docs/troubleshooting-common-issues-related-to-interacting-with-an-element/"
    - "/katalon-studio/docs/troubleshooting-common-issues-related-to-interacting-with-an-element.html"
    - "/display/KD/troubleshooting+web+automated+testing/"
    - "/display/KD/troubleshooting%20web%20automated%20testing/"
    - "/katalon-studio/docs/troubleshooting-web-automated-testing/"
    - "/katalon-studio/docs/troubleshooting-web-automated-testing.html"
---

> Tips
>
>* Please use **Ctrl+F** to look for the exceptions and errors you have encountered quickly.
>* If the exception you are looking for is not documented, please leave a comment below to request a proposed solution from the Katalon team.

<table>
<thead>
<tr>
<th>Issue</th>
<th>Solution</th>
</tr>
</thead>
<tbody>
<tr>
<td>com.kms.katalon.core.webui.exception.WebElementNotFoundException: Web element with id ... not found.</td>
<td>
<p>Update WebDriver via the Katalon tool:</p>
On the main toolbar, select <strong>Tool &gt;&nbsp;Update WebDrivers&nbsp;&gt; select the corresponding browser in the drop-down list.</strong></td>
</tr>
<tr>
<td>com.kms.katalon.core.webui.exception.WebElementNotFoundException: Web element with id ... not found.</td>
<td>
<p>Try one of the following solutions to resolve the issue:</p>
<ol>
<li>Correct the element's XPath locator.
<ul>
<li>Open your page using Chrome.</li>
<li>Right-click on your desired test object &gt;&nbsp;select <strong>Inspect</strong>.</li>
<li>In the <strong>Elements</strong> tab of <strong>DevTool</strong>, right-click on your target object and select <strong>Copy</strong> &gt;&nbsp;<strong>Copy XPath</strong>.</li>
<li>Open your test object in Katalon Studio &gt;&nbsp;update XPath property with the copied value.</li>
</ul>
</li>
<li>You can also try optimizing your Test Object properties by referring to this document here:<a href="https://docs.katalon.com/katalon-studio/docs/optimizing-object-identification-and-tools.html"> Optimize object identification and tools.</a></li>
</ol>
</td>
</tr>
<tr>
<td>selenium.ElementNotVisibleException: Element is not currently visible and so may not be interacted.</td>
<td>Add the <code>Wait For Element Visible</code> keyword before the one having this issue. To learn more about the <code>Wait For Element Visible</code> keyword, you can refer to this document here: <a href="https://docs.katalon.com/katalon-studio/docs/webui-wait-for-element-visible.html"> [WebUI] Wait For Element Visible</a>. For example:
<pre><code>WebUI.openBrowser('http://demoaut.katalon.com')
WebUI.waitForElementVisible(findtestObject('btn_Login'),30)<br />WebUI.click(findTestObject('btn_Login'))</code></pre>
</td>
</tr>
<tr>
<td>org.openqa.selenium.InvalidElementStateException: invalid element state: Element is not currently interactable and may not be manipulated.</td>
<td>
<p>Try one of the following solutions to resolve the issue:</p>
<ol>
<li>Wait until the element is visible.</li>
<li>Set a value directly using Javascript.</li>
</ol>
<pre><code>import com.kms.katalon.core.webui.common.WebUiCommonHelper
WebElement element = WebUiCommonHelper.findWebElement(findTestObject('your/object'),30)<br />WebUI.executeJavaScript("arguments[0].value='Your Value'", Arrays.asList(element))</code></pre>
</td>
</tr>
<tr>
<td>org.openqa.selenium.WebDriverException: Element is not clickable at point (x, y). Other elements would receive the click: ...</td>
<td>
<p>Click on the element using the <code>Execute Javascript</code> keyword instead. To learn more about the <code>Javascript</code> keyowrd, you can refer to this document here: <a href="https://docs.katalon.com/katalon-studio/docs/webui-execute-javascript.html#description-"> [WebUI] Execute JavaScript</a>. For example:</p>
<pre><code>import com.kms.katalon.core.webui.common.WebUiCommonHelper
WebElement element = WebUiCommonHelper.findWebElement(findTestObject('your/object'),30)<br />WebUI.executeJavaScript("arguments[0].click", Arrays.asList(element))</code></pre>
</td>
</tr>
<tr>
<td>Timed out waiting for the driver server to start.</td>
<td>
<ul>
<li>Download the correct Edge driver from the Microsoft website here:&nbsp;<a href="https://developer.microsoft.com/en-us/microsoft-edge/tools/webdriver/">Microsoft Edge Driver </a>based on your OS build (Go to&nbsp;<strong>Start</strong>&nbsp;&gt;&nbsp;<strong>Settings</strong>&nbsp;&gt;&nbsp;<strong>System</strong>&nbsp;&gt;&nbsp;<strong>About</strong>&nbsp;and locate the number next to OS Build on the screen).</li>
<li>Copy downloaded Edge driver and replace it in existing edgedriver&nbsp;folder of Katalon Studio. For example:&nbsp;<strong>C:\\Katalon\_Studio\_Windows_64-4.8\\configuration\\resources\\drivers\\edgedriver</strong></li>
</ul>
</td>
</tr>
<tr>
<td>Unable to record on Internet Explorer.</td>
<td>
<ul>
<li>Open Internet Explorer, select the <strong>Tools</strong> button, and then select <strong> Manage add-ons</strong>.</li>
<li>Under <strong>Show</strong>, select <strong>All add-ons</strong>.</li>
<li>Select the <strong>RecorderExtension.RecorderBHO</strong>, <strong>Enable,</strong> and then select <strong>Close</strong>. <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/troubleshooting-web-automated-testing/image2017-10-27-163A293A17.png" alt="" width="85%" /></li>
</ul>
</td>
</tr>
<tr>
<td>Unable to connect to Katalon server.</td>
<td>
<p>Allow the following .exe files to communicate through Windows Firewall. To learn more about allowing apps through Windows Firewall, you can refer to the Microsoft document here: <a href="https://support.microsoft.com/en-us/windows/risks-of-allowing-apps-through-windows-defender-firewall-654559af-3f54-3dcf-349f-71ccd90bcc5c">Risks of allowing apps through Windows Defender Firewall</a>.</p>
<ul>
<li>geckodriver.exe</li>
<li>chromedriver.exe</li>
<li>iedriverserver.exe</li>
</ul>
<p>These executable files can be located in: <strong>&lt;Katalon Studio folder&gt;\\configuration\\resources\\drivers</strong>.</p>
<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/troubleshooting-web-automated-testing/Screen-Shot-2018-04-24-at-13.51.51.png" alt="" width="85%" /><img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/troubleshooting-web-automated-testing/Screen-Shot-2018-04-24-at-13.51.41.png" alt="" width="85%" />
<p>You may also need to add Google Chrome (chrome.exe) and Firefox (firefox.exe) in the worst case if your current Windows Firewall blocks them as well.</p>
</td>
</tr>
<tr>
<td>Use different browser versions.</td>
<td>In case you want Katalon Studio to use different versions besides the currently installed version, there are two ways to do it:
<p>1. Use custom keywords. Follow these steps:</p>
<ul>
<li>The browser&nbsp;instances you wish to use should be installed on your machine first.</li>
<li>Create a custom keyword&nbsp;to open the browser. Press <strong>Ctrl + Shift + O</strong> to automatically import necessary packages. To learn more about creating a custom keyword, you can refer to this document here: <a href="https://docs.katalon.com/katalon-studio/docs/introduction-to-custom-keywords.html#create-a-custom-keyword">Introduction to Custom Keyword</a>.</li>
<li><details><summary>For example</summary>
<pre><code>package com.example
import org.openqa.selenium.WebDriver
import org.openqa.selenium.chrome.ChromeDriver
import org.openqa.selenium.chrome.ChromeOptions
import org.openqa.selenium.firefox.FirefoxDriver
import com.kms.katalon.core.annotation.Keyword
import com.kms.katalon.core.webui.driver.DriverFactory
public class WebUICustomKeywords {
&nbsp;@Keyword
&nbsp;def openFirefoxBrowser(String firefoxPath, String firefoxDriver) {
 //Set path to Firefox version
 System.setProperty("webdriver.firefox.bin", firefoxPath)
 //Set path to Firefox driver: \configuration\resources\drivers\firefox_win64\geckodriver.exe
 System.setProperty("webdriver.gecko.driver", firefoxDriver)
 WebDriver driver = new FirefoxDriver()
 DriverFactory.changeWebDriver(driver)
&nbsp;}
&nbsp;@Keyword
&nbsp;def openChromeBrowser(String chromeDriverPath, String chromePath)
&nbsp;{
//Set path to chromedriver driver: \configuration\resources\drivers\chrome_win32\chromedriver.exe
 System.setProperty("webdriver.chrome.driver", chromeDriverPath)
 ChromeOptions options = new ChromeOptions()
 //Set path to Chrome binary
 options.setBinary(chromePath)
 WebDriver driver = new ChromeDriver(options)
 DriverFactory.changeWebDriver(driver)
&nbsp;}
}</code></pre>
</details></li>
<li>In a test case, use this custom keyword instead of the<code>&nbsp;Open Browser&nbsp;</code>keyword.</li>
<li><details><summary>For example.</summary>
<pre><code>CustomKeywords.'com.example.WebUICustomKeywords.openFirefoxBrowser'('C:\\Program Files\\Mozilla Firefox 52\\firefox.exe',
&nbsp;'C:\\5.4\\Katalon Studio Windows 64\\configuration\\resources\\drivers\\firefox_win64\\geckodriver.exe')
WebUI.navigateToUrl(GlobalVariable.G_SiteURL)
WebUI.click(findTestObject('Page_CuraHomepage/btn_MakeAppointment'))</code></pre>
</details></li>
</ul>
2. Downgrade browser version: Another approach is to downgrade your current browser's version to a version you want. If you want to use a very old version of your current browser, you may need to downgrade or upgrade browser drivers as well as Selenium WebDriver, you can refer to this document here: <a href="https://docs.katalon.com/katalon-studio/docs/upgrade-or-downgrade-webdrivers.html">Update or Downgrade WebDrivers</a>.</td>
</tr>
</tbody>
<tbody>
<tr>
<td>org.openqa.selenium.ElementClickInterceptedException: element click intercepted: Element is not clickable at point</td>
<td>
<p>1.&nbsp;If the test case fails because there is another object covering the target element, for example, a pop-up dialog, you can add actions to remove the object before the <strong>Click </strong>action.</p>
<p>2. From Katalon version 8.2.0 onwards, if the <strong>Default wait for element timeout</strong> setting is not long enough for Katalon to click on the target element behind an overlay, you can add the <code>WebUI.waitForElementClickable</code> keyword before the <strong>Click</strong> action. To learn more about using the <code>WebUI.waitForElementClickable</code> keyword, you can refer to this document here:&nbsp;<a href="https://docs.katalon.com/katalon-studio/docs/webui-wait-for-element-clickable.html#description">[WebUI] Wait For Element Clickable.</a></p>
&nbsp;</td>
</tr>
</tbody>
</table>


> The exception you are looking for is not on this page?
>
> Leave a comment below.
