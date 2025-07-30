# Source Buttons

## Select Action

> bool JMRInteraction.GetSelect();

Returns true during the frame the user completes a single click of the Select Button. You need to call this function from the [Update](https://docs.unity3d.com/ScriptReference/MonoBehaviour.Update.html) function since the state gets reset for each frame. It will not return true until the user releases this key and presses it again.

```csharp
using UnityEngine;
using JMRSDK.InputModule;
 
public class JMRDemoSelectExample : MonoBehaviour
{
     public void Update()
     {
          bool isSelected = JMRInteraction.GetSelect();
     }
}
```

## Source Button Down

> bool JMRInteraction.GetSourceDown(JMRSDK.InputModule.JMRInteractionSourceInfo);

Returns true during the frames the user was pressing the source button, defined as the argument of type _JMRSDK.InputModule.JMRInteractionSourceInfo_. You need to call this function from the [Update](https://docs.unity3d.com/ScriptReference/MonoBehaviour.Update.html) function. It keeps returning true as long as the user has this button pressed down.

```csharp
using UnityEngine;
using UnityEngine.UI;
using JMRSDK.InputModule;
using JMRSDK;
 
public class JMRDemoSourceDownExample : MonoBehaviour
{
     public void Update()
     {
          bool isSourceDown= JMRInteraction.GetSourceDown(JMRSDK.InputModule.JMRInteractionSourceInfo.Select);
     }
}
```

## Source Button Up

> bool JMRInteraction.GetSourceUp(JMRSDK.InputModule.JMRInteractionSourceInfo);

Returns true during the frames the user was not pressing the source button, defined as the argument of type _JMRSDK.InputModule.JMRInteractionSourceInfo_. You need to call this function from the [Update](https://docs.unity3d.com/ScriptReference/MonoBehaviour.Update.html) function. It keeps returning true as long as the user has this button in the released state.

```csharp
using UnityEngine;
using UnityEngine.UI;
using JMRSDK.InputModule;
using JMRSDK;
 
public class JMRDemoSourceUpExample : MonoBehaviour
{
     public void Update()
     {
          bool isSourceUp= JMRInteraction.GetSourceUp(JMRSDK.InputModule.JMRInteractionSourceInfo.Select);
     }
}
```
