# Publishing to Google Play Store

## Player Settings for Publishing to Play Store

* Set Minimum Api level to API level 28
* Target API level to API level 33
* Set Scripting level backend has to be set to IL2CPP with ARM64 supported.

{% hint style="info" %}
You might need to upgrade your Target API level to API level 33.
{% endhint %}

<figure><img src="../../.gitbook/assets/Player settings (3).png" alt=""><figcaption></figcaption></figure>

{% hint style="danger" %}
Make sure to add a custom keystore and not publish with debug key.

Keep your keystore safe as it will be required to create any new updates in the play store.
{% endhint %}

If your application size is more than 150 MB, you need to check the split application binary checkbox, as shown in the image.

<figure><img src="../../.gitbook/assets/Publishing Settings.png" alt=""><figcaption></figcaption></figure>

## Build Settings for Publishing to Play Store

Select Build App Bundle (Google Play) as the play store does not allow publishing of apk.

<figure><img src="../../.gitbook/assets/Build Settings.png" alt=""><figcaption></figcaption></figure>

## Note for Publishing on Play Store with JMRSDK

{% hint style="warning" %}
In the play store, it has to be mentioned that the application will not work without the JioImmerse application, as it will cause issues with the testing process of the play store.
{% endhint %}

### Sharing the testing link with testers

Goto your testing track > Testers > Copy link and share.

{% hint style="success" %}
The application has to be on closed beta testing with **ittesseract@gmail.com** as a tester.

On Tesseract's approval, the application shall further be asked to shift to a different track.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (55).png" alt=""><figcaption></figcaption></figure>
