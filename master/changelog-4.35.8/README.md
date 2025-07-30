---
description: Changelog for JMRSDK 4.35.8
---

# Changelog 4.35.8

## Important Notice

{% hint style="danger" %}
JMRSDK 4.35 is an LTS Update for all Developer Applications to function with the latest JioImmerse Ecosystem.

* Your Application will not be listed on the iOS JioVerse Store if not upgraded to JMRSDK 4.35 in iOS.
* Your Application will not be listed on the Android JioVerse Store if not upgraded to >= JMRSDK 4.34 in Android.
* Please read the New Feature Released below carefully
* Please refer to the section - [Configuring your Project for Device](../../building-and-testing/publishing-to-target-device/#configuring-your-project-for-the-build-device) and follow the steps to configure your project for JioGlass Ecosystem
* Please refer to the section - [Adding Category Tag In AndroidManifest ](../../building-and-testing/publishing-to-target-device/#adding-category-tag-in-androidmanifest)to ensure that your application is reflected within the same category as it is uploaded on the developer console.
* Please refer to the section - [Publishing your Application Listing on the Developer Console for JioGlass Ecosystem](../../publish/publishing-to-jioimmerse-developer-console.md)
* Developers are recommended to update their tutorial graphics with Physical Controllers and Virtual controllers by checking which Interaction device is active. Refer to the section [JioGlass Controller](../../develop/controller-interactions.md) V3 and [Virtual Controller with Keyboard](../../controller-specifications/virtual-controller-virtual-keyboard-for-jioglass.md) below for more information
{% endhint %}

## What's New!  <a href="#new-features-released" id="new-features-released"></a>

* <mark style="color:green;">Added Support for iOS</mark>
* <mark style="color:yellow;">Licensing Journey has been added to link applications with JioImmerse.</mark>
* <mark style="color:yellow;">SDK has been optimized for better performance.</mark>

### Devices:

Introduced 3 different devices JioGlass Lite, JioPrism(Holoboard), and JioDive.

Optimization of 2d and 3d switch time.

### **Separation of JioGlass Lite, JioPrism, and JioDive Ecosystems**&#x20;

* The JioGlass product ecosystem is evolving with three separate product offerings for our customers – JioGlass Lite, JioPrism, and JioDive&#x20;
  * **JioGlass Lite** is an entertainment and gaming device for users who want to augment their smartphones with true AR capabilities using JioGlass.&#x20;
    * This will be the primary, cost-effective, and smartphone-enabled JioGlass offering.&#x20;
    * This ecosystem only supports 3DoF applications&#x20;
  * **Jio Prism (Holoboard)** is a smartphone-based AR offering with 3DoF support.
  * **JioDive** is a smartphone-based VR offering with 3DoF support.
* We are currently revamping the SDK for JioGlass Pro with 6DoF capabilities, and all developer applications published until now will ONLY be available on JioGlass Lite, JioPrism (Holoboard), and JioDive ecosystem.&#x20;
* Developers can now create and manage separate releases and app store listings for the JioGlass Lite, JioPrism (Holoboard), and JioDive ecosystems.&#x20;
  * Please refer to the section - [Configuring your Project for JioGlass Lite](../../building-and-testing/publishing-to-target-device/#configuring-your-project-for-the-build-device) and follow the steps to configure your project.&#x20;
  * Please refer to the section - [Configuring your Project for JioDive](../../building-and-testing/publishing-to-target-device/#configuring-your-project-for-the-build-device) and follow the steps to configure your project
  * Please refer to the section  - [Configuring your project for JioPrism](../../building-and-testing/publishing-to-target-device/#configuring-your-project-for-the-build-device) (Holoboard) and follow the steps to configure your project.&#x20;

### **Web Applications**

* Developers will now be able to create Web Applications from Developer Console
* Developers can find this enabled on the JioGlass Developer Console while creating a new Application Listing.
  * _Note – The web applications will only be accessible on JioGlass at the moment and not on Holoboard devices_

### **Developer Analytics**&#x20;

* Developers can learn how their app is performing among the Customers. They can find the Analytics section on their Developer Console, you can refer to [Developer Console Analytics](broken-reference).
* Developers will now have access to the following Analytics of their applications.
  * Number of installs Average&#x20;
  * Session Time of App&#x20;
  * DAU, MAU and Stickiness of App&#x20;
  * Lifetime Usage of App&#x20;
  * Average Rating

### **Virtual Controller with Keyboard**

* Virtual Controller with Keyboard support has been added for JioGlass&#x20;
* Developers are recommended to update their tutorial graphics with Virtual Controller by checking which Interaction device is active. Refer to the section [Virtual Controller with Keyboard](../../controller-specifications/virtual-controller-virtual-keyboard-for-jioglass.md) below for more information

### **Categories and Perfromance Optimization**&#x20;

* JioGlass Lite Applications will now appear categorized on the JioGlass Launcher screen based on the configuration set by the Developer while building the application from the Unity3D editor.
  * Please refer to the section - [Adding Category Tag In AndroidManifest](../../building-and-testing/publishing-to-target-device/#adding-category-tag-in-androidmanifest) to ensure that your application is reflected within the same category as it is uploaded on the developer console.
* Please refer to the Section - [Performance Optimization](../../building-and-testing/publishing-to-target-device/performance-optimization.md) to ensure latest arm64 architecture for the best performance of your application.

### **URP Support for JioGlass Lite and JioDive**

* Developers can take advantage of Unity’s Universal Rendering Pipeline to improve the graphics and performance of their applications&#x20;
* Please refer to the section - [URP Support](../../getting-started/urp-support/) to setup your project using Unity3D's Universal Render Pipeline

### **Backward / Forward Compatibility**

* JioGlass Lite Ecosystem installed on a user’s device and the JioGlass applications installed on the user’s device will always remain compatible&#x20;
* In case JioGlass Lite Ecosystem becomes updated, the user will not be able to view, interact or install any incompatible applications&#x20;
* In case any JioGlass application becomes incompatible with the user JioGlass Lite Ecosystem, the user will not be able to view or interact with it.
* This feature is enabled by default. Developers do not have to do anything to enable this feature.

## Known Issues <a href="#known-issues" id="known-issues"></a>

* Toolkit v1 is not compatible with Virtual Keyboard
* Existing applications using SDK versions prior to v4.27.10 will have to be recompiled with SDK v.4.27.10+ to make them compatible with Physical Controller, Virtual Controller, and Virtual Keyboard on smartphones, JioPrism and JioDive.
* With the controller v2, the controller render is upside down.&#x20;
