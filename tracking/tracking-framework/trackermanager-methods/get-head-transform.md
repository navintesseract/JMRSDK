---
description: How to get Head Transform
---

# Get Head Transform

> public Transform GetHeadTransform()

Return type

| Datatype  | Description       |
| --------- | ----------------- |
| Transform | Transform of head |

This method returns the updated head transform.

{% hint style="info" %}
If you want to get the updated transform then this function must be used in Update()
{% endhint %}

```csharp
using JMRSDK;
using UnityEngine;

public class PositionRotationExample: MonoBehaviour
{
    public void Update()
    {
        //getting the updated head transform by calling GetHeadTransform()
        Transform headTransform = JMRTrackerManager.Instance.GetHeadTransform();
    }
}
```
