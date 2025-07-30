# Battery percentage update

> public void OnBatteryUpdate(JMRInteractionManager.InteractionDeviceType deviceType, int index, int percentage)

| Parameters            | Description               |
| --------------------- | ------------------------- |
| InteractionDeviceType | Type of device connected  |
| index                 | Index of connected device |
| percentage            | Percentage of Battery     |

To get notified when the battery percentage is updated need to implement the callback method exposed through InteractionManager:&#x20;

OnBatteryUpdate(JMRInteractionManager.InteractionDeviceType deviceType, int index, int percentage)

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
        JMRInteractionManager.OnBatteryUpdate += OnBatteryUpdate;
    } 
    private void OnDisable()
    {
        JMRInteractionManager.OnBatteryUpdate -= OnBatteryUpdate;
    }
    private void OnBatteryUpdate(JMRInteractionManager.InteractionDeviceType devType, int index, int percentage)
    {
        //do something when battery updated
        JMRInteractionManager.InteractionDeviceType deviceType= devType;
        int deviceIndex=index;
        int batteryPercentage=percentage;
    }
}
```
