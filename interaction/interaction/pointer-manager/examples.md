# Examples

## Get HitInfo of the current Hit

> JMRPointerManager.Instance.GetCurrentRay();

```csharp
using JMRSDK.InputModule;
using UnityEngine;
public class GetHitInfoExample: MonoBehaviour
{
    private void Update()
    {
        Ray ray = JMRSDK.InputModule.JMRPointerManager.Instance.GetCurrentRay();
        if(Physics.Raycast(ray, out RaycastHit hit))
        {
            Debug.Log(hit.transform.name);
        }
    }
}
```

## Get currently focused object

> JMRPointerManager.Instance.GetCurrentFocusedObject();

```
using JMRSDK.InputModule;
using UnityEngine;
public class GetCursorFocusedObjectExample: MonoBehaviour, ISelectHandler
{
    private void Update()
    {
 
        GameObject go = JMRPointerManager.Instance.GetCurrentFocusedObject();
    }
}
```

## Get cursor

> JMRPointerManager.Instance.GetCursor ();

```
using JMRSDK.InputModule;
using UnityEngine;
public class GetCurrentFocusedObjectExample: MonoBehaviour
{
    private void Update()
    {
        JMRCursor cursor= JMRPointerManager.Instance.GetCursor();
    }
}
```

## Get current Ray

> JMRPointerManager.Instance.GetCurrentRay();

```
using JMRSDK.InputModule;
using UnityEngine;
public class GetCurrentRayExample: MonoBehaviour
{
    private void Update()
    {
        Ray ray = JMRSDK.InputModule.JMRPointerManager.Instance.GetCurrentRay();
    }
}
```

## Get cursor transform

> JMRPointerManager.Instance. GetCursorTransform();

```
using JMRSDK.InputModule;
using UnityEngine;
public class GetCursorTransformExample: MonoBehaviour
{
    private void Update()
    {
        Transform cursorTransform= JMRSDK.InputModule.JMRPointerManager.Instance. GetCursorTransform();
    }
}
```
