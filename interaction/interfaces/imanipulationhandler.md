# IManipulationHandler

Interface to handle object **Manipulation** interaction. Manipulation is done by **long-pressing** the select button. In **Manipulation,** you can **grab** an object and then perform actions like **rotating**, **scaling,** or **dragging** it from one place to another.

| Method                  | Description                               |
| ----------------------- | ----------------------------------------- |
| OnManipulationCompleted | Called when the manipulation is completed |
| OnManipulationStarted   | Called when the manipulation is started   |
| OnManipulationUpdated   | Called when the manipulation is updated   |

```csharp
using JMRSDK.InputModule;
using UnityEngine;
public class InterfaceExample: MonoBehaviour, IManipulationHandler
{
    public void OnManipulationCompleted(ManipulationEventData eventData) {
        Debug.Log("OnManipulationCompleted");
    }
    public void OnManipulationStarted(ManipulationEventData eventData) {
        Debug.Log("OnManipulationStarted");
    }
    public void OnManipulationUpdated(ManipulationEventData eventData) {
        Debug.Log("OnManipulationUpdated");
    }
}
```

## **ManipulationEventData**

| Datatype                     | Variable           | Description                                                 |
| ---------------------------- | ------------------ | ----------------------------------------------------------- |
| EventSystems.BaseInputModule | currentInputModule | Get the currently active Input Module                       |
| GameObject                   | selectedObject     | Get the currently selected object                           |
| Vector3                      | CumulativeDelta    | Cumulative manipulation distance since manipulation started |
