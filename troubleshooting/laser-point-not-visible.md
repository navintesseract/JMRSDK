# Laser Point Not Visible

## **Laser Pointer not visible fix**

If Pointer does not appear after importing, please follow the steps given in LaserRayFix

Go to Asset > JMRSDK > Core > Prefabs > Pointers > JMRLaserPointer and check in the inspector.

1. Set LineMaterial to LaserPointerMatUnlit
2. Set Line Renderer to JMRSDK > Core > Prefabs > Pointers > JMRLaserPointer.
3. Set Width Multiplier to **0.04**.
4. Set Line Number Steps to **20**.

![](<../.gitbook/assets/image (11).png>)

See also:

{% content-ref url="../interaction/gaze-and-dwell.md" %}
[gaze-and-dwell.md](../interaction/gaze-and-dwell.md)
{% endcontent-ref %}
