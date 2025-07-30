---
description: How to get the Battery percentage
---

# Battery Percentage

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
        float batterPercentage = JMRInteractionManager.Instance.GetBatteryPercentage(Controllers[0].inputIndex);
    }
}
```
