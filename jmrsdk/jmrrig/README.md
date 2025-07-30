# JMRRig

## Introduction to JMR Rig

The JMRRig consists of cameras letting users view the content, known as the JMRRenderer. It consists of 3 cameras. \
**Head** camera renders only in the editor. \
The **left and Right** cameras handle rendering in Prism(Holoboard), Dive and JioGlass with a split-screen effect.&#x20;

It also contains the tracking manager, which initializes the necessities for head movement tracking.

### What is the purpose of JMRRig?

* Controls Re-center Location
* Re-Center on Resume
* Cameras

{% embed url="https://youtu.be/9BSGg-uMYHI?si=YM4889ckPzjK7vZj" %}

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

