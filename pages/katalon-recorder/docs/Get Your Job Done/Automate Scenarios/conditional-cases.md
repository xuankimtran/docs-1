---
title: "Handle conditional cases"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-recorder/docs/conditional-cases.html
description:
---

Handling conditional cases may become important when you want your scenarios to be executes successfully under different circumstances. An example of that is a workflow executed on a website whose functionality depends on the log-in state. You have to log in first to use the functionality, and you have to use the functionality after log in.

The test scenario

1.  Go to <https://katalon-demo-cura.herokuapp.com/>
2.  If you are not logged in, go to **Log in** screen then log in into the system. Otherwise, skip this step.
3.  Select **Hongkong CURA Healthcare Center** in the **Facility** drop down

## Record the scenario

1/ Start recording on Katalon Recorder

![](../../images/katalon-recorder/docs/conditional-cases/media/image1.png)

2/ On the Chrome\'s active tab, go to <https://katalon-demo-cura.herokuapp.com/>

_Notes: Make sure that you are not logged in._

3/ Click on the hamburger menu then click on Login link

![](../../images/katalon-recorder/docs/conditional-cases/media/image2.png)

4/ Input the Username and Password that are on the screen

![](../../images/katalon-recorder/docs/conditional-cases/media/image3.jpeg)

5/ Select 'Hongkong CURA Healthcare Center' in the Facility drop down

![](../../images/katalon-recorder/docs/conditional-cases/media/image4.png)

Then, you got this automated steps

![](../../images/katalon-recorder/docs/conditional-cases/media/image5.png)

6/ Run the test, it will be failed due to there is no Login link

![](../../images/katalon-recorder/docs/conditional-cases/media/image6.jpeg)

7/ Manually log out the web, then run the test again, it should be passed

![](../../images/katalon-recorder/docs/conditional-cases/media/image7.jpeg)

## Add conditional statements

Manually add **IF statement** to check the log-in state. If user is already logged in, then we want to only select the value. Otherwise, we want to log in into the system first.

1/ Add a new test step after Open command

![](../../images/katalon-recorder/docs/conditional-cases/media/image8.jpeg)

2/ Add storeElementPresent step to store a value into a variable

![](../../images/katalon-recorder/docs/conditional-cases/media/image9.jpeg)

3/ Add IF statement after storeElementPresent command

![](../../images/katalon-recorder/docs/conditional-cases/media/image10.jpeg)

4/ Add ELSE statement before Select facility command

![](../../images/katalon-recorder/docs/conditional-cases/media/image11.jpeg)

5/ Run the test several times

The test case should be passed for both cases, logged and not logged in.

![](../../images/katalon-recorder/docs/conditional-cases/media/image12.jpeg)
