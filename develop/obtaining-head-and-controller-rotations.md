# Controller Input

## Obtaining Interaction Ray

* You can get the Interaction Ray from the **JMRPointerManager** class as follows

```
JMRPointerManager.Instance.GetCurrentRay();
```

## Obtaining Head Orientation

* You can get the Head Orientation from the **JMRTrackerManager** class as follows

```
JMRTrackerManager.Instance.GetHeadTransform();
```

## Obtaining Controller Orientation

* You can get the Controller Orientation from the **JMRInteractionManager** class as follows

```
IInputSource source = JMRInteractionManager.Instance.GetCurrentSource();
Quaternion controllerOrientation;
Source.TryGetPointerRotation(out controllerOrientation);
```

## Obtaining Input Actions

{% hint style="info" %}
In order to enable the below APIs, you must add JMRInteraction Script to any one GameObject in your scene.
{% endhint %}

## Select Action

```
bool JMRInteraction.GetSelect();
```

Returns true during the frame the user completes single click of the Select Button. You need to call this function from the [Update](https://docs.unity3d.com/ScriptReference/MonoBehaviour.Update.html) function, since the state gets reset each frame. It will not return true until the user has releases this key and he presses it again.&#x20;

## Source Button Down

```
bool JMRInteraction.GetSourceDown(JMRSDK.InputModule.JMRInteractionSourceInfo);
```

Returns true during the frames the user has pressed the source button, defined as the argument of type _JMRSDK.InputModule.JMRInteractionSourceInfo_. You need to call this function from the [Update](https://docs.unity3d.com/ScriptReference/MonoBehaviour.Update.html) function, and keeps returning true as long as the user has this button pressed down

## Source Button Up

```
bool JMRInteraction.GetSourceUp(JMRSDK.InputModule.JMRInteractionSourceInfo);
```

Returns true during the frames the user has not pressed the source button, defined as the argument of type _JMRSDK.InputModule.JMRInteractionSourceInfo_. You need to call this function from the [Update](https://docs.unity3d.com/ScriptReference/MonoBehaviour.Update.html) function, and keeps returning true as long as the user has this button in released state.

## Swipe Up/ Down/ Left/ Right

```
bool JMRInteraction.GetSwipeUp();
bool JMRInteraction.GetSwipeDown();
bool JMRInteraction.GetSwipeLeft();
bool JMRInteraction.GetSwipeRight();
```

Returns true during the frame the user performs swipe using trackpad. You need to call this function from the [Update](https://docs.unity3d.com/ScriptReference/MonoBehaviour.Update.html) function, since the state gets reset each frame. It will not return true until the user has releases this key and he swipes the trackpad again.&#x20;

## Trackpad Touch Values

```
Vector2 JMRInteraction.GetTouch();
```

Returns the Vector2 position of the touch coordinates on the trackpad.&#x20;

Returns (0,0) when trackpad is not being touched.

##
