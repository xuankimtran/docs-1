---
title: "Troubleshoot common exception when executing in console mode"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/troubleshoot-executing-in-console-mode.html
redirect_from:
    - "/katalon-studio/docs/troubleshoot-globalvariable-special-character.html"

---

> Tips
>
> * Please use **Ctrl+F** to look for the exceptions and errors you have encountered quickly.
> * If the exception you are looking for is not documented, please leave go to the [Katalon forum](https://forum.katalon.com/) to have a better support.



<table>
	<tbody>
		<tr>
			<td><strong>Issue</strong></td>
			<td><strong>Solution</strong></td>
		</tr>
		<tr>
			<td>
				<div><br />
					<div>joptsimple.IllegalOptionSpecificationException: is not a legal option character&nbsp;</div>
					<div><details><summary>Expand to see the full log</summary>
							<pre><code>joptsimple.IllegalOptionSpecificationException: $ is not a legal option character at joptsimple.ParserRules.ensureLegalOptionCharacter(ParserRules.java:77) at joptsimple.ParserRules.ensureLegalOption(ParserRules.java:67) at joptsimple.ParserRules.ensureLegalOptions(ParserRules.java:72) at joptsimple.OptionParser.acceptsAll(OptionParser.java:267) at joptsimple.OptionParser.acceptsAll(OptionParser.java:260) at joptsimple.OptionParser.accepts(OptionParser.java:252) at com.kms.katalon.execution.console.ConsoleMain.acceptConsoleOptionList(ConsoleMain.java:421) at com.kms.katalon.execution.console.ConsoleMain.launch(ConsoleMain.java:217) at com.kms.katalon.console.application.Application.runConsole(Application.java:71) at com.kms.katalon.core.application.Application.runConsole(Application.java:93) at com.kms.katalon.core.application.Application.start(Application.java:72) at org.eclipse.equinox.internal.app.EclipseAppHandle.run(EclipseAppHandle.java:196) at org.eclipse.core.runtime.internal.adaptor.EclipseAppLauncher.runApplication(EclipseAppLauncher.java:134) at org.eclipse.core.runtime.internal.adaptor.EclipseAppLauncher.start(EclipseAppLauncher.java:104) at org.eclipse.core.runtime.adaptor.EclipseStarter.run(EclipseStarter.java:388) at org.eclipse.core.runtime.adaptor.EclipseStarter.run(EclipseStarter.java:243) at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method) at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62) at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43) at java.lang.reflect.Method.invoke(Method.java:498) at org.eclipse.equinox.launcher.Main.invokeFramework(Main.java:673) at org.eclipse.equinox.launcher.Main.basicRun(Main.java:610) at org.eclipse.equinox.launcher.Main.run(Main.java:1519)</code></pre>
						</details></div>
				</div>
			</td>
			<td>
				<p>This is because the name of your global variables might contain special characters like <code>$</code>, or a space. For instance:&nbsp;</p>
				<ul>
					<li><code>-g_myVar="test"</code> (supported)</li>
					<li><code>-g_$myVar="test"</code> (not supported)</li>
				</ul>
				<div>
					<div>
						<div>We recommend to give global variables a name without <code>$</code>, and/or a space.</div>
					</div>
				</div>
			</td>
		</tr>
		<tr>
			<td>
				<div>
					<div>
						<div>
							<div>
								<div>When executing tests in KRE in Windows with Chrome version 93.x or 94.x, users may come across the following error:</div>
							</div>
						</div>
					</div>
				</div>
				<div>
					<div>
						<div>
							<div>
								<div>
									<div>
										<pre><code>SessionNotCreatedException: Message: session not created from timeout: Timed out receiving message from renderer: 600.000</code></pre>
									</div>
								</div>
							</div>
						</div>
					</div>
				</div>
			</td>
			<td>
				<div>
					<div>
						<div>This is an issue from Chrome version 93.x and 94.x that doesn&rsquo;t allow the ChromeDriver to start as a Windows service.&nbsp;</div>
					</div>
				</div>
				<div>
					<div>
						<div>
							<div>
								<div>
									<div>There are two ways to solve this issue:</div>
									1. Downgrade to Chrome version 92.x</div>
								<div>2. Set <code>--disable-gpu</code> for the desired capability in <strong>Project Settings &gt; Desired Capabilities &gt; Web UI &gt; Chrome</strong>. Click <strong>Add</strong>, then input as follows:</div>
								<div>&nbsp;</div>
								<div>
									<table style="height: 31px;" width="172">
										<tbody>
											<tr>
												<td style="width: 50px;"><strong>Name</strong></td>
												<td style="width: 50px;"><strong>Type</strong></td>
												<td style="width: 50px;"><strong>Value</strong></td>
											</tr>
											<tr>
												<td style="width: 50px;">args</td>
												<td style="width: 50px;">List</td>
												<td style="width: 50px;">--disable-gpu</td>
											</tr>
										</tbody>
									</table>
									<p>&nbsp;</p>
								</div>
								<div><img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/troubleshoot/TC-TROUBLESHOOT-Set-desired-capability.png" alt="Set desired capabilities in chrome" width="100%" /></div>
							</div>
						</div>
					</div>
				</div>
				&nbsp;</td>
		</tr>
	</tbody>
</table>

