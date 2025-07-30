# JMRRig

## Introduction to JMR Rig

The JMRRig consists of cameras that let the users view the content, known as the JMRRenderer. It consists of 3 cameras. Head camera renders only in the editor. The left and Right cameras handle rendering in HoloBoard and JioGlass with a split-screen effect. It also contains the tracking manager which initializes the necessities for tracking the head movement tracking.

### What is the purpose of JMR Rig?

* Controls recenter location
* Recenter on resume
* Cameras

## Rig Manager

#### Methods

> public GameObject GetHeadObject();

Returns Head game object

```csharp
using UnityEngine;
using JMRSDK;
 
public class JMRDemoInteractionExample : MonoBehaviour
{
 public void Start()
 {
  GameObject head = JMRRigManager.Instance.GetHeadObject();
 }
}
```

