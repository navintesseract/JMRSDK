# Virtual Controller / Virtual Keyboard for JioGlass

{% hint style="danger" %}
JMRSDK 4.24.6 is a Mandatory Update for all Developer Applications to function with the latest JioGlass Ecosystem

* Your Application will not be listed on the JioGlass Application Store if not upgraded to JMRSDK 4.24.6
* Developers are recommended to update their tutorial graphics with Virtual Controller by checking which Interaction device is active. Refer below for example
{% endhint %}

{% hint style="warning" %}
Virtual Controller and Keyboard will only work in the JioGlass smartphone ecosystem (Not compatible with Holoboard).
{% endhint %}

We are launching Virtual Controller and Virtual Keyboard support since JMRSDK 4.12.4 that allows the smartphone to become the controller when used with JioGlass (Not compatible with Holoboard)

JMRSDK 4.24.1 onwards developers can now check whether the application is using a Virtual Controller or a Physical Controller to update their tutorial screens with VC Image as well as any specific controller binding.&#x20;

* Example Usage -&#x20;

```csharp
private InteractionDeviceType deviceType; 
deviceType = JMRInteractionManager.Instance.GetSupportedInteractionDeviceType();
```

![Virtual Controller and its functions](<../.gitbook/assets/VC Keybinding.png>)

Get the Lite renders from [here](https://tesseractpvt-my.sharepoint.com/:f:/g/personal/virendra_tesseract_in/EoFrakY5K7RBkZv8zioMXIUBgzA6RP86w7-_bIG2-C624w?e=OPYnO9)
