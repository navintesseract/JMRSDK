---
description: Changelog for JMRSDK
---

# Changelog 4.45

## Important Notice

{% hint style="danger" %}
JMRSDK 4.45 is a mandatory LTS Update for all Developer Applications to function with the latest JioImmerse Ecosystem.

* To list your application in the JioVerse Store, it should have the minimum SDK requirement as follows:
  * Android&#x20;
    * Dive - 4.45 or higher
    * JioGlass Lite - 4.45 or higher
  * iOS
    * Dive - 4.35 or higher
* Please read the New Feature Released below carefully
* Please refer to the section - [Configuring your Project for Device](../../building-and-testing/publishing-to-target-device/#configuring-your-project-for-the-build-device) and follow the steps to configure your project for JioGlass Ecosystem
* Please refer to the section - [Adding Category Tag In AndroidManifest ](../../building-and-testing/publishing-to-target-device/#adding-category-tag-in-androidmanifest)to ensure that your application is reflected within the same category as it is uploaded on the developer console.
* Please refer to the section - [Publishing your Application Listing on the Developer Console for JioGlass Ecosystem](../../publish/publishing-to-jioimmerse-developer-console.md)
* Developers are recommended to update their tutorial graphics with Physical Controllers and Virtual controllers by checking which Interaction device is active. Refer to the section [JioGlass Controller](../../develop/controller-interactions.md) V3 and [Virtual Controller with Keyboard](../../controller-specifications/virtual-controller-virtual-keyboard-for-jioglass.md) below for more information
{% endhint %}

## What's New!  <a href="#new-features-released" id="new-features-released"></a>

<mark style="color:green;">JMRSDK</mark>

* <mark style="color:green;">Support to build with Android 14.</mark>
* <mark style="color:green;">Toolkit V3 is a new design with a more glassy effect.</mark>
* <mark style="color:green;">Android 14 support for JioGlass 6.0 and JioDive.</mark>&#x20;
* <mark style="color:green;">Optimized JMRSDK analytics.</mark>
* <mark style="color:green;">Optimized VC Tracking.</mark>
* <mark style="color:green;">Enhanced dock behavior for JioDive.</mark>&#x20;
* <mark style="color:green;">Improved Ray visibility upon launching the virtual controller from iOS.</mark>&#x20;
* <mark style="color:green;">Optimized functionality of all virtual controller actions.</mark>&#x20;

<mark style="color:green;">EDITOR</mark>

* <mark style="color:green;">Improved FOV Behavior</mark>&#x20;
* <mark style="color:green;">Camera Skybox is visible by default in the Unity editor</mark>
* <mark style="color:green;">Manifest modification is now done through a Scriptable Object</mark>

<mark style="color:yellow;">External Gamepad Support for Android.</mark>

{% content-ref url="../../publish/licensing-journey-in-ios-jioimmerse.md" %}
[licensing-journey-in-ios-jioimmerse.md](../../publish/licensing-journey-in-ios-jioimmerse.md)
{% endcontent-ref %}

{% content-ref url="../../controller-specifications/external-gamepad.md" %}
[external-gamepad.md](../../controller-specifications/external-gamepad.md)
{% endcontent-ref %}

### Devices:

Introducing 3 devices - JioGlass Lite, JioPrism(Holoboard), and JioDive.

### **Separation of JioGlass Lite, JioPrism, and JioDive Ecosystems**&#x20;

* The JioGlass product ecosystem is evolving with three separate product offerings for our customers – JioGlass Lite, JioPrism, and JioDive&#x20;
  * **JioGlass Lite** is an entertainment and gaming device for users who want to augment their smartphones with true AR capabilities using JioGlass.&#x20;
    * This will be the primary, cost-effective, and smartphone-enabled JioGlass offering.&#x20;
    * This ecosystem only supports 3DoF applications&#x20;
  * **Jio Prism (Holoboard)** is a smartphone-based AR offering with 3DoF support.
  * **JioDive** is a smartphone-based VR offering with 3DoF support.

### **Virtual Controller with Keyboard**

* Virtual Controller with Keyboard support has been added for JioGlass&#x20;
* Developers are recommended to update their tutorial graphics with Virtual Controller by checking which Interaction device is active. Refer to the section [Virtual Controller with Keyboard](../../controller-specifications/virtual-controller-virtual-keyboard-for-jioglass.md) below for more information

### **Categories and Perfromance Optimization**&#x20;

* JioGlass Lite Applications will now appear categorized on the JioGlass Launcher screen based on the configuration set by the Developer while building the application from the Unity3D editor.
  * Please refer to the section - [Adding Category Tag In AndroidManifest](../../building-and-testing/publishing-to-target-device/#adding-category-tag-in-androidmanifest) to ensure that your application is reflected within the same category as it is uploaded on the developer console.
* Please refer to the Section - [Performance Optimization](../../building-and-testing/publishing-to-target-device/performance-optimization.md) to ensure latest arm64 architecture for the best performance of your application.

### **URP Support for JioGlass Lite and JioDive \[Android]**

* Developers can take advantage of Unity’s Universal Rendering Pipeline to improve the graphics and performance of their applications&#x20;
* Please refer to the section - [URP Support](../../getting-started/urp-support/) to setup your project using Unity's Universal Render Pipeline

### **Backward / Forward Compatibility**

* JioGlass Lite Ecosystem installed on a user’s device and the JioGlass applications installed on the user’s device will always remain compatible&#x20;
* In case JioGlass Lite Ecosystem becomes updated, the user will not be able to view, interact or install any incompatible applications&#x20;
* In case any JioGlass application becomes incompatible with the user JioGlass Lite Ecosystem, the user will not be able to view or interact with it.
* This feature is enabled by default. Developers do not have to do anything to enable this feature.

## Known Issues <a href="#known-issues" id="known-issues"></a>

* Toolkit v1 (Deprecated) is not compatible with Virtual Keyboard.
* With the controller v2, the controller render is upside down.&#x20;
* \[Holoboard] JMRTrackerManager.Instance.GetHeadTransform() returns x-axis tilted at +42.5.
* \[Editor] JMRRigManager.Instance.getDeviceID() returns 3 for Editor instead of 0.
