---
description: licensing is important to validate the integrity of the application
---

# Licensing Journey In Android JioImmerse

_Use this developer console link to upload your application:_ [_developer.tesseract.in_](https://developer.tesseract.in/console)

{% embed url="https://developer.tesseract.in/console" %}
JioImmerse Developer Console
{% endembed %}

## Production Key

### Overview

To create a licensed application, the following steps have to be performed.

1. Get the application ready in unity.
2. Create a Google Play Console account, if you don't have one already.
3. Create an application in the Google Play Console and upload a build in internal testing track.
4. Get <mark style="color:yellow;">SHA1</mark> <mark style="color:yellow;"></mark><mark style="color:yellow;">**App**</mark> <mark style="color:yellow;"></mark><mark style="color:yellow;">Signing Certificate</mark> from the application in Google Play Console.
5. Create a project in JioImmerse Developer Console.
6. Create an application in JioImmerse Developer Console.
7. Enter the SHA1 key in the JioImmerse Developer Console.
8. Copy the production key from Dev Console and enter it in Editor > Configure License Key popup.
9. Your application is now licensed.

### Getting the SHA1 key from Play Console

1.  Goto your application in Play Console\


    (**Skip** steps 2 - 3, if a build has been uploaded in this Google Play App before).&#x20;
2.  Upload a build in the internal testing track.

    <div align="center" data-full-width="false"><figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure></div>
3.  Choose the signing key as `Use Google-generated` key for best security.\


    <div data-full-width="true"><figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure></div>
4. Goto Setup > App integrity > App signing\
   Copy the SHA-1 certificate fingerprint to be entered into the Developer Console.

<figure><img src="../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>

### Setting up licensing in Developer Console

Upload your application SHA1 key from the Play Store and enter it in the Application Signature on the Dev Console.

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

Get the production licensing key to upload in Unity.&#x20;

{% hint style="success" %}
* Debug Key - Debug key can be used to test your application.
* Production Key - This key has to be used for licensing the application to be available for users outside your team.
{% endhint %}

<figure><img src="../.gitbook/assets/image (44).png" alt=""><figcaption><p>Generating licensing key</p></figcaption></figure>

### Setting up licensing in Unity Editor

To build a licensed application compatible with JioImmerse:

1. Goto JioMixedReality > Manifest > Configure License Key and enter the debug / production key from Developer Console
2. Enter the key in the popup in the Unity editor and hit save.
3. The application is now licensed. Build the application. &#x20;

<div align="left"><figure><img src="../.gitbook/assets/image (51).png" alt=""><figcaption></figcaption></figure></div>

## Debug Key

### Overview

1. Get the application ready in unity.
2. Create a Google Play Console account, if you don't have one already.
3. Create an application in the Google Play Console, if not present for your application.
4. Upload a build in Google Play Console internal testing. &#x20;
5. Get the <mark style="color:yellow;">SHA1</mark> <mark style="color:yellow;"></mark><mark style="color:yellow;">**Upload**</mark> <mark style="color:yellow;">Signing Certificate</mark> from the application in Google Play Console.
6. Create a project in the JioImmerse Developer Console.
7. Create an application in the JioImmerse Developer Console.
8. Enter the upload SHA1 key in the JioImmerse Developer Console.
9. Copy the debug key from the Developer Console and enter it in the Editor > Configure License Key popup.
10. Your application is now licensed for you to test.
11. Login into your DemoXR application as a developer with developer console credentials.
12. Run your application with an active internet connection.

### Getting the Debug Key

1\. Copy the SHA-1 Key from the Google Play Console under the Upload Key certificate.

<figure><img src="../.gitbook/assets/image (114).png" alt=""><figcaption></figcaption></figure>

2\. Paste the copied SHA -1 key to JioImmerse Developer Console > Application Signature

<figure><img src="../.gitbook/assets/image (115).png" alt=""><figcaption></figcaption></figure>

3\. Generate and Copy the Debug key from the developer console.

<figure><img src="../.gitbook/assets/image (116).png" alt=""><figcaption></figcaption></figure>

4\. Paste your debug key in Unity > JioMixedReality > Manifest > Configure License Key

<figure><img src="../.gitbook/assets/image (117).png" alt=""><figcaption></figcaption></figure>

5\. Create a build and install it on your device to run directly.

6\. Login with <mark style="color:yellow;">your Jio Developer Console credential</mark> on the <mark style="color:yellow;">Demo XR</mark>.

{% hint style="info" %}
Debug key builds must <mark style="color:yellow;">NOT</mark> be uploaded on JioImmerse Developer Console or Google Play Console.
{% endhint %}
