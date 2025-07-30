# ISelectHandler

Interface to handle select button inputs like **OnSelectDown** & **OnSelectUp**.

| Method           | Description                               |
| ---------------- | ----------------------------------------- |
| **OnSelectDown** | Called when select button is pressed down |
| **OnSelectUp**   | Called when select button is released     |

```csharp
using JMRSDK.InputModule;
using UnityEngine;
public class InterfaceExample: MonoBehaviour, ISelectHandler
{
    public void OnSelectDown(SelectEventData eventData) {
        if (eventData.PressType == JMRInteractionSourceInfo.Select){
            Debug.Log("OnSelectDown");
        }
    }
    public void OnSelectUp(SelectEventData eventData) {
        if (eventData.PressType == JMRInteractionSourceInfo.Select){
            Debug.Log("OnSelectUp");
        }
    }
}
```

## **SelectEventData**

| EventSystems.BaseInputModule | **currentInputModule** | Get the currently active Input Module |
| ---------------------------- | ---------------------- | ------------------------------------- |
| GameObject                   | **selectedObject**     | Get the currently selected object     |

{% hint style="success" %}
You can use OnSelectDown and OnSelectUp to get the inputs of all the buttons using

```csharp
eventData.PressType
```

This can be used in the following ways

```csharp
eventData.PressType == JMRInteractionSourceInfo.Select
eventData.PressType == JMRInteractionSourceInfo.Back
eventData.PressType == JMRInteractionSourceInfo.Home
eventData.PressType == JMRInteractionSourceInfo.Function
```
{% endhint %}
