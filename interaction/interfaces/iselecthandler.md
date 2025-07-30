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
        Debug.Log("OnSelectDown");
    }
    public void OnSelectUp(SelectEventData eventData) {
        Debug.Log("OnSelectUp");
    }
}
```

## **SelectEventData**

| EventSystems.BaseInputModule | **currentInputModule** | Get the currently active Input Module |
| ---------------------------- | ---------------------- | ------------------------------------- |
| GameObject                   | **selectedObject**     | Get the currently selected object     |
