---
description: Changelog for JMRSDK
---

# Changelog

## What's New!  <a href="#new-features-released" id="new-features-released"></a>

JMRSDK

* <mark style="color:yellow;">Added Support for JioGlass with iOS</mark>
* <mark style="color:yellow;">External Gamepad Support for Android & iOS</mark>
* <mark style="color:yellow;">Easier Deep Linking - Firebase is no longer required for deep linking and is handled automatically through URL schemas</mark>
* <mark style="color:yellow;">Webcast support for Android through WebRTC</mark>
* Toolkit V3 is a new design with a more glassy effect
* Android 14 support for JioGlass 6.0 and JioDive
* Improved Ray visibility upon launching the virtual controller from iOS
* Optimized functionality of all virtual controller actions

EDITOR

* Improved FOV Behavior&#x20;
* Manifest modification is now done through a Scriptable Object

{% content-ref url="../../controller-specifications/external-gamepad.md" %}
[external-gamepad.md](../../controller-specifications/external-gamepad.md)
{% endcontent-ref %}

{% content-ref url="../../building-and-testing/licensing-journey-in-ios-jioimmerse.md" %}
[licensing-journey-in-ios-jioimmerse.md](../../building-and-testing/licensing-journey-in-ios-jioimmerse.md)
{% endcontent-ref %}

## Known Issues <a href="#known-issues" id="known-issues"></a>

* Toolkit v1 (Deprecated) is not compatible with Virtual Keyboard.
* With the controller v2, the controller render is upside down.&#x20;
* \[Holoboard] JMRTrackerManager.Instance.GetHeadTransform() returns the x-axis tilted at +42.5.
* \[Editor] JMRRigManager.Instance.getDeviceID() returns 3 for Editor instead of 0.
