---
description: Journey to publish on the apple store
---

# Publishing to Apple Store

Assuming that you have created your Apple developer account. If not, then check from [here](https://www.youtube.com/watch?v=dkdsjA4KR0g\&ab_channel=AppyPie).

## Configuring Unity&#x20;

<mark style="color:red;">Delete</mark> the Agora Folder.

<img src="../.gitbook/assets/Unity_ZlWspBthfR.png" alt="" data-size="original">

<mark style="color:red;">Delete</mark> the screencast folder from the JMRSDK.

![](../.gitbook/assets/Unity_vjs9waV5V7.png)

Goto Unity > Build Settings > Set the orientation to Auto Rotation.\
**Select Landscape Right and Portrait**&#x20;

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

In Build settings > Other settings > Identification > Enable Automatically Sign

Set the Target device to "iPhone only"

<figure><img src="../.gitbook/assets/Unity_vlTyPk8ODf.png" alt=""><figcaption></figcaption></figure>

Build the project for iOS in Unity Build Settings

***

## XCode

Open the project in the XCode.

<figure><img src="../.gitbook/assets/Screenshot 2023-07-14 at 8.03.38 PM (1).png" alt=""><figcaption></figcaption></figure>

Select the data folder under the project tab, there you will get multiple checkboxes for target membership. Select Unity-iPhone and UnityFramework

<figure><img src="../.gitbook/assets/ApplicationFrameHost_IMMhelrghJ.png" alt=""><figcaption></figcaption></figure>

### Unity-iPhone&#x20;

Select Unity-iPhone, there you will get the Build Settings, and set the "Enable Bitcode" to no.

<figure><img src="../.gitbook/assets/ApplicationFrameHost_MYqgLiiLzu (1).png" alt=""><figcaption></figcaption></figure>

Add push notification from the signing and bundle, while selecting the Unity-iPhone.

<figure><img src="../.gitbook/assets/ApplicationFrameHost_zIZlKlpcJj.png" alt=""><figcaption></figcaption></figure>

Select the team signing from the signing and bundle, after selecting the "All" tab.

<figure><img src="../.gitbook/assets/ApplicationFrameHost_L9KeTZX3gP (1).png" alt=""><figcaption></figcaption></figure>

## Licensing your iOS Application to work with JioImmerse

{% content-ref url="../building-and-testing/licensing-journey-in-ios-jioimmerse.md" %}
[licensing-journey-in-ios-jioimmerse.md](../building-and-testing/licensing-journey-in-ios-jioimmerse.md)
{% endcontent-ref %}

## Building and publishing the app

Create a build from Product > Build or use the Command + 'B' shortcut.

<figure><img src="../.gitbook/assets/Screenshot 2023-07-14 at 8.07.30 PM.png" alt=""><figcaption></figcaption></figure>

If the build fails, refer to FAQs

{% content-ref url="../troubleshooting/faqs-building-to-device/faqs-ios.md" %}
[faqs-ios.md](../troubleshooting/faqs-building-to-device/faqs-ios.md)
{% endcontent-ref %}

Create an Archive after your build is created from Product > Archive&#x20;

<figure><img src="../.gitbook/assets/Screenshot 2023-07-14 at 8.07.39 PM (1).png" alt=""><figcaption></figcaption></figure>

Then go to Window > Organizer, select your build and choose Distribute App

<figure><img src="../.gitbook/assets/ApplicationFrameHost_df9EiiRq7x.png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
If your build fails in distribution, you will receive a mail with the reason for failure.
{% endhint %}

***

## Deep linking

{% hint style="success" %}
Now You must perform [deep linking](ios-deep-linking.md) before proceeding with the build.
{% endhint %}

{% content-ref url="ios-deep-linking.md" %}
[ios-deep-linking.md](ios-deep-linking.md)
{% endcontent-ref %}

***

## App Store Connect

Goto [App Store Connect](https://appstoreconnect.apple.com/). Select My Apps.

Refer to [https://developer.apple.com/app-store-connect/](https://developer.apple.com/app-store-connect/) for publishing your application in iOS App Store.

***

### How to generate IPA file?

Once your archive is generated.

1. Select App Store Connect.&#x20;

<figure><img src="../.gitbook/assets/MicrosoftTeams-image (6).png" alt=""><figcaption></figcaption></figure>

2. Select Export

<figure><img src="../.gitbook/assets/MicrosoftTeams-image (7).png" alt=""><figcaption></figcaption></figure>

Proceed to generate the IPA file.
