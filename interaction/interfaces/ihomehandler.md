# IHomeHandler

Interface to handle **Home Button** interaction.

| Method       | Description                                              |
| ------------ | -------------------------------------------------------- |
| OnHomeAction | Called when the home button of the controller is pressed |

```csharp
using JMRSDK.InputModule;
using UnityEngine;
public class InterfaceExample: MonoBehaviour, IHomeHandler
{
    public void OnHomeAction() {
        Debug.Log("OnHomeAction");
    }
}
```
