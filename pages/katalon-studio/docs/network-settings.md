---
title: "Network Settings" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/network-settings.html 
redirect_from:
    - "/display/KD/Network+Settings/"
    - "/display/KD/Network%20Settings/"
    - "/x/gQ1O/"
    - "/katalon-studio/docs/network-settings/"
description: 
---

## Certificate settings

Katalon Studio supports the capability to bypass certificate validation so that users with protected network policy can work with Katalon Studio as usual. Go to **Project > Settings > Network**:

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/project-settings-network.png)

You are giving two options, including **None** or **Bypass certificate validation**.

* None
* Bypass certificate validation

The configuration here affects both WebUI and Web Service testings.

## Client certificate settings

> Please be noted that the setting for **Client certificate** is only available for **Katalon Studio Enterprise** users.
>
> This setting is only applied for requests in API/Web Services projects.

Katalon Studio can be configured to use the Client Certificate for all requests. To sign all the requests from Katalon Studio, specify the full path to your KeyStore file and the KeyStore Password. The recommended key store format is **PKCS #12** (.p12).

### Create a Certificate

To generate public and private key pairs (KeyStore and KeyStore Password) for the above configuration, you can use the keytool utility that is included in the JDK installation.

1. Open the command prompt and navigate to the bin folder in the JDK folder.

2. Run this command to create a KeyStore:

   `keytool -genkey -alias katalon -keyalg RSA -keystore katalon.keystore`

3. Enter a password for the new KeyStore and provide the utility with the required information (your name, the name of your organization, and etc).

To export a certificate with your public key, run the this command:
`keytool -export -alias katalon -file katalon.cer -keystore katalon.keystore`.
