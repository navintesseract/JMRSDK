# JioGlass Device State

## JioGlass Proximity Sensor

JioGlass Proximity sensor can be used to detect if the user is wearing JioGlass or not.

> public static Action onPowerStateChange;

To get notified when the device's proximity is changed use this method from JMRDisplayManager.

```csharp
using JMRSDK.InputModule;
using JMRSDK;
using UnityEngine;

public class JMRDemoInteractionExample : MonoBehaviour
{  
    void Start()
    {
        JMRDisplayManager.onPowerStateChange += GlassState;
    }
    
    void GlassState(int state)
    {
        if(state == 0)
        {
            //removed JioGlass
        }
        if(state == 1)
        {
            //worn JioGlass
        }
    }
}
```
