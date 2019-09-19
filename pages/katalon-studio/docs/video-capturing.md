---
title: "Video Capturing" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/video-capturing.html 
redirect_from:
    - "/display/KD/Video+Capturing/"
    - "/display/KD/Video%20Capturing/"
    - "/x/qRJO/"
    - "/katalon-studio/docs/video-capturing/"
description: 
---
## Compatibility

> * [K-Lite Codec](https://www.codecguide.com/download_kl.htm) is recommended to play the Katalon Studio test execution video.
> * Support execution at Test Suite level.
> * Support all browsers **except for** Remote, Headless, Kobiton, Custom. For remote or headless browsers, it's recommended to use [Katalium Server](https://docs.katalon.com/katalium-server/docs/katalium-server-katalon-studio-remote-machine.html) to view captured sessions.
>
> * Recording **parallel execution** is **NOT** supported yet
>

Debugging can be time-consuming and challenging for many automation testers. Katalon Studio helps solve this problem by supporting users with the ability to capture test execution via video format. Users can enable video capturing feature in Project Settings.

Follow the steps below to see how to work with Katalon Studio video capturing feature

1.  After creating a test suite in Katalon Studio, select **Project > Settings** to open the _Project Settings dialog_ box. Navigate to the **Report** section.
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/video-capturing/image2017-8-25-143A243A12.png)  
      
    
2.  Check the "**Enable Video Recorder during execution**" option. By default, Katalon Studio only captures **Failed** test cases. However, users can select options to capture only the **Passed**/**Failed** test cases or both.  
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/video-capturing/image2017-8-25-153A43A45.png)  

    Video settings can be specified based on the preferences of users. Katalon Studio recommends AVI (`.avi`) format and low quality to save disk space. The higher the video quality is, the bigger the file size is.

* **Video format**: AVI (`.avi`) or MOV (`.mov`)

* **Video quality**: Low; Medium or High

3. After executing the test suite, navigate to the **Result** tab, you can view the list of test cases in the test cases table with its video attached accordingly. Click on the play icon in the 'Video' column to play the video. Test steps descriptions are embedded as a subtitle. For example, please take a look at below screenshot  
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/video-capturing/image2017-8-25-153A353A13.png)

By watching how the automated test was executed, the testing team can identify exactly where the test failed. Thus, time and resources are managed more efficiently and effectively.
