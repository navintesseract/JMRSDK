# ISwipeHandler

Interface to handle swipe gestures on the touchpad.

| Function         | Description                        |
| ---------------- | ---------------------------------- |
| OnSwipeCanceled  | Called when swipe is cancelled     |
| OnSwipeCompleted | Called when swipe is completed     |
| OnSwipeDown      | Called when swiped down            |
| OnSwipeLeft      | Called when swiped left            |
| OnSwipeRight     | Called when swiped right           |
| OnSwipeStarted   | Called when swipe starts           |
| OnSwipeUp        | Called when swiped up              |
| OnSwipeUpdated   | Called when swipe position updates |

```
using JMRSDK.InputModule;
using UnityEngine;

public class InterfaceExample: MonoBehaviour, ISwipeHandler
{
    public void OnSwipeCanceled(SwipeEventData eventData) {
        Debug.Log("OnSwipeCanceled");
    }
    public void OnSwipeCompleted(SwipeEventData eventData) {
        Debug.Log("OnSwipeCompleted");
    }
    public void OnSwipeDown(SwipeEventData eventData, float delta) {
        Debug.Log("OnSwipeDown");
    }
    public void OnSwipeLeft(SwipeEventData eventData, float delta) {
        Debug.Log("OnSwipeLeft");
    }
    public void OnSwipeRight(SwipeEventData eventData, float delta) {
        Debug.Log("OnSwipeRight");
    }
    public void OnSwipeStarted(SwipeEventData eventData) {
        Debug.Log("OnSwipeStarted");
    }
    public void OnSwipeUp(SwipeEventData eventData, float delta) {
        Debug.Log("OnSwipeUp");
    }
    public void OnSwipeUpdated(SwipeEventData eventData, Vector2 delta) {
        Debug.Log("OnSwipeUpdated");
    }
}
```

## **SwipeEventData**

<table><thead><tr><th width="185.33333333333331">Datatype</th><th width="208.58086560364467">Variable</th><th>Description</th></tr></thead><tbody><tr><td>EventSystems.BaseInputModule</td><td>currentInputModule</td><td>Get the currently active Input Module</td></tr><tr><td>GameObject</td><td>selectedObject</td><td>Get the currently selected object</td></tr><tr><td>Vector2</td><td>SwipeDelta</td><td>Amount of swipe moved by the user</td></tr><tr><td>float</td><td>SwipeTouchTime</td><td>Amount of time spent in touch</td></tr><tr><td>float</td><td>SwipeMovementAmount</td><td>Movement done by the user while swiping</td></tr><tr><td>Vector2</td><td>NormalizedOffset</td><td>Offset over the duration of swipe</td></tr><tr><td>float</td><td>SwipeTime</td><td>Amount of time the swipe was registered</td></tr><tr><td>float</td><td>SwipeAmount</td><td>Amount of swipe registered</td></tr></tbody></table>
