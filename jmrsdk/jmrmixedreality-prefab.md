# JMRMixedReality Prefab

JMRMixedReality is the prefab instantiated when you configure a scene for Mixed Reality. This prefab consists of all the systems required for communication with the hardware, rendering, input, and handling system UI popups.

#### Types

* Persistent (when allow persist is enabled)
* Non-Persistent (when allow persist is disabled)

{% hint style="info" %}
When allow persist is enabled JMRMixedReality Gameobject persists, i.e., when the scene is changed, the new JMRMixedReality Gameobject in the loaded scene is replaced with the persistent JMRMixedReality Gameobject.
{% endhint %}

<div align="left"><img src="../.gitbook/assets/image (20).png" alt="JMRMixed Reality Prefab Structure"></div>

