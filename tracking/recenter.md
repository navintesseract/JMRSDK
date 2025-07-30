---
description: How to recenter automatically on resume?
---

# Recenter

![Scene reference](<../.gitbook/assets/image (65).png>)

| Parameter                           | Description                                     |
| ----------------------------------- | ----------------------------------------------- |
| shouldRecenterUponApplicationResume | Recenter position and rotation if value is true |

```csharp
using JMRSDK;
using UnityEngine;

public class TrackingExample : MonoBehaviour
{
    void OnEnable()
    {
        JMRTrackerManager.Instance.SetRecenterUponApplicationResume(true);
    }
}
```

## Recenter Actions

### How to use recenter action events

```csharp
JMRSystemActions.Instance.OnRecenterStart.AddListener(() => 
{ 
    Debug.log("On Recenter Start"); 
});
```

```csharp
JMRSystemActions.Instance.OnRecenterCancelled.AddListener(() => 
{ 
    Debug.log("On Recenter Cancelled"); 
});
```

```csharp
JMRSystemActions.Instance.OnRecenterEnd.AddListener(() => 
{ 
    Debug.log("On Recenter End"); 
});
```

### **Recenter Head/Rig Function**

#### Exposed a function to recenter game scene anytime

```csharp
JMRTrackerManager.Instance.Recenter()
```
