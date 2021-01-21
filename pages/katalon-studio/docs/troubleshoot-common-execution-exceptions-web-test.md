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

## Handling WebDriver issues

### "org.openqa.selenium.SessionNotCreatedException: session not created: This version of ChromeDriver only supports Chrome version ..."

**Possible cause**:

Your WebDriver is not up to date.

**Suggested solution**:

You can update WebDriver via the Katalon tool. From the main toolbar, select **Tools > Update WebDrivers >** select the corresponding browser in the drop-down list.

## Handling issues of interacting with an element

### "com.kms.katalon.core.webui.exception.WebElementNotFoundException: Web element with id ... not found."

**Possible cause**:

The element can't be detected on the current page due to the incorrect XPath or CSS selectors.

**Suggested solutions**:

You can try one of the following solutions to resolve the issue:

* Correct the element's XPath locator. Here is how to identify XPath:

1. Open your page using Chrome.
2. Right-click on your desired test object and choose **Inspect**
3. In the **Elements** tab of **DevTools**, right-click on your target object and select **Copy** > **Copy XPath**.
4. Open your test object in Katalon Studio, update XPath property with the copied value.

* [Optimize object identification and tools](https://docs.katalon.com/katalon-studio/docs/optimizing-object-identification-and-tools.html)

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

*A warning for this method (contributed by Russ Thomas)*
Click-prevention techniques (overlays, spinners) are used to control the application state while the application is in a state of transition. Using any mechanism to subvert the app developer's intentions places the application into an unknown state,  a state the developer has deliberately guarded against – and renders the test case meaningless. (See Tip: [DO NOT CHANGE THE AUT THROUGH TEST CODE 2](https://forum.katalon.com/t/tip-do-not-change-the-aut-through-test-code/11938)). One should pay attention to this and consider the trade-off in using Javascript clicks.

```groovy
import com.kms.katalon.core.webui.common.WebUiCommonHelper

WebElement element = WebUiCommonHelper.findWebElement(findTestObject('your/object'),30)
WebUI.executeJavaScript("arguments[0].click", Arrays.asList(element))
```

> The exception you are looking for isn’t on this page?
>
> Leave a comment below.
