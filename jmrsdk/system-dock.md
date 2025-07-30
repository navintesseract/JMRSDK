---
description: Available for Gaze mode.
---

# System Dock

Gaze mode has a system dock to control the user's journey for reserved buttons of the controller.

<figure><img src="../.gitbook/assets/image (20).png" alt=""><figcaption><p>System Dock</p></figcaption></figure>

The dock provides the functionality of the back button, home button, and recenter button similar to that provided by the controller.

{% content-ref url="../controller-specifications/" %}
[controller-specifications](../controller-specifications/)
{% endcontent-ref %}

System Dock follows the user's head automatically to make sure that it is non-obtrusive as well as available to access all the time.

{% hint style="info" %}
Dock is shown automatically and is controlled by JMRSDK.
{% endhint %}

### Enable/Disable System Dock

If you want to enable/disable the dock and its interaction, you can use&#x20;

```csharp
JMRSystemDockManager.Instance.ToggleDockVisiblity(bool visible)
```

### Dock is not visible

If the dock is not visible in JioDive while in Gaze mode:

* Make sure that the controller is disconnected.&#x20;
*   In unity, the layer for System Dock shall be rendered by the left and right cameras in all the scenes.

    <figure><img src="../.gitbook/assets/image (54).png" alt=""><figcaption></figcaption></figure>

## Global back button

To complete the user's journey - minimize the application and return back to the companion app, the global back button is present.&#x20;

<figure><img src="../.gitbook/assets/image (60).png" alt=""><figcaption><p>Global back button</p></figcaption></figure>
