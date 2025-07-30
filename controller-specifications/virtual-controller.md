# Virtual Controller

## Virtual Controller

The Virtual Controller allows the smartphone to act as a controller by utilizing the sensors of the smartphone.

{% hint style="info" %}
Virtual Controller only has single-touch functionality. Multi-tap functionality is not supported.
{% endhint %}

{% hint style="warning" %}
Virtual Controller and Virtual Keyboard will only work with JioGlass.&#x20;

Incompatible with JioPrism (Holoboard) and JioDive.
{% endhint %}

## Other features

* **Webcast**: Quickly activate the webcast feature. Detailed instructions are on the [Webcast](../jmrsdk/webcast.md) page.
* **Pocket Mode**: Allows users to eliminate unintended screen taps and swipes when their phone is in their pocket by disabling all touch inputs, except for rotational tracking.
* **VR Background**: Toggle the skybox visibility in either the left or right camera views. For more details, see the [Cameras](../develop/cameras.md) page. (Default - off)
* **Hand Preference**: Customize the ray origin in the applications for left or right-handed users based on user preference. (Default - Right-handed).

## Compatibility

<table><thead><tr><th>Compatability</th><th data-type="checkbox">Virtual Controller</th><th data-type="checkbox">Virtual Keyboard</th></tr></thead><tbody><tr><td>JioGlass</td><td>true</td><td>true</td></tr><tr><td>JioDive</td><td>false</td><td>false</td></tr><tr><td>JioPrism</td><td>false</td><td>false</td></tr></tbody></table>

### Checking Interaction Mode

To check whether the application uses a Virtual Controller, Physical Controller, or Gaze mode to update their tutorial screens with respective images and specific controller binding.&#x20;

* Example Usage -&#x20;

```csharp
private InteractionDeviceType deviceType; 
deviceType = JMRInteractionManager.Instance.GetSupportedInteractionDeviceType();
```

![Virtual Controller and its functions](<../.gitbook/assets/Frame 2147206544.png>)

## Virtual Controller Renders

Get the Virtual Controller renders or use the images below

{% file src="../.gitbook/assets/Virtual Controller Renders.zip" %}
5 png files - VC Right handed, VC Left handed, VC more options, Pocket mode, Pocket mode activated
{% endfile %}

<div align="center"><figure><img src="../.gitbook/assets/VC - right handed.png" alt="" width="180"><figcaption><p>Default - VC Right Handed</p></figcaption></figure> <figure><img src="../.gitbook/assets/VC - left handed.png" alt="" width="180"><figcaption><p>VC Left Handed</p></figcaption></figure></div>

<div align="center"><figure><img src="../.gitbook/assets/VC - more options (1).png" alt="" width="180"><figcaption><p>VC More Options</p></figcaption></figure> <figure><img src="../.gitbook/assets/Pocket mode - Activated.png" alt="" width="180"><figcaption><p>VC Pocket Mode</p></figcaption></figure></div>

## Virtual Keyboard

When using the Virtual Controller, if a keyboard input is required, the system seamlessly presents the Virtual Keyboard on the smartphone. This integration enables users to conveniently type using their smartphone's interface. This ensures smooth switching between control and typing functionalities, enhancing the overall user experience.
