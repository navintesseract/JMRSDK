---
description: How to recenter automatically on resume?
---

# Recenter

![Scene reference](<../.gitbook/assets/image (14).png>)

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
