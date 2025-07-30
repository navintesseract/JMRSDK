# IFn2Handler

Interface to handle **Fn2 Button** interaction.

| Method      | Description                                                   |
| ----------- | ------------------------------------------------------------- |
| OnFn2Action | Called when pressing the Fn2 button, on touchpad double click |

```csharp
using JMRSDK.InputModule;
using UnityEngine;
public class InterfaceExample: MonoBehaviour, IFn2Handler
{
 public void OnFn2Action() {
  Debug.Log("OnFn1Action");
 }
}
```
