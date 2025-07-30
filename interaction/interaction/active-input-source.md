---
description: Get the information about the active input source
---

# Active Input Source

To get the currently active input _device_ in JMRSDK. JMRSDK provides a method to fetch it.

{% content-ref url="../device-state/controller-device-state.md" %}
[controller-device-state.md](../device-state/controller-device-state.md)
{% endcontent-ref %}

The `JMRInteractionManager.InteractionDeviceType` is an enum as follows:

<details>

<summary>public enum <code>JMRInteractionManager.InteractionDeviceType</code></summary>

JIOGLASS\_CONTROLLER = 1\
KEYBOARD = 2\
MOUSE = 3\
VIRTUAL\_CONRTOLLER = 4\
VIRTUAL\_KEYBOARD = 5\
EDITOR\_MOUSE = 6\
GAZE\_AND\_CLICK = 7\
GAZE\_AND\_DWELL = 8\
GAMEPAD = 9\
INVALID\_DEVICE\_TYPE = 0

</details>

To make a complete system that returns the currently active input **source,** use the code below.\
The currently active device can be fetched by calling the function `GetInteractionDeviceType()` in the below code. It returns the value of the enum `JMRInteractionManager.InteractionDeviceType`

```csharp
using JMRSDK.InputModule;
using UnityEngine;

public class InteractionDeviceFetcher : MonoBehaviour
{
    JMRInteractionManager.InteractionDeviceType _addedDevice = 0;

    private JMRInteractionManager.InteractionDeviceType InteractionDeviceType => 
        _addedDevice == 0 ? JMRInteractionManager.Instance.GetSupportedInteractionDeviceType() : _addedDevice;
    
    public JMRInteractionManager.InteractionDeviceType GetInteractionDeviceType() => InteractionDeviceType;

    private void OnEnable()
    {
        JMRInteractionManager.OnConnected += OnConnect;
        JMRInteractionManager.OnDisconnected += OnDisconnect;
    } 
    private void OnDisable()
    {
        JMRInteractionManager.OnConnected -= OnConnect;
        JMRInteractionManager.OnDisconnected -= OnDisconnect;
    }

    private void OnConnect(JMRInteractionManager.InteractionDeviceType devType, int index, string val)
    {
        _addedDevice = devType;
    }
    private void OnDisconnect(JMRInteractionManager.InteractionDeviceType devType, int index, string val)
    {
        _addedDevice = 0;
    }
}
```

{% content-ref url="../device-state/" %}
[device-state](../device-state/)
{% endcontent-ref %}
