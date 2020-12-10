---
title: "joptsimple.IllegalOptionSpecificationException: is not a legal option character"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/troubleshoot-globalvariable-special-character.html
---

When running your tests in console mode, you may get the `joptsimple.IllegalOptionSpecificationException: is not a legal option character` error when your global  variables' names contain special characters like `$`, or a space. For instance:

* `-g_myVar="test"` (supported)
* `-g_$myVar="test"` (not supported)

> We recommend to give global variables a name without '$', and space.

```groovy
joptsimple.IllegalOptionSpecificationException: $ is not a legal option character
	at joptsimple.ParserRules.ensureLegalOptionCharacter(ParserRules.java:77)
	at joptsimple.ParserRules.ensureLegalOption(ParserRules.java:67)
	at joptsimple.ParserRules.ensureLegalOptions(ParserRules.java:72)
	at joptsimple.OptionParser.acceptsAll(OptionParser.java:267)
	at joptsimple.OptionParser.acceptsAll(OptionParser.java:260)
	at joptsimple.OptionParser.accepts(OptionParser.java:252)
	at com.kms.katalon.execution.console.ConsoleMain.acceptConsoleOptionList(ConsoleMain.java:421)
	at com.kms.katalon.execution.console.ConsoleMain.launch(ConsoleMain.java:217)
	at com.kms.katalon.console.application.Application.runConsole(Application.java:71)
	at com.kms.katalon.core.application.Application.runConsole(Application.java:93)
	at com.kms.katalon.core.application.Application.start(Application.java:72)
	at org.eclipse.equinox.internal.app.EclipseAppHandle.run(EclipseAppHandle.java:196)
	at org.eclipse.core.runtime.internal.adaptor.EclipseAppLauncher.runApplication(EclipseAppLauncher.java:134)
	at org.eclipse.core.runtime.internal.adaptor.EclipseAppLauncher.start(EclipseAppLauncher.java:104)
	at org.eclipse.core.runtime.adaptor.EclipseStarter.run(EclipseStarter.java:388)
	at org.eclipse.core.runtime.adaptor.EclipseStarter.run(EclipseStarter.java:243)
	at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)
	at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.lang.reflect.Method.invoke(Method.java:498)
	at org.eclipse.equinox.launcher.Main.invokeFramework(Main.java:673)
	at org.eclipse.equinox.launcher.Main.basicRun(Main.java:610)
	at org.eclipse.equinox.launcher.Main.run(Main.java:1519)
```

