---
title: "Slack Integration Plugin" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/slack-plugin-integration.html
redirect_from:
    - "/katalon-studio/docs/slack-integration.html"
    - "/display/KD/Slack+Integration/"
    - "/display/KD/Slack%20Integration/"
    - "/x/boUw/"
    - "/katalon-studio/docs/slack-integration/"
description: 
---
### Configure Slack plugin   
Go to **Project** > **Setting** > **Plugin**. 
Check the **Using Slack** checkbox. Next, provide all required information. Click **Test Connection** to make sure Katalon Studio and Slack are integrated.

Once the connection from Katalon Studio to your Slack team space has been successfully established, you can verify as below:

<center>
<img src="https://i.ibb.co/68wFsZN/Slack-2.png" width="550" >
</center>




### Obtain Slack OAuth authentication token

Log in to your Slack team space and navigate to the [Slack API App](https://api.slack.com/apps). Then create a Katalon Studio app.

Click on **OAuth & Permissions**

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/slack-plugin-integration/Slack_3.png) 

Scroll down to the **Scopes** section.  
Under **Select Permission Scopes**, choose all options: **Send messages as Katalon Studio**, **Send messages as user**, and **Access information about user's public channels** > **Save Changes**.  An authentication token will be generated. 

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/slack-plugin-integration/Slack_4.png) 
*Note*: If you forget to define Scopes to the chatbot, you will have to reinstall the app and define Scopes again.

### Obtain Slack Legacy token

Under Slack ‘Settings’, navigate to the [Legacy Tokens](http://api.slack.com/custom-integrations/legacy-tokens) page > click **Create token**.  
You may see the Request token if the Approved Apps feature is turned on for your workspace.

<center>
<img src="https://i.ibb.co/64PP0f8/Slack-5.png">
</center>

*Note*. After the configuration, messages will be automatically sent from Katalon Studio Slack Plugin once the test suite has been successfully executed.
