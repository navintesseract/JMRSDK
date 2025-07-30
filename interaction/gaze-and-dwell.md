# Gaze and Dwell

## How to use

* Developer can select Pointer source from the editor inside input manager

![](<../.gitbook/assets/image (16).png>)

* Drag and drop `JMRGazeandDwellInteractable.cs` to use default Gaze and Dwell features.\
  For example 3d objects ,2d objects ,UI elements etc. for more information refer Example scene.
* To add custom behaviour in your UI extent `IDwellhandler` Interface
  * `OnDwellStart`
  * `OnDwellCancel`
  * `OnDwellCompleted`

## Switching between Gaze Mode and JioGlass Controller at runtime

To change the current pointing source between Gaze Mode and JioGlass Controller at runtime, use below line of code , it will change Gaze mode (Head) to Controller Mode and vice versa -&#x20;

```
JMRPointerManager.Instance.SwitchPointingSource();
```

To get current pointing source use below line of code -

```
JMRPointerManager.Instance.PrefferedPointingSource
```
