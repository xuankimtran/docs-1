---
title: "Troubleshooting automated mobile testing" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/troubleshooting-automated-mobile-testing.html 
redirect_from:
    - "/display/KD/Troubleshooting+automated+mobile+testing/"
    - "/display/KD/Troubleshooting%20automated%20mobile%20testing/"
    - "/x/fBdO/"
    - "/katalon-studio/docs/troubleshooting-automated-mobile-testing/"
description: 
---
> * Please read **[Installation and Set-up](/display/KD/Before+You+Start)** guide first to set up your mobile. The information below is provided for those who can't get their mobile testing work properly after going through the set-up guide.

<table>
    <thead>
        <tr>
            <th>Issue</th>
            <th>Solution</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Connected device is not displayed in 'Device Name' list.</td>
            <td>
                <strong>iOS</strong>
                <ul>
                    <li>Connect your&nbsp;device to Xcode.</li>
                    <li>Go to Settings -&gt;&nbsp;Developer&nbsp;&gt; turn ON&nbsp;UIAutomation.</li>
                    <li>
                        <p>Check if your device is recognized using the following commands on Terminal.</p>
                        <pre><code class="language-groovy">cd /Applications/Katalon\ Studio.app/Contents/Eclipse/configuration/resources/tools/imobiledevice&nbsp;
idevice_id -l</code></pre>
                        <p>If your iOS version is iOS 11, make sure Katalon Studio's version is 5.3+.</p>
                    </li>
                </ul>
                <strong>Android</strong>
                <ul>
                    <li>Developer option is turned on.</li>
                    <li>A trusted&nbsp;connection is established by&nbsp;tapping&nbsp;on 'Trust this computer' whenever this dialog is displayed on your device.</li>
                    <li>
                        Check if the device is listed using&nbsp;adb&nbsp;command:
                        <ul>
                            <li>On Windows command line/ MacOS terminal: Navigate to platform-tools folder in &lt;Android SDK folder&gt;\platform-tools.</li>
                            <li>Type in "adb&nbsp;devices" and observe devices listed there. Make sure that your corrected device is listed there with online status.&nbsp;</li>
                        </ul>
                    </li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>xcodebuild exited with code&nbsp;'65'&nbsp;and signal&nbsp;'null'.</td>
            <td>
                <p>Your .ipa application and/or WebDriverAgent is not signed correctly.</p>
                Solutions:
                <ul>
                    <li>Sign and rebuild the WebDriverAgent XCode project with your developer certificate.</li>
                    <li>Uncheck 'Automatically Signing' option from WebDriverAgentRunner and select <strong>valid provisioning profile</strong> (profile displayed as Eligible from the list).</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Xcode fails to create a provisioning profile for the <code>WebDriverAgentRunner</code>&nbsp;target.</td>
            <td>
                <p>This necessitates manually changing the bundle id for the target by going into the "Build Settings" tab, and changing the "Product Bundle Identifier" from&nbsp;<code>com.facebook.WebDriverAgentRunner</code>&nbsp;to something that Xcode will accept.</p>
            </td>
        </tr>
        <tr>
            <td>Fail to start Appium server in 30 seconds.</td>
            <td>Katalon Studio can't start Appium server within 30 seconds (default timeout). You can increase this timeout value from this settings: Project&nbsp;→ Settings&nbsp;→ Execution&nbsp;→ Default&nbsp;→ Default wait for elements timeout (in seconds).</td>
        </tr>
        <tr>
            <td>
                <ul>
                    <li>Fail to start the Appium server in 60 seconds.</li>
                    <li>Original error: 'x.x.SplashActivity' never started.</li>
                </ul>
            </td>
            <td>
                <p>Set your Appium Log Level to "Debug" which you can find this option in Windows &gt; Katalon Studio Preferences &gt; Katalon &gt; Mobile to generate debug logs of Appium.</p>
                <p>After this change is applied, retry your record/spy session and then open generated&nbsp;.appium&nbsp;file in the project folder.&nbsp;<br>Somewhere in this file you are likely will see these lines:&nbsp;</p>
                <pre><code class="language-groovy">[debug] [ADB] Running '..\adb.exe' with args: [...] 
[debug] [ADB] Found package: 'com.abc.def.xyz' and fully qualified activity name : 'com.egh.jik' 
[debug] [ADB] Incorrect package and activity. Retrying.</code></pre>
                <p>&nbsp;</p>
                <p>The root cause is Katalon Studio can't start application due to incorrect package and activity by default, so you need to add additional settings to desired capabilities:&nbsp;</p>
                <p>&nbsp;-&nbsp;Navigate to Mobile settings (Project &gt; Settings &gt; Execution &gt; Default &gt; Mobile &gt; Android).&nbsp;<br>&nbsp;-&nbsp;Add the following key.<br>&nbsp; &nbsp;Name: appWaitActivity.&nbsp;<br>&nbsp; &nbsp;Value: com.* (<strong>based on the prefix of 'Found package' log</strong>).</p>
                <p><br></p>
            </td>
        </tr>
        <tr>
            <td>Carthage&nbsp;is not found.</td>
            <td>Known issue of Appium 1.7 with Xcode 9:&nbsp;<a class="external-link" href="https://github.com/appium/appium/issues/9344" rel="nofollow">https://github.com/appium/appium/issues/9344</a>, so please use Katalon Studio 5.1.0.2+ to avoid this message.</td>
        </tr>
        <tr>
            <td>Unable to Start Application on this device: Appium directory is invalid.</td>
            <td>
                <p>Katalon Studio cannot locate the provided Appium directory. Please double check your Appium directory to make sure it should be as shown below:</p>
                <p>Windows: (Window&nbsp;→ Katalon Studio Preferences&nbsp;→ Mobile&nbsp;→ Appium Directory).</p>
                <pre><code class="language-groovy">C:\Users\&lt;Username&gt;\AppData\Roaming\npm\node_modules\appium</code></pre>
                <p>MacOS/Linux: (Katalon Studio&nbsp;→ Preferences&nbsp;→ Mobile&nbsp;→ Appium Directory).</p>
                <pre><code class="language-groovy">/usr/local/lib/node_modules/appium</code></pre>
            </td>
        </tr>
        <tr>
            <td>Unable to Start Application while running Android tests on a Windows machine.</td>
            <td>
                <p>First, upgrade to the latest version of Appium.</p>
                <p>In Katalon Studio, go to <strong> Project Settings > Desired Capabilities > Mobile > Android</strong> and add this desired capabilities:
                    <ul>
                        <li>Name: <code>appWaitActivity</code></li>
                        <li>Type: String</li>
                        <li>Value: *</li>
                    </ul>
                <p><img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/roubleshooting-automated-mobile-testing/android-error.png" alt="desired capabilities" width=70%>
                <p>Click <strong>Apply</strong> to save, then run the test again.</p>    
            </td>
        </tr>
        <tr>
            <td>com.kms.katalon.core.appium.exception.AppiumStartException: Appium directory is not set.</td>
            <td>
                <p> When running tests with <strong>Katalon Runtime Engine</strong>, by default Katalon checks the Appium directory at:</p>
                <ul>
                  <li>APPIUM_HOME environment variable (*). </li>
                  <li>Windows: C:\Users<Username>\AppData\Roaming\npm\node_modules\appium.</li>
                  <li>macOS and Linux: /usr/local/lib/node_modules/appium.</li>
                </ul>
                <p> (*) To set Appium location by using APPIUM_HOME environment variable:
                <li>Windows: <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/roubleshooting-automated-mobile-testing/windows-appium-home.png"></li>
                <li>macOS and Linux: <pre><code class="language-groovy">export APPIUM_HOME=/usr/local/lib/node_modules/appium</code></pre></li>
                </p>
            </td>
        </tr>
        <tr>
            <td>java.util.concurrent.ExecutionException: org.openqa.selenium.WebDriverException: An unknown server-side error occurred while processing the command. Original error: Could not proxy command to the remote server. Original error: timeout of 240000ms exceeded.</td>
            <td>
                <p>Solution:</p>
                    <ol>
                        <li> Install <a href="https://docs.katalon.com/katalon-studio/docs/installing-webdriveragent-for-ios-devices.html">Webdriveragent</a>.</li>
                        <li> Kill the running appium proccesses with the following command:  <pre><code>killall -9 node</code></pre></li>
                        <li> Start the AUT again.</li>
                    </ul>
            </td>
        </tr>  
<tr>
            <td>Katalon Mobile Recorder and SetText keyword cannot perform on an <strong>EditText</strong> element of the Flutter-based application</td>
            <td>
                <p>Solution:</p>
                    <ol>
                        <li> Create a <a href="https://docs.katalon.com/katalon-studio/docs/flutter-based-application-testing.html">SetText Custom keyword</a>.</li>
                        <li> Run the test again in script mode.</li>
                    </ul>
            </td>
        </tr>                                 
    </tbody>
</table>
