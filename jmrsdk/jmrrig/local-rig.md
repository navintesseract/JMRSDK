---
description: Local Rig is a feature that allows overriding JMRRig's rotation.
---

# Local Rig

The local rig prevents device sensors from overriding JMRRig's rotation directly. \
Instead, it adds the rotation delta to the current rotation.

If you want to rotate JMRRig from scripts or animations, enable Local Rig Feature.

{% hint style="info" %}
Local Rig is only required when the application runs on the target device. \
In Unity Editor, there is no sensor data to override JMRRig's rotation and hence in unity editor, JMRRig acts as a local rig by default.
{% endhint %}

## How to use Rig as a local transform

1. Configure scene for JioMixedReality.
2. Go to JMRMixedReality > JMRRig.
3. Go to Inspector > JMRTrackerManager component.
4. Check IsLocalRig to true.
5. Assign parent transform to the RigParent.

![](<../../.gitbook/assets/image (34).png>)
