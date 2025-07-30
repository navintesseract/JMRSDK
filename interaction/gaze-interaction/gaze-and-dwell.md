---
description: >-
  Gaze and Dwell interaction uses your head movement as a pointer, and focusing
  on any object allows you to select any option in the application.
---

# Gaze and Dwell

{% hint style="info" %}
This feature is recommended for only a few applications where the objective is to explore the immersive environment with minimum interactions.&#x20;
{% endhint %}

## How to Implement Gaze and Dwell Interaction&#x20;

* Select the Pointer source and gaze mode from the editor inside the input manager.

<figure><img src="../../.gitbook/assets/image (31).png" alt=""><figcaption></figcaption></figure>

* Drag and drop `JMRGazeInteractable.cs` to use the default Gaze and Dwell features. For example, 3d objects,2d objects, UI elements, etc.; for more information, refer to the Example scene.

{% hint style="danger" %}
JMRGazeAndDwellInteraction script has been renamed to JMRGazeInteraction as it now functions with gaze and dwell with gaze and click as well.

Therefore all applications using gaze and dwell before JMRSDK 4.30 will get a missing component error in unity and will have to replace that component with JMRGazeInteraction.
{% endhint %}

* To add custom behavior to dwell extent `IDwellhandler` Interface
  * `OnDwellStart`
  * `OnDwellCancel`
  * `OnDwellCompleted`

{% hint style="danger" %}
Gaze and dwell works on unity's scaled time scale, which means that interaction WILL get slower and faster with Time.timeScale.\
In the same way, if Time.timeScale is set to 0, Gaze and dwell will not be triggered.
{% endhint %}

