# Virtual Controller / Virtual Keyboard for JioGlass

{% hint style="warning" %}
Virtual Controller and Virtual Keyboard will only work with JioGlass. Not compatible with JioPrism (Holoboard) and JioDive.
{% endhint %}

<table><thead><tr><th>Compatability</th><th data-type="checkbox">Virtual Controller</th><th data-type="checkbox">Virtual Keyboard</th></tr></thead><tbody><tr><td>JioGlass</td><td>true</td><td>true</td></tr><tr><td>JioDive</td><td>false</td><td>false</td></tr><tr><td>JioPrism</td><td>false</td><td>false</td></tr></tbody></table>

Virtual Controller and Virtual Keyboard have been supported since JMRSDK 4.12.4. It allows the smartphone to become the controller when used with JioGlass Lite.

JMRSDK 4.24.1 onwards, developers can now check whether the application is using a Virtual Controller, Physical Controller, or Gaze mode to update their tutorial screens with respective images and specific controller binding.&#x20;

* Example Usage -&#x20;

```csharp
private InteractionDeviceType deviceType; 
deviceType = JMRInteractionManager.Instance.GetSupportedInteractionDeviceType();
```

![Virtual Controller and its functions](<../.gitbook/assets/VC Keybinding.png>)

Get the Virtual Controller render from [here](https://tesseractpvt-my.sharepoint.com/:f:/g/personal/virendra_tesseract_in/EoFrakY5K7RBkZv8zioMXIUBgzA6RP86w7-_bIG2-C624w?e=OPYnO9) or use the image below

<figure><img src="../.gitbook/assets/image (4).png" alt=""><figcaption><p>JioGlass render</p></figcaption></figure>
