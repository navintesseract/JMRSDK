# IVoiceHandler

Interface to handle **Voice Button** interaction.

| Method        | Description                                                          |
| ------------- | -------------------------------------------------------------------- |
| OnVoiceAction | Called when voice action is performed (on long pressing back button) |

```csharp
using JMRSDK.InputModule;
using UnityEngine;
public class InterfaceExample: MonoBehaviour, IVoiceHandler
{
 public void OnVoiceAction() {
  Debug.Log("OnVoiceAction");
 }
}
```
