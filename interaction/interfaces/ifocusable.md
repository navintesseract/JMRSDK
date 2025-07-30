# IFocusable

Interface to handle when the pointer is focussed on a game object.

| Method       | Description                                      |
| ------------ | ------------------------------------------------ |
| OnFocusEnter | Called when hovering the pointer on gameobject   |
| OnFocusExit  | Called when removing the pointer from gameobject |

```csharp
using JMRSDK.InputModule;
using UnityEngine;
public class InterfaceExample: MonoBehaviour, IFocusable
{
    public void OnFocusEnter() {
        Debug.Log("OnFocusEnter");
    }
    public void OnFocusExit() {
        Debug.Log("OnFocusExit");
    }   
}
```
