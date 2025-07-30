---
description: Gaze interaction is mandatory for running JioDive without controller.
---

# Gaze Interaction

## JioDive

JioDive can run without a controller through Gaze Interaction.

In Gaze interaction there are two modes:

1. **Gaze and Click**:\
   Gaze and Click interaction uses your head movement as a pointer, and clicking on any object using the JioDive allows you to select any option in the application.
2. **Gaze and Dwell**:\
   Gaze and Dwell interaction uses your head movement as a pointer, and focusing on any object allows you to select any option in the application.

### Currently active pointing source

To get the current pointing source, use the below line of code -

```csharp
JMRPointerManager.Instance.PrefferedPointingSource
```

This will return if the application is running on JioGlass Controller or gaze (head) control.

### Gaze for interaction

> Gaze can be used for much more than just UI

{% hint style="success" %}
Create a ray from the Head towards the forward direction to create more interactions of your own.
{% endhint %}

```csharp
Ray ray = new Ray(JMRTrackerManager.Instance.GetHeadPosition(),
    JMRTrackerManager.Instance.GetHeadTransform().forward);
bool isHitting = Physics.Raycast(ray, out RaycastHit hit);
if (isHitting)
{
    //do something
}
```
