# ITouchHandler

Interface to handle touch events on the trackpad.

| Method         | Description                        |
| -------------- | ---------------------------------- |
| OnTouchStart   | Called when touch started          |
| OnTouchStop    | Called when touch stopped          |
| OnTouchUpdated | Called when touch position updated |

```csharp
using JMRSDK.InputModule;
using UnityEngine;
public class InterfaceExample: MonoBehaviour, ITouchHandler
{
    public void OnTouchStart(TouchEventData eventData, Vector2 TouchData) {
        Debug.Log("OnTouchStarted " + TouchData.ToString());
    }
    public void OnTouchStop(TouchEventData eventData, Vector2 TouchData) {
        Debug.Log("OnTouchStop " + TouchData.ToString());
    }
    public void OnTouchUpdated(TouchEventData eventData, Vector2 TouchData) {
        Debug.Log("OnTouchUpdated " + TouchData.ToString());
    }
}
```

## **TouchEventData**

| Datatype                     | Variable           | Description                           |
| ---------------------------- | ------------------ | ------------------------------------- |
| EventSystems.BaseInputModule | currentInputModule | Get the currently active Input Module |
| GameObject                   | selectedObject     | Get the currently selected object     |
| Vector2                      | TouchVector        | Get Touch Position                    |
