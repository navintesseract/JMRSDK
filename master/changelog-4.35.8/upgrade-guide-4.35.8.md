---
description: For JMRSDK 4.35.8
---

# Upgrade Guide 4.35.8

Upgrade Unity to 2021.3.x LTS

* To interact with Gaze and click on editor press \[j] on the keyboard
* To enable and disable the dock, developers can use `JMRSystemDockManager.Instance.ToggleDockVisiblity(bool)` function
* To enable and disable interaction, developers can use `JMRPointerManager.Instance.ToggleInteraction(bool, JMRPointerManager.PointingSource.Head)`

## <mark style="color:yellow;">Analytics</mark>

{% hint style="info" %}
<mark style="color:yellow;">This is a compulsory step to add the analytics manager to each of your scenes or as \`Dont destroy on load\`</mark>
{% endhint %}

#### Adding Analytics Manager as Don't Destroy On Load.

1. Create a C# script named `JMRAnalyticsDontDestroyOnLoad` as shown below.

```
using UnityEngine;

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
3. For IOS change the Analytics Env to Production from Pre-Production.

<img src="../../.gitbook/assets/image (1).png" alt="" data-size="original">

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

{% content-ref url="../../building-and-testing/branding-guidelines.md" %}
[branding-guidelines.md](../../building-and-testing/branding-guidelines.md)
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
