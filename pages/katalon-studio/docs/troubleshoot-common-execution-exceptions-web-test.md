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
            <td>
                    com.kms.katalon.core.webui.exception.WebElementNotFoundException: Web element with id ... not found.</td>
            <td>
                    <p>Update WebDriver via the Katalon tool:</p>
                    On main toolbar, select 
                    <b>Tool &gt;&nbsp;Update WebDrivers&nbsp;&gt; select the corresponding browser in the drop-down list.</b>
</code></pre>
                </ul>
                    </li>
            </td>
        </tr>
        <tr>
            <td>com.kms.katalon.core.webui.exception.WebElementNotFoundException: Web element with id ... not found.</td>
            <td>
                <p>
                    Try one of the following solutions to resolve the issue:
                <ol>
                    <li>Correct the element's XPath locator.
                        <ul>
                            <li>Open your page using Chrome.</li>
                            <li>Right-click on your desired test object &gt;&nbsp;select <b>Inspect</b>.</li>
                            <li>In the <b>Elements</b> tab of <strong>DevTool</strong>, right-click on your target object and select <b>Copy</b> &gt;&nbsp;<b>Copy XPath</b>.
                            <li>Open your test object in Katalon Studio &gt;&nbsp;update XPath property with the copied value.</li>
                        </ul>
                    </li>
                    <li><a href="https://docs.katalon.com/katalon-studio/docs/optimizing-object-identification-and-tools.html">Optimize object identification and tools.</a></li>
                </p>
                </ol>
            </td>
        </tr>
        <tr>
            <td>
                selenium.ElementNotVisibleException: Element is not currently visible and so may not be interacted.
            </td>
            <td>
            Add the <a href="display/KD/%5BWebUI%5D+Wait+For+Element+Visible">Wait For Element Visible</a> step before the one having this issue. For example:
            <pre><code class="language-groovy">WebUI.openBrowser('http://demoaut.katalon.com')
WebUI.waitForElementVisible(findtestObject('btn_Login'),30)
WebUI.click(findTestObject('btn_Login'))</code></pre>
            </td>
        </tr>
        <tr>
            <td>org.openqa.selenium.InvalidElementStateException: invalid element state: Element is not currently interactable and may not be manipulated.</td>
            <td>
                <p>
                    Try one of the following solutions to resolve the issue:
                    <ol>
                        <li>Wait until the element is visible.
                        <li>Set a value directly using Javascript.
                    </ol>
                        <pre><code class="language-groovy">import com.kms.katalon.core.webui common.WebUiCommonHelper
WebElement element = WebUiCommonHelper.findWebElement(findTestObject('your/object'),30)
WebUI.executeJavaScript("arguments[0].value='Your Value'", Arrays.asList(element))</code></pre>
                </p>
            </td>
        </tr>
        <tr>
            <td>org.openqa.selenium.WebDriverException: Element is not clickable at point (x, y). Other element would receive the click: ...</td>
            <td>
                <p> 
                    Click on the element using <a href="/display/KD/%5BWebUI%5D+Execute+JavaScript">Javascript</a> instead.
                    <pre><code>import com.kms.katalon.core.webui.common.WebUiCommonHelper
WebElement element = WebUiCommonHelper.findWebElement(findTestObject('your/object'),30)
WebUI.executeJavaScript("arguments[0].click", Arrays.asList(element))</code></pre>
                </p>
            </td>
        </tr>
        <tr>
            <td>Timed out waiting for driver server to start.</td>
            <td>
                    <ul>
                        <li>Download correct Edge driver from this page: <a href="https://developer.microsoft.com/en-us/microsoft-edge/tools/webdriver/">https://developer.microsoft.com/en-us/microsoft-edge/tools/webdriver/</a> based on your OS build (Go to <b>Start</b> > <b>Settings</b> > <b>System</b> > <b>About</b> and locate the number next to OS Build on the screen).
                        <li>Copy downloaded Edge driver and replace it in existing edgedriver folder of Katalon Studio. For example: <strong>C:\\Katalon\_Studio\_Windows_64-4.8\\configuration\\resources\\drivers\\edgedriver</strong>
                    </ul>
            </td>
        </tr>
        <tr>
            <td>Unable to record on Internet Explorer.</td>
            <td>
                <ul>
                    <li>Open 'Manage Add-ons' in Internet Explorer: <a href="https://support.microsoft.com/en-us/help/17447/windows-internet-explorer-11-manage-add-ons">https://support.microsoft.com/en-us/help/17447/windows-internet-explorer-11-manage-add-ons</a>.
                    <li>Enable the RecorderExtension.RecorderBHO.
                    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/troubleshooting-web-automated-testing/image2017-10-27-163A293A17.png" width=85%>
                <ul>
            </td>
        </tr>
        <tr>
            <td>Unable to connect to Katalon server.</td>
            <td>
                <p>
                    Allow the following .exe files to communicate through Windows Firewall. Here is the full <a href="https://www.howtogeek.com/howto/uncategorized/how-to-create-exceptions-in-windows-vista-firewall/">guide</a> to access this interface:
                </p>
                    <ul>
                        <li> geckodriver.exe
                        <li> chromedriver.exe
                        <li> iedriverserver.exe
                    </ul>
                <p> 
                    These executable files can be located in: <strong>&lt;Katalon Studio folder&gt;\\configuration\\resources\\drivers</strong>.
                </p>
                <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/troubleshooting-web-automated-testing/Screen-Shot-2018-04-24-at-13.51.51.png" width=85%>
                <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/troubleshooting-web-automated-testing/Screen-Shot-2018-04-24-at-13.51.41.png" width=85%>
                <p>
                    You may also need to add Google Chrome (chrome.exe) and Firefox (firefox.exe) in the worst case if your current Windows Firewall block them as well.
                </p>
            </td>
        </tr>
        <tr>
            <td>Use different browser versions.</td>
                    In case you want Katalon Studio to use different versions besides the current installed version, there are two ways to do it:
                </p>
    </tbody>
</table>





> The exception you are looking for isn’t on this page?
>
> Leave a comment below.