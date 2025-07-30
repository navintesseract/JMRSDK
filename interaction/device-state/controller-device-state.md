# Controller Device State

## Controller Connected / Disconnected

> public void OnConnected (JMRInteractionManager.InteractionDeviceType devType, int index, string val)

> Public void OnDisconnect(JMRInteractionManager.InteractionDeviceType devType, int index, string val)

| Parameters            | Description               |
| --------------------- | ------------------------- |
| InteractionDeviceType | Type of device connected  |
| index                 | Index of connected device |
| name                  | Name of connected device  |

To get notified when the device is connected or disconnected, implement the callback method exposed through InteractionManager:&#x20;

OnConnected(JMRInteractionManager.InteractionDeviceType devType, int index, string val)

OnDisconnected(JMRInteractionManager.InteractionDeviceType devType, int index, string val)

Interaction Manager will call this action when the device is connected.&#x20;

{% hint style="info" %}
Action will be called only when it’s subscribed to a method. Action must be subscribed to a method with a matching signature.&#x20;
{% endhint %}

```csharp
using JMRSDK.InputModule;
using UnityEngine;

public class JMRDemoInteractionExample : MonoBehaviour
{  
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
        //do something when connected
        JMRInteractionManager.InteractionDeviceType deviceType = devType;
        int deviceIndex = index;
        string deviceName = val;
    }
    private void OnDisconnect(JMRInteractionManager.InteractionDeviceType devType, int index, string val)
    {
        //do something when disconnected
        JMRInteractionManager.InteractionDeviceType deviceType = devType;
        int deviceIndex = index;
        string DeviceName = val;
    }
}
```



***

## Battery Percentage

> public int GetBatteryPercentage(int controllerIndex)

| Parameter       | Description                |
| --------------- | -------------------------- |
| controllerIndex | Connected controller index |

| Return Type | Description                               |
| ----------- | ----------------------------------------- |
| int         | Batter percentage of connected controller |

```csharp
using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using JMRSDK.InputModule;

public class JMRInteractionExample : MonoBehaviour
{
    private List<IInputSource> Controllers = new List<IInputSource>();
    private bool isInitialized;
    private void OnEnable()
    {
        isInitialized = false;
        Controllers = new List<IInputSource>();
    }
    private IEnumerator WaitTilFindController()
    {
        do
        {
            Controllers = JMRInteractionManager.Instance.GetSources();
            yield return null;
        } while (Controllers.Count == 0);
        isInitialized = true;
    }
    private void OnDisable()
    {
        isInitialized = false;
        Controllers = new List<IInputSource>();
    }
    public void Update()
    {
        if (!isInitialized)
        {
            return;
        }
        float batteryPercentage = JMRInteractionManager.Instance.GetBatteryPercentage(Controllers[0].inputIndex);
    }
}
```



***

## Battery percentage update

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



***

##
