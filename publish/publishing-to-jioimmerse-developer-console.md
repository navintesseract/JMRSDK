# Publishing to JioImmerse Developer Console

The Application should be published in the Google Play console and JioImmerse Developer console so that they can be published on JioVerse

{% hint style="info" %}
Suppose you are updating an existing application on the JioGlass Developer Console. In that case, you can skip the below steps and follow the usual process to update your application as mentioned in updating the App section.&#x20;
{% endhint %}

### How to Setup an Account on Developer Console and Upload an App

* The developer can access the Developer console from here [https://developer.tesseract.in/](https://developer.tesseract.in/)
* For creating an account on Developer Console refer to [this](https://tesseractpvt-my.sharepoint.com/:b:/g/personal/developer_tesseract_in/EUK6YjFqtQBFict7fhQQFkIBMTog1T5J-Ze1C3czU6e9zA?e=3UZpZc).
* For Jio Prism and Jio Dive, you must only follow Similar Steps but select a Different Platform while creating the App.

<figure><img src="../.gitbook/assets/image (124).png" alt=""><figcaption><p>Create New App</p></figcaption></figure>

* Select the Platform and fill in all the details
  1. Platform: Select the Platform(s) for which you are uploading an app - **Jio Glass Lite, Jio Prism, and JioDive.**
  2. App Name: Name of the Application.&#x20;
  3. Application type: 3D application.
  4. Package Name: The package name of the application that you have built the application within Unity.

<figure><img src="../.gitbook/assets/MicrosoftTeams-image (5).png" alt=""><figcaption><p>Go to Project Settings >> Player >> In Identification >> Package Name</p></figcaption></figure>

{% hint style="success" %}
If you have already created an app on the console, you cannot change its package name.&#x20;

You do not need to create a new application if you have already created one for some device.
{% endhint %}

<figure><img src="../.gitbook/assets/2023-01-16-20-59-57.png" alt=""><figcaption></figcaption></figure>

* Store Listing: Fill in the store listing details (App Information, Upload Creatives, Upload Build)
* App Creatives  - Please Upload the App Logo, Thumbnails, and Banners as mentioned in the "Add Creative". Go to Manage >> Upload Creatives. \
  &#x20;

<figure><img src="../.gitbook/assets/image (127).png" alt=""><figcaption><p>Go to Manage >> Store Listing</p></figcaption></figure>

{% content-ref url="../building-and-testing/licensing-journey-in-android-jioimmerse.md" %}
[licensing-journey-in-android-jioimmerse.md](../building-and-testing/licensing-journey-in-android-jioimmerse.md)
{% endcontent-ref %}

{% content-ref url="../building-and-testing/licensing-journey-in-ios-jioimmerse.md" %}
[licensing-journey-in-ios-jioimmerse.md](../building-and-testing/licensing-journey-in-ios-jioimmerse.md)
{% endcontent-ref %}

* Licensing Journey - \
  Android only - Upload your application SHA1 key from Google Play Console in `App Information` section.

<figure><img src="../.gitbook/assets/image (126).png" alt=""><figcaption><p>Enter Application Signature in App Information</p></figcaption></figure>

* Licensing Journey - Get the key to implement in Unity for licensing.

{% hint style="info" %}
iOS - Only Production key works with iOS builds
{% endhint %}

<figure><img src="../.gitbook/assets/image (59).png" alt=""><figcaption><p>licensing the application</p></figcaption></figure>

### Screenshots and Visual Representation of App on the Jioverse

* The application must adhere to the JioImmerse brand guidelines. Please find the brand guidelines [here](branding-guidelines.md)
* Create and Publish High-Quality Images and Visual Representations of your Application on the Platform.
* These Screenshots must represent the Gameplay, App features, and User Experience.&#x20;
* You can also include Posters of your Application as well.&#x20;

{% hint style="warning" %}
Note: The Creatives will be live on the platform only when you upload a build with it. E.g. If your Application is already published on the platform, and you decided to change the images, you have to re-upload the images and then upload a new build along with it, for the new graphical assets to be visible on the XR App store.
{% endhint %}

<figure><img src="../.gitbook/assets/brave_MwRfLdsGj1.png" alt=""><figcaption><p>Click on Upload Creatives</p></figcaption></figure>

### Upload the Build and Under Review&#x20;

* After uploading the Creatives, Click on Release Management, as seen in the bottom left corner of the image.
* (Android) Enter the application PlayStore URL to redirect to, from the JioImmerse Developer Console.
* (IOS) Enter the deep-link URL to redirect to, from the JioImmerse Developer Console.
* In the Build Name section, **Only** mention the "Version" of the Application (which we have defined earlier)
* Upload the APK and mention the Release notes with the changes you have made in the Latest build of the application. &#x20;

<figure><img src="../.gitbook/assets/image (129).png" alt=""><figcaption><p>Upload the apk</p></figcaption></figure>

* Make sure to Submit and Publish to send the build for approval.

<figure><img src="../.gitbook/assets/brave_P4WymQAEqJ.png" alt=""><figcaption><p>Upload and build your application from here</p></figcaption></figure>

* Once the Application is approved, it will be visible under the platform/s for which it was published.
