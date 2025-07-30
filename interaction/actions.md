# Actions

## Global Actions

* **Back button** - Single click button for navigation in the application to previous / pause state hierarchy. You are expected to implement the IBackHandler Interface and manage the application flow within your application yourself. Maps to IBackHandler.
* **Home button** - Single click button that takes the user back to the home screen.
* **Menu button** - On pressing the home button twice - Double press the button that opens System Menu.
* **Voice button** - Long pressing back button – Enables voice interaction.
* **Recentre -** Long press button to recentre head and controller orientation during an application.

## Global Listener

To make these interactions **Global** to trigger them from anywhere, add the following line to the **Start** function of the **InterfaceExample** script.

```csharp
JMRInputManager.Instance.AddGlobalListener(gameObject);
```

## Local Action

* **Select -** Single click button for carrying out any app-related interaction.
* **Touch**
* **Swipe**

## Obtaining Interaction Ray

You can get the Interaction Ray from the **JMRPointerManager** class as follows

> JMRPointerManager.Instance.GetCurrentRay();

```csharp
using UnityEngine;
using JMRSDK.InputModule;
 
public class JMRDemoRayExample : MonoBehaviour
{
    public void Update()
    {
        Ray ray = JMRPointerManager.Instance.GetCurrentRay();
    }
}
```

## Obtaining Head Orientation

You can get the Head Orientation from the **JMRTrackerManager** class as follows

> JMRTrackerManager.Instance.GetHeadTransform();

```csharp
using UnityEngine;
using JMRSDK;
 
public class JMRDemoHeadExample : MonoBehaviour
{
     public void Update()
     {
          Transform head = JMRTrackerManager.Instance.GetHeadTransform();
     }
}
```

## Obtaining Controller Orientation

You can get the Controller Orientation from the **JMRInteractionManager** class as follows

> ```csharp
> IInputSource source = JMRInteractionManager.Instance.GetCurrentSource();
> Quaternion controllerOrientation;
> Source.TryGetPointerRotation(out controllerOrientation);
> ```

```csharp
using UnityEngine;
using JMRSDK.InputModule;
 
public class JMRDemoHeadExample : MonoBehaviour
{
     public void Update()
     {
          IInputSource source = JMRInteractionManager.Instance.GetCurrentSource();
          Quaternion controllerOrientation;
          source.TryGetPointerRotation(out controllerOrientation);
     }
}
```
