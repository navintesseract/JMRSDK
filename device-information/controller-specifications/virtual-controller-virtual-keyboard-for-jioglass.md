# Virtual Controller / Virtual Keyboard for JioGlass

{% hint style="warning" %}
The virtual Controller and Keyboard will only work in the JioGlass smartphone ecosystem. Not compatible with Jio Prism (Holoboard) and Jio Dive.
{% endhint %}

We are launching Virtual Controller and Virtual Keyboard support since JMRSDK 4.12.4 allows the smartphone to become the controller when used with JioGlass (Not compatible with Jio Prism (Holoboard) and Jio Dive).

JMRSDK 4.24.1 onwards, developers can now check whether the application is using a Virtual Controller or a Physical Controller to update their tutorial screens with VC Image and any specific controller binding.&#x20;

* Example Usage -&#x20;

```csharp
private InteractionDeviceType deviceType; 
deviceType = JMRInteractionManager.Instance.GetSupportedInteractionDeviceType();
```

![Virtual Controller and its functions](<../../.gitbook/assets/VC Keybinding.png>)

Get the JioGlass Lite renders from [here](https://tesseractpvt-my.sharepoint.com/:f:/g/personal/virendra_tesseract_in/EoFrakY5K7RBkZv8zioMXIUBgzA6RP86w7-_bIG2-C624w?e=OPYnO9).
