---
description: Action to get head Transform
---

# Get Head Transform

| Parameter | Description                  |
| --------- | ---------------------------- |
| Transform | Transform of head gameobject |

Action gives the updated head Transform.

{% hint style="info" %}
Action will be called only when it’s subscribed to a method. Action must be subscribed to the method with a matching signature.
{% endhint %}

```csharp
using JMRSDK;
using UnityEngine;

public class TrackingExample : MonoBehaviour
{
    void OnEnable()
    {
        // subscribing to the action
        JMRTrackerManager.OnHeadTransform += onHeadTranform;
    }
    void OnDisable()
    {
        //unsubscribing to the action
        JMRTrackerManager.OnHeadTransform -= onHeadTranform;
    }
    //this action will be called per frame automatically
    // get head transform
    public void onHeadTranform(Transform t)
    {
        Transform _transform = t;
    }
}
```
