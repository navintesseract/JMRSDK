---
description: >-
  Gaze and Dwell interaction uses your head movement as a pointer, and focusing
  on any object allows you to select any option in the application.
---

# Gaze and Dwell

{% hint style="info" %}
This feature is recommended for only a few applications where the objective is to explore the immersive environment with minimum interactions.&#x20;
{% endhint %}

## How to Implement Gaze and Dwell Interaction&#x20;

* The developer can select the Pointer source from the editor inside the input manager.

![](<../.gitbook/assets/image (9).png>)

* Drag and drop `JMRGazeandDwellInteractable.cs` to use the default Gaze and Dwell features. For example, 3d objects,2d objects, UI elements, etc.; for more information, refer to the Example scene.
* To add custom behavior in your UI extent `IDwellhandler` Interface
  * `OnDwellStart`
  * `OnDwellCancel`
  * `OnDwellCompleted`

{% hint style="danger" %}
Gaze and dwell works on unity's scaled time scale, which means that interaction WILL get slower and faster with Time.timeScale.\
In the same way, if Time.timeScale is set to 0, Gaze and dwell will not be triggered.
{% endhint %}

## Switching between Gaze Mode and JioGlass Controller at runtime

To change the current pointing source between Gaze Mode and JioGlass Controller at runtime, use the below line of code; it will change Gaze mode (Head) to Controller Mode and vice versa -&#x20;

```csharp
JMRPointerManager.Instance.SwitchPointingSource();
```

To get the current pointing source, use the below line of code -

```csharp
JMRPointerManager.Instance.PrefferedPointingSource
```
