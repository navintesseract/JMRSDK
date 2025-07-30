---
description: Swipe Up/ Down/ Left/ Right
---

# Touchpad - Swipe

{% hint style="info" %}
In order to enable the below APIs, you must add JMRInteraction Script to a GameObject in your scene.
{% endhint %}

{% hint style="success" %}
Returns true during the frame the user performs swipe using the trackpad. You need to call this function from the [Update](https://docs.unity3d.com/ScriptReference/MonoBehaviour.Update.html) function since the state gets reset for each frame. It will not return true until the user releases this key and swipes the trackpad again.
{% endhint %}

## Swipe Up

> bool JMRInteraction.GetSwipeUp(out float val);

Returns true if swiped up, also returns swipe up value.

```csharp
using UnityEngine;
using UnityEngine.UI;
using JMRSDK.InputModule;
using JMRSDK;
 
public class JMRDemoInteractionExample : MonoBehaviour
{
     public void Update()
     {
          bool isSwipeUp=JMRInteraction.GetSwipeUp(out float val);
     }
}
```

## Swipe Down

> bool JMRInteraction.GetSwipeDown();

Returns true if swiped down, also returns swipe down value.

```csharp
using UnityEngine;
using UnityEngine.UI;
using JMRSDK.InputModule;
using JMRSDK;
 
public class JMRDemoInteractionExample : MonoBehaviour
{
     public void Update()
     {
          bool isSwipeDown=JMRInteraction.GetSwipeDown(out float val);
     }
}
```

## Swipe Left

> bool JMRInteraction.GetSwipeLeft();

Returns true if swiped left, also returns swipe left value.

```csharp
using UnityEngine;
using UnityEngine.UI;
using JMRSDK.InputModule;
using JMRSDK;
 
public class JMRDemoInteractionExample : MonoBehaviour
{
     public void Update()
     {
          bool isSwipeLeft=JMRInteraction.GetSwipeLeft(out float val);
     }
}
```

## Swipe Right

> bool JMRInteraction.GetSwipeRight();

Returns true if swiped right, also returns swipe right value.

```csharp
using UnityEngine;
using UnityEngine.UI;
using JMRSDK.InputModule;
using JMRSDK;
 
public class JMRDemoInteractionExample : MonoBehaviour
{
     public void Update()
     {
          bool isSwipeRight=JMRInteraction.GetSwipeRight(out float val);
     }
}
```
