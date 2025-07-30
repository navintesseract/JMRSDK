# Recenter

## Recenter on Application Resume

To recenter automatically when the application opens or resumes, check the `` Recenter Upon Application Resume` `` in JMRRig -> JMR Tracker Manager.&#x20;

![Scene reference](<../.gitbook/assets/image (46).png>)

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

## **Recenter Head/Rig Function**

#### Exposed a function to recenter game scene anytime

```csharp
JMRTrackerManager.Instance.Recenter()
```
