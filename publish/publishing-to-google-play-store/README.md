# Publishing to Google Play Store

Player Settings for Publishing to Play Store

* Set Minimum Api level to API level 28 for Android 9.0 Pie
* Target API level to API level 34 for Android 14
* The scripting level backend has to be set to IL2CPP with ARM64 supported.

{% hint style="info" %}
You might need to upgrade your Target API level to API level 34.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

For build errors, refer:

{% content-ref url="../../troubleshooting/faqs-building-to-device/" %}
[faqs-building-to-device](../../troubleshooting/faqs-building-to-device/)
{% endcontent-ref %}

{% content-ref url="../../troubleshooting/faqs-develop.md" %}
[faqs-develop.md](../../troubleshooting/faqs-develop.md)
{% endcontent-ref %}

{% hint style="danger" %}
Add a custom keystore and not publish with a debug key.

Keep your keystore safe as it will be required to create new updates in the Play Store and Developer Console.
{% endhint %}

If your application size is more than 200 MB, check the split application binary checkbox, as shown in the image.

<figure><img src="../../.gitbook/assets/brave_FHR32dPuUs.png" alt=""><figcaption></figcaption></figure>

## Build Settings for Publishing to Play Store

Select Build App Bundle (Google Play) as the play store does not allow publishing of apk.

<figure><img src="../../.gitbook/assets/Build Settings (2).png" alt=""><figcaption></figcaption></figure>

## Note for Publishing on Play Store with JMRSDK

{% hint style="warning" %}
In the Play Console, it has to be mentioned that the application will not work without the JioImmerse application, as it will cause issues with their testing process.
{% endhint %}

Mention app access for Google App Review:

Goto App content > App Access > Manage

<figure><img src="../../.gitbook/assets/image (130).png" alt=""><figcaption></figcaption></figure>

Select All or some functionality in my app is restricted.

Add an instruction to open the app from JioImmerse.

_Sample for JioDive apps:_

> **Instruction name**: JioImmerse Required
>
> **Any other information required to access your app:** \
> After installing this application, install JioImmerse app and login into it, open JioDive mode. Goto Home in JioImmerse. Select this app. For best experience use a VR cardboard device like JioDive.

<figure><img src="../../.gitbook/assets/image (131).png" alt=""><figcaption></figcaption></figure>

## Sharing the testing link

Goto your testing track > Testers > Copy link and share.

{% hint style="success" %}
The application must be on closed beta or internal testing with developertesseract@gmail.com as a tester.

On Tesseract's approval, the application shall further be asked to shift to a different track.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (51).png" alt=""><figcaption></figcaption></figure>
