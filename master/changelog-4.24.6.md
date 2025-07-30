# Changelog - 4.24.6

## Important Notice

{% hint style="danger" %}
JMRSDK 4.24.6 is a Mandatory Update for all Developer Applications to function with the latest JioGlass Ecosystem

* Your Application will not be listed on the JioGlass Application Store if not upgraded to JMRSDK 4.24.6.
* Please read the [New Feature Released](changelog-4.24.6.md#new-features-released) below carefully
* Please refer to the section - [Configuring your Project for JioGlass Lite](../getting-started/setting-up-a-jio-mixed-reality-project-in-unity.md#configuring-your-project-for-jioglass-lite) and follow the steps to configure your project for JioGlass Lite Ecosystem
* Please refer to the section - [Adding Category Tag In AndroidManifest](../getting-started/setting-up-a-jio-mixed-reality-project-in-unity.md#adding-category-tag-in-androidmanifest) to ensure that your application is reflected within the same category as it is uploaded on the developer console.
* Please refer to the section - [Publishing your Application Listing on the Developer Console for JioGlass Lite Ecosystem](../publish/publishing-to-jioglass-developer-console.md)
* Developers are recommended to update their tutorial graphics with Virtual Controller by checking which Interaction device is active. Refer to the section [Virtual Controller with Keyboard](../interaction/virtual-controller-virtual-keyboard-for-jioglass.md) below for more information
{% endhint %}

{% hint style="danger" %}
Important notice for users upgrading to JMRSDK 4.12.4+ from any previous versions

* JMRInputField needs to be updated with the new prefab
* Toolkit v1 has been deprecated from JMRSDK 4.12.4, please upgrade to Toolkit v2 to enjoy the latest features and upgrades
{% endhint %}

## New Features Released <a href="#new-features-released" id="new-features-released"></a>

### **Separation of JioGlass Lite and JioGlass Pro Ecosystems**&#x20;

* The JioGlass product ecosystem is evolving with two separate product offerings for our customers – JioGlass Lite and JioGlass Pro&#x20;
  * **JioGlass Lite** is an entertainment and gaming device for users who want to augment their smartphones with true AR capabilities using JioGlass.&#x20;
    * This is going to be the primary, cost-effective and smartphone-enabled JioGlass offering.&#x20;
    * This ecosystem only supports 3DoF applications&#x20;
  * **JioGlass Pro** is a standalone gaming powerhouse with 6DoF support which will be released to developers very soon.
    * This is going to be a more niche, heavy duty and standalone JioGlass offering. This ecosystem will support both 6DoF and 3DoF applications.&#x20;
* We are currently revamping the SDK for JioGlass Pro with 6DoF capabilities, and all developer applications published until now will ONLY be available on the JioGlass Lite ecosystem.&#x20;
* Developers will now be able to create and manage separate releases and app store listings for the JioGlass Lite and JioGlass Pro ecosystems.&#x20;
  * Please refer to the section - [Configuring your Project for JioGlass Lite](../getting-started/setting-up-a-jio-mixed-reality-project-in-unity.md#configuring-your-project-for-jioglass-lite) and follow the steps to configure your project for JioGlass Lite Ecosystem
  * Please refer to the section - [Adding Category Tag In AndroidManifest](../getting-started/setting-up-a-jio-mixed-reality-project-in-unity.md#adding-category-tag-in-androidmanifest) to ensure that your application is reflected within the same category as it is uploaded on the developer console.

### **Web Applications**

* Developers will now be able to create Web Applications from Developer Console
* Developers can find this enabled on the JioGlass Developer Console while creating a new Application Listing.
  * _Note – The web applications will only be accessible on JioGlass at the moment and not on Holoboard devices_

### **Developer Analytics**&#x20;

* Developers will now have access to the following Analytics of their applications.
  * Number of installs Average&#x20;
  * Session Time of App&#x20;
  * DAU, MAU and Stickiness of App&#x20;
  * Lifetime Usage of App&#x20;
  * Average Rating
* Developers can find the Analytics section on their Developer Console

### **Virtual Controller with Keyboard**

* Virtual Controller with Keyboard support has been added for JioGlass&#x20;
* Developers are recommended to update their tutorial graphics with Virtual Controller by checking which Interaction device is active. Refer to the section [Virtual Controller with Keyboard](../interaction/virtual-controller-virtual-keyboard-for-jioglass.md) below for more information

### **Categories**

* JioGlass Lite Applications will now appear categorized on the JioGlass Launcher screen based on the configuration set by the Developer while building the application from the Unity3D editor.
  * Please refer to the section - [Adding Category Tag In AndroidManifest](../getting-started/setting-up-a-jio-mixed-reality-project-in-unity.md#adding-category-tag-in-androidmanifest) to ensure that your application is reflected within the same category as it is uploaded on the developer console.

### **URP Support for JioGlass and Holoboard**&#x20;

* Developers can take advantage of Unity’s Universal Rendering Pipeline to improve the graphics and performance of their applications&#x20;
  * Please refer to the section - [URP Support](broken-reference) to setup your project using Unity3D's Universal Render Pipeline

### **Backward / Forward Compatibility**

* JioGlass Lite Ecosystem installed on a user’s device and the JioGlass applications installed on the user’s device will always remain compatible&#x20;
* In case JioGlass Lite Ecosystem becomes updated, the user will not be able to view, interact or install any incompatible applications&#x20;
* In case any JioGlass application becomes incompatible with the user JioGlass Lite Ecosystem, the user will not be able to view or interact with it.
* This feature is enabled by default. Developers do not have to do anything to enable this feature.

## Bugfixes <a href="#bugfixes" id="bugfixes"></a>

NA

## Known Issues <a href="#known-issues" id="known-issues"></a>

* Toolkit v1 is not compatible with Virtual Keyboard
* Existing applications using SDK versions prior to v4.24.1 will have to be recompiled with SDK v.4.24.1+ to make them compatible with Virtual Controller and Virtual Keyboard on smartphones

\
