---
description: How to get Head Position
---

# Get Head Position

> public Vector3 GetHeadPosition()

Return type

| Datatype | Description                          |
| -------- | ------------------------------------ |
| Vector3  | Position of head in world coordinate |

This method returns the updated head position in world coordinate.

{% hint style="info" %}
If you want to get the updated position then this function must be used in Update()
{% endhint %}

```csharp
using JMRSDK;
using UnityEngine;

public class PositionRotationExample: MonoBehaviour
{
    public void Update()
    {
        //Getting the updated Head position by calling the GetHeadPosition()
        Vector3 position = JMRTrackerManager.Instance.GetHeadPosition();
    }
}
```
