# Gaze and Dwell

## How to use

* Developer can select Pointer source from the editor inside input manager

![](<../.gitbook/assets/image (26).png>)

* Drag and drop `JMRGazeandDwellInteractable.cs` to use default Gaze and Dwell features.\
  For example 3d objects ,2d objects ,UI elements etc. for more information refer Example scene.
* To add custom behaviour in your UI extent `IDwellhandler` Interface
  * `OnDwellStart`
  * `OnDwellCancel`
  * `OnDwellCompleted`

## Switching between Gaze Mode and JioGlass Controller at runtime

To change the current pointing source between Gaze Mode and JioGlass Controller at runtime, use the below line of code, it will change Gaze mode (Head) to Controller Mode and vice versa -&#x20;

```csharp
JMRPointerManager.Instance.SwitchPointingSource();
```

To get the current pointing source use the below line of code -

```csharp
JMRPointerManager.Instance.PrefferedPointingSource
```
