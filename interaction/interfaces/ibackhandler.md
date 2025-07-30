# IBackHandler

Interface to handle **Back Button** interaction.

| Method       | Description                                              |
| ------------ | -------------------------------------------------------- |
| OnBackAction | Called when the back button of the controller is pressed |

```csharp
using JMRSDK.InputModule;
using UnityEngine;
public class InterfaceExample: MonoBehaviour, IBackHandler
{
    public void OnBackAction() {
        Debug.Log("OnBackAction");
    }
}
```
