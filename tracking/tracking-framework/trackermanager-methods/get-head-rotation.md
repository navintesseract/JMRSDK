---
description: How to get Head Rotation
---

# Get Head Rotation

> public Quaternion GetHeadRotation()

Return type

| Datatype   | Description                          |
| ---------- | ------------------------------------ |
| Quaternion | Rotation of head in world coordinate |

This method returns the updated head rotation in world coordinate.

{% hint style="info" %}
If you want to get the updated rotation then this function must be used in Update()
{% endhint %}

```csharp
using JMRSDK;
using UnityEngine;

public class PositionRotationExample: MonoBehaviour
{
    public void Update()
    {
        //getting the updated head rotation by calling GetHeadRotation()
        Quaternion rotation = JMRTrackerManager.Instance.GetHeadRotation();
    }
}
```
