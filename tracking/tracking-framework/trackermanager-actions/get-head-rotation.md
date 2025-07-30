---
description: Actions to get head rotation
---

# Get Head Rotation

> public void OnHeadRotation(Quaternion quaternion)

| Parameter  | Description                                 |
| ---------- | ------------------------------------------- |
| Quaternion | Rotation of head in world coordinate system |

Action gives the updated head rotation.

{% hint style="info" %}
Action will be called only when it’s subscribed to a method. Action must be subscribed to the method with a matching signature.
{% endhint %}

```csharp
using JMRSDK;
using UnityEngine;

public class TrackingHeadRotationExample : MonoBehaviour
{
    void OnEnable()
    {
        // subscribing to the action
        JMRTrackerManager.OnHeadRotation += onHeadRotationLocal;
    }
    void OnDisable()
    {
        // unsubscribing to the action
        JMRTrackerManager.OnHeadRotation -= onHeadRotationLocal;
    }
    //this action will be called per frame automatically
    // get rotation when rotation updating
    public void onHeadRotationLocal(Quaternion rotation)
    {
        Quaternion Rot = rotation;
    }
}
```
