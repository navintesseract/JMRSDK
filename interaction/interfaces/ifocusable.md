# IFocusable

The `IFocusable` interface handles pointer focus events on a GameObject, such as when the pointer targets the object (`OnFocusEnter`) or leaves the object (`OnFocusExit`).

| Method       | Description                                      |
| ------------ | ------------------------------------------------ |
| OnFocusEnter | Called when hovering the pointer on gameobject   |
| OnFocusExit  | Called when removing the pointer from gameobject |

## Global Listener Usage

Utilize Global Listener with IFocusable to know if the pointer focus enters/exits on something.

{% hint style="warning" %}
When both the `IFocusable` interface and Global Listener are used on the same GameObject, the event-handling methods may be triggered **twice**:

1. Once by the pointer event.
2. Once by the Global Listener capturing the same event globally.

This behavior can lead to duplicate responses if not managed properly.
{% endhint %}

## **Pointer Interaction Requirement**

For the pointer to interact with a GameObject and trigger the `IFocusable` events:

* **3D Objects**: The GameObject must have a **collider** component.
* **UI Elements**: The UI element must have the **Raycast Target** property enabled.

Without these, the pointer will not detect the GameObject, and `IFocusable` events will not be triggered.

## Example

```csharp
using JMRSDK.InputModule;
using UnityEngine;
public class InterfaceExample: MonoBehaviour, IFocusable
{
    public void OnFocusEnter() {
        Debug.Log("OnFocusEnter");
    }
    public void OnFocusExit() {
        Debug.Log("OnFocusExit");
    }   
}
```
