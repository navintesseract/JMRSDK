---
description: Scanning when device not connected
---

# Scanning for Device

> public void OnStartScan(JMRInteractionManager.InteractionDeviceType devType, int index)

| Parameters            | Description               |
| --------------------- | ------------------------- |
| InteractionDeviceType | Type of device connected  |
| index                 | Index of connected device |

To scan when the device is not connected need to implement the callback method exposed through InteractionManager:&#x20;

OnStartScan(JMRInteractionManager.InteractionDeviceType devType, int index)

Interaction Manager will call this action when the device is not connected

{% hint style="info" %}
Action will be called only when it’s subscribed to a method. Action must be subscribed to the method with a matching signature.
{% endhint %}

```csharp
using JMRSDK.InputModule;
using UnityEngine;

public class JMRInteractionExample : MonoBehaviour
{  
    private void OnEnable()
    {
        JMRInteractionManager.OnStartScanning += OnStartScan;
    } 
    private void OnDisable()
    {
        JMRInteractionManager.OnStartScanning -= OnStartScan;
    }
    private void OnStartScan(JMRInteractionManager.InteractionDeviceType devType, int index)
    {
        JMRInteractionManager.InteractionDeviceType deviceType= devType;
        int deviceIndex=index;
    }
}
```
