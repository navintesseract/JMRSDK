# Virtual Controller / Virtual Keyboard for JioGlass

{% hint style="warning" %}
The Virtual Controller and Virtual Keyboard will only work in the JioGlass Lite ecosystem. Not compatible with JioPrism (Holoboard) and JioDive.
{% endhint %}

Virtual Controller and Virtual Keyboard are supported since JMRSDK 4.12.4. They allows the smartphone to become the controller when used with JioGlass Lite.

JMRSDK 4.24.1 onwards, developers can now check whether the application is using a Virtual Controller, Physical Controller, or Gaze mode to update their tutorial screens with respective images and specific controller binding.&#x20;

* Example Usage -&#x20;

```csharp
private InteractionDeviceType deviceType; 
deviceType = JMRInteractionManager.Instance.GetSupportedInteractionDeviceType();
```

![Virtual Controller and its functions](<../.gitbook/assets/VC Keybinding.png>)

Get the JioGlass Lite renders from [here](https://tesseractpvt-my.sharepoint.com/:f:/g/personal/virendra_tesseract_in/EoFrakY5K7RBkZv8zioMXIUBgzA6RP86w7-_bIG2-C624w?e=OPYnO9).
