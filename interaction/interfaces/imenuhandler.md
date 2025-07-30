# IMenuHandler

Interface to handle **Menu Button** interaction.

| Method       | Description                                                           |
| ------------ | --------------------------------------------------------------------- |
| OnMenuAction | Called when menu action is performed (pressing the home button twice) |

```csharp
using JMRSDK.InputModule;
using UnityEngine;
public class InterfaceExample: MonoBehaviour, IMenuHandler
{
    public void OnMenuAction() {
        Debug.Log("OnMenuAction");
    }
}
```
