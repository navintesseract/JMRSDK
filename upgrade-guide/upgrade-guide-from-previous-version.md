# Upgrade guide from v4.7.3

{% hint style="info" %}
Before importing new package, please delete Packages folder from your project folder, this is probable fix for missing references from SDK prefabs.
{% endhint %}

## **JMRDraggable component**

All existing custom-scrolls, sliders and all other draggable objects should have JMRDraggable.cs script component on it.

1\.  Select ViewPort of existing CustomScrolls or Sliders.

2\.  Add component “JMRDraggable.cs” on it.

\
**Laser Pointer not visible fix**
---------------------------------

If Pointer does not appear after importing, please follow the steps given in LaserRayFix

Go to Asset > JMRSDK > Core > Prefabs > Pointers > JMRLaserPointer and check in the inspector.

1. Set LineMaterial to LaserPointerMatUnlit
2. Set Line Renderer to JMRSDK > Core > Prefabs > Pointers > JMRLaserPointer.
3. Set Width Multiplier to **0.04**.
4. Set Line Number Steps to **20**.

![](<../.gitbook/assets/image (7).png>)

{% hint style="info" %}
**Mandatory**: Configure System UI in all applications before building your app.
{% endhint %}

## **Configure System UI**

From menu, select

JioMixedReality > SystemUI > UpdateSortedLayer

![](<../.gitbook/assets/image (5).png>)

## **Recenter Application on Resume**&#x20;

It is set to true by default to recenter the view.

![](<../.gitbook/assets/image (3).png>)
