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

### "org.openqa.selenium.InvalidElementStateException: invalid element state: Element is not currently interactable and may not be manipulated"

**Possible causes**:

* This issue usually occurs with the '[Set Text](/display/KD/%5BWebUI%5D+Set+Text)' keyword having a read-only input field.
* The element is not visible.
* The element requires some conditions to display.

**Suggested solutions**:

You can try one of the following solutions to resolve the issue:

* Wait until the element is visible
* Set a value directly using Javascript

   ```groovy
   import com.kms.katalon.core.webui.common.WebUiCommonHelper

   WebElement element = WebUiCommonHelper.findWebElement(findTestObject('your/object'),30)
   WebUI.executeJavaScript("arguments[0].value='Your Value'", Arrays.asList(element))
    ```

### "org.openqa.selenium.WebDriverException: Element is not clickable at point (x, y). Other element would receive the click: ..."

**Possible causes**:

* These are ChromeDriver's clicking issues. [More details](http://chromedriver.chromium.org/help/clicking-issues).
* The element is clickable, but there is a spinner/overlay on top of it.

**Suggested solution**:

Click on the element using [Javascript](/display/KD/%5BWebUI%5D+Execute+JavaScript) instead.

```groovy
import com.kms.katalon.core.webui.common.WebUiCommonHelper

WebElement element = WebUiCommonHelper.findWebElement(findTestObject('your/object'),30)
WebUI.executeJavaScript("arguments[0].click", Arrays.asList(element))
```

> The exception you are looking for isn’t on this page?
>
> Leave a comment below.

You can try one of the following solutions to resolve the issue:

### "selenium.ElementNotVisibleException: Element is not currently visible and so may not be interacted."

**Possible causes**:

* The element is hidden and is not ready.
* The element is not visible yet after the current page is loaded.

**Suggested solution**:

Add the [Wait For Element Visible](/display/KD/%5BWebUI%5D+Wait+For+Element+Visible) step before the step having this issue. For example:

```groovy
WebUI.openBrowser('http://demoaut.katalon.com')
WebUI.waitForElementVisible(findtestObject('btn_Login'), 30)
WebUI.click(findTestObject('btn_Login'))
```

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
                <ul>
                    com.kms.katalon.core.webui.exception.WebElementNotFoundException: Web element with id ... not found.</td>
            <td>
                <ul>
                    <li>Update WebDriver via the Katalon tool:</li>
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
            <td>Carthage&nbsp;is not found</td>
            <td>Known issue of Appium 1.7 with Xcode 9:&nbsp;<a class="external-link" href="https://github.com/appium/appium/issues/9344" rel="nofollow">https://github.com/appium/appium/issues/9344</a>, so please use Katalon Studio 5.1.0.2+ to avoid this message.</td>
        </tr>
        <tr>
            <td>Unable to Start Application on this device: Appium directory is invalid.</td>
            <td>
                <p>Katalon Studio cannot locate the provided Appium directory. Please double check your Appium directory to make sure it should be as shown below:</p>
                <p>Windows: (Window&nbsp;→ Katalon Studio Preferences&nbsp;→ Mobile&nbsp;→ Appium Directory)</p>
                <pre><code class="language-groovy">C:\Users\&lt;Username&gt;\AppData\Roaming\npm\node_modules\appium</code></pre>
                <p>MacOS/Linux: (Katalon Studio&nbsp;→ Preferences&nbsp;→ Mobile&nbsp;→ Appium Directory)</p>
                <pre><code class="language-groovy">/usr/local/lib/node_modules/appium</code></pre>
            </td>
        </tr>
        <tr>
            <td>Root cause: com.kms.katalon.core.appium.exception.AppiumStartException: Appium directory is not set</td>
            <td>
                <p> When running tests with <strong>Katalon Runtime Engine</strong>, by default Katalon checks the Appium directory at:</p>
                <ul>
                  <li>APPIUM_HOME environment variable (*) </li>
                  <li>Windows: C:\Users<Username>\AppData\Roaming\npm\node_modules\appium</li>
                  <li>macOS and Linux: /usr/local/lib/node_modules/appium</li>
                </ul>
                <p> (*) To set Appium location by using APPIUM_HOME environment variable:
                <li>Windows: <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/roubleshooting-automated-mobile-testing/windows-appium-home.png"></li>
                <li>macOS and Linux: <pre><code class="language-groovy">export APPIUM_HOME=/usr/local/lib/node_modules/appium</code></pre></li>
                </p>
            </td>
        </tr>
    </tbody>
</table>
