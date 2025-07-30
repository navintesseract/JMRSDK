# Application Requirements

## Important Notice

{% hint style="danger" %}
JMRSDK 4.57 is a mandatory LTS Update for all Developer Applications for iOS to function with the latest JioImmerse Ecosystem.

* To list your application in the JioVerse Store, it should have the minimum SDK requirement as follows:
  * Android&#x20;
    * Dive - 4.45 or higher
    * JioGlass - 4.45 or higher
  * iOS
    * Dive - 4.57 or higher
    * JioGlass - 4.57 or higher
* Please read the New Feature Released below carefully
* Please refer to the section - [Configuring your Project for Device](../building-and-testing/publishing-to-target-device/#configuring-your-project-for-the-build-device) and follow the steps to configure your project for JioGlass Ecosystem
* Please refer to the section - [Adding Category Tag In AndroidManifest ](../building-and-testing/publishing-to-target-device/#adding-category-tag-in-androidmanifest)to ensure that your application is reflected within the same category as it is uploaded on the developer console.
* Please refer to the section - [Publishing your Application Listing on the Developer Console for JioGlass Ecosystem](../publish/publishing-to-jioimmerse-developer-console.md)
* Developers are recommended to update their tutorial graphics with Physical Controllers and Virtual controllers by checking which Interaction device is active. Refer to the section [JioGlass Controller](../develop/controller-interactions.md) V3 and [Virtual Controller with Keyboard](../controller-specifications/virtual-controller.md) below for more information
{% endhint %}

When developing an application make sure of the following:

1. An instance of **JMRAnalyticsManager** should be present at all times with the environment set to **Production**.
2. In Manifest > Show Manifest > Setup`Device type, Interaction type, category, license key, and webcast support` correctly.
3. Make sure your application does not have Unity 2D splash screen.
4. The application should always have Back functionality.
5. The application should work with Home functionality as provided by the JMRSDK.
6. If using the Physical Controller, Virtual Controller, or Gamepad, include a tutorial for the respective active interaction device.
7. The application should be crash-free and should not lag (try to maintain 60 FPS)
8. The application should show a paused state when minimized and resumed or in case of [JioGlass device is removed](../interaction/device-state/#jioglass-methods).
9. Make sure to adhere to Google Play Console policies for Android and Apple App Store Connect policies for iOS.&#x20;

These points are cumulated to avoid rejection of an application in JioImmerse but are not limited to these.
