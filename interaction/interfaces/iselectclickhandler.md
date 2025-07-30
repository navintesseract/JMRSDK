# ISelectClickHandler

Interface to handle select button click.

| Method          | Description                          |
| --------------- | ------------------------------------ |
| OnSelectClicked | Called when select button is clicked |

```csharp
using JMRSDK.InputModule;
using UnityEngine;
public class InterfaceExample: MonoBehaviour, ISelectClickHandler
{
    public void OnSelectClicked(SelectClickEventData eventData) 
    {
        Debug.Log("OnSelectClicked");
    }
}

```

## **SelectClickEventData**

| Datatype                     | Variable           | Description                           |
| ---------------------------- | ------------------ | ------------------------------------- |
| EventSystems.BaseInputModule | currentInputModule | Get the currently active Input Module |
| GameObject                   | selectedObject     | Get the currently selected object     |
| int                          | TapCount           | Get the tap count                     |
