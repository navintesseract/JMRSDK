# IFn1Handler

Interface to handle **Fn1 Button** interaction.

| OnFn1Action | Called when pressing the Fn1 button, on touchpad click |
| ----------- | ------------------------------------------------------ |

```
using JMRSDK.InputModule;
using UnityEngine;
public class InterfaceExample: MonoBehaviour, IFn1Handler
{
    public void OnFn1Action() {
        Debug.Log("OnFn1Action");
    }
}
```
