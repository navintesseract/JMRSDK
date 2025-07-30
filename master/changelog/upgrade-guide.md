---
description: For JMRSDK
---

# Upgrade Guide

## Steps to upgrade JMRSDK

Upgrade Unity to **2021.3.x** LTS for best support

* Import JMRSDK Core package\
  Import JMRSDK Toolkit package\
  If using URP, Import JMRSDK URP package
* <mark style="background-color:yellow;">After importing the SDK for android platform, please add WebRTC package through the git url here:</mark> `com.unity.webrtc@3.0.0-pre.6`
* Add the Analytics Manager to each of your scenes or as \`DontDestroyOnLoad\` and change the Analytics Env to **Production**.
* Select category and interaction device type.
* In Hierarchy select JMRMixedReality > Input Manager > \
  In Inspector select JMRPointerManager > Select Pointer Source as Jio Glass Controller for best compatibility with all input sources.
* Make your application interactable with supported interaction sources.
* In your application have a tutorial for input sources (Gaze, Virtual Controller, Physical Controller, Gamepad) that are being used in your application.&#x20;
* Go through the [Application Requirements](../application-requirements.md) and ensure your application is compatible.

Publish your application.

## <mark style="color:yellow;">JioGlass Device State</mark>

The application should show a paused state of the application when minimized and resumed or in case of [JioGlass device is removed](../../interaction/device-state/#jioglass-methods) from the user's face.

## <mark style="color:yellow;">Important APIs</mark>

Getting the JioGlass proximity sensor to pause the application

{% content-ref url="../../interaction/device-state/jioglass-device-state.md" %}
[jioglass-device-state.md](../../interaction/device-state/jioglass-device-state.md)
{% endcontent-ref %}

Getting Device Type

{% content-ref url="../../interaction/device-state/" %}
[device-state](../../interaction/device-state/)
{% endcontent-ref %}

Getting currently active input source

{% content-ref url="../../interaction/interaction/active-input-source.md" %}
[active-input-source.md](../../interaction/interaction/active-input-source.md)
{% endcontent-ref %}

## <mark style="color:yellow;">Analytics</mark>

{% content-ref url="../../getting-started/setting-up-a-jio-mixed-reality-project-in-unity.md" %}
[setting-up-a-jio-mixed-reality-project-in-unity.md](../../getting-started/setting-up-a-jio-mixed-reality-project-in-unity.md)
{% endcontent-ref %}

{% hint style="info" %}
<mark style="color:yellow;">This is compulsory to add the analytics manager to each of your scenes or as \`Dont destroy on load\` and change the</mark> <mark style="color:yellow;">Analytics Env to</mark> <mark style="color:yellow;"></mark><mark style="color:yellow;">**Production**</mark>.
{% endhint %}

#### Adding Analytics Manager as Don't Destroy On Load.

1. Create a C# script named `JMRAnalyticsDontDestroyOnLoad` as shown below.

```csharp
using UnityEngine;
using JMRSDK;
public class JMRAnalyticsDontDestroyOnLoad : JMRAnalyticsManager
{
    void Start()
    {
        transform.parent = null;
        DontDestroyOnLoad(gameObject);
    }
}
```

2. In the first scene of your application, create an empty gameobject and add `JMRAnalyticsDontDestroyOnLoad` script on the same gameobject.
3. Change the Analytics Env to <mark style="color:yellow;">**Production**</mark>.

<img src="../../.gitbook/assets/image (15).png" alt="" data-size="original">

{% hint style="info" %}
Alternate Method: JMRAnalyticsManager can also be added to any game object in each scene of the project.
{% endhint %}

### iOS Publishing

Refer to the following pages to get your application live on iOS JioImmerse.

{% content-ref url="../../publish/publishing-to-apple-store.md" %}
[publishing-to-apple-store.md](../../publish/publishing-to-apple-store.md)
{% endcontent-ref %}

{% content-ref url="../../publish/ios-deep-linking.md" %}
[ios-deep-linking.md](../../publish/ios-deep-linking.md)
{% endcontent-ref %}

{% content-ref url="../../publish/branding-guidelines.md" %}
[branding-guidelines.md](../../publish/branding-guidelines.md)
{% endcontent-ref %}

### Gaze

{% hint style="danger" %}
Important notice for users upgrading to JMRSDK 4.30.0+ from any previous versions

JMRGazeAndDwellInteraction script has been renamed to JMRGazeInteraction as it now functions with gaze and dwell with gaze and click as well.

Therefore all applications using gaze and dwell before JMRSDK 4.30 will get a missing component error in unity and will have to replace the JMRGazeAndDwellInteraction component with JMRGazeInteraction.
{% endhint %}

### Toolkit

{% hint style="danger" %}
Important notice for users upgrading to JMRSDK 4.12.4+ from any previous versions

* JMRInputField needs to be updated with the new prefab
* Toolkit v1 has been deprecated from JMRSDK 4.12.4, please upgrade to Toolkit v2 to enjoy the latest features and upgrades
{% endhint %}
