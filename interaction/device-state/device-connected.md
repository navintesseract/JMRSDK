---
description: When the device is connected
---

# Device Connected

> public void OnConnected (JMRInteractionManager.InteractionDeviceType devType, int index, string val)

| Parameters            | Description               |
| --------------------- | ------------------------- |
| InteractionDeviceType | Type of device connected  |
| index                 | Index of connected device |
| name                  | Name of connected device  |

To get notified when the device is connected need to implement the callback method exposed through InteractionManager:&#x20;

OnConnected(JMRInteractionManager.InteractionDeviceType devType, int index, string val)

Interaction Manager will call this action when the device is connected.&#x20;

{% hint style="info" %}
Action will be called only when it’s subscribed to a method. Action must be subscribed to method with a matching signature.&#x20;
{% endhint %}

```csharp
using JMRSDK.InputModule;
using UnityEngine;

public class JMRDemoInteractionExample : MonoBehaviour
{  
    private void OnEnable()
    {
        JMRInteractionManager.OnConnected += OnConnect;
    } 
    private void OnDisable()
    {
        JMRInteractionManager.OnConnected -= OnConnect;
    }
    private void OnConnect(JMRInteractionManager.InteractionDeviceType devType, int index, string val)
    {
        //do something when connected
        JMRInteractionManager.InteractionDeviceType deviceType = devType;
        int deviceIndex = index;
        string deviceName = val;
    }
}
```
