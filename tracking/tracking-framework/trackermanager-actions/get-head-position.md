---
description: Actions to get head position
---

# Get Head Position

> public void OnHeadPosition(Vector3 position)

| Parameter | Description                                 |
| --------- | ------------------------------------------- |
| Vector3   | Position of head in world coordinate system |

Action gives the updated head position.

{% hint style="info" %}
Action will be called only when it’s subscribed to a method. Action must be subscribed to the method with a matching signature.
{% endhint %}

```csharp
using JMRSDK;
using UnityEngine;

public class TrackingHeadPositionExample : MonoBehaviour
{
    void OnEnable()
    { 
        // subscribing to the action
        JMRTrackerManager.OnHeadPosition += onHeadPositionLocal;
    }
    void OnDisable()
    {
        // unsubscribing to the action
        JMRTrackerManager.OnHeadPosition -= onHeadPositionLocal;
    }
    
    //this action will be called per frame automatically
    // get Position when position updating 
    public void onHeadPositionLocal(Vector3 position)
    {
        Vector3 Pos = position;
    }
}
```
