# Device Disconnected

> Public void OnDisconnect(JMRInteractionManager.InteractionDeviceType devType, int index, string val)

| Parameters            | Description               |
| --------------------- | ------------------------- |
| InteractionDeviceType | Type of device connected  |
| index                 | Index of connected device |
| name                  | Name of connected device  |

To get notified when the device is disconnected need to implement callback method exposed through InteractionManager:&#x20;

OnDisconnected(JMRInteractionManager.InteractionDeviceType devType, int index, string val)

Interaction Manager will call this action when the device is connected

{% hint style="info" %}
Action will be called only when it’s subscribed to a method. Action must be subscribed to a method with a matching signature.
{% endhint %}

```csharp
using JMRSDK.InputModule;
using UnityEngine;

public class JMRInteractionExample : MonoBehaviour
{  
    private void OnEnable()
    {
        JMRInteractionManager. OnDisconnected += OnDisconnect;
    } 
    private void OnDisable()
    {
        JMRInteractionManager. OnDisconnected -= OnDisconnect;
    }
    private void OnDisconnect(JMRInteractionManager.InteractionDeviceType devType, int index, string val)
    {
        //do something when connected
        JMRInteractionManager.InteractionDeviceType deviceType= devType;
        int deviceIndex=index;
        string DeviceName=val;
    }
}
```
