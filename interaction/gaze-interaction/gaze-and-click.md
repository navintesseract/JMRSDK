# Gaze and Click

To interact with Gaze and click on editor press \[<mark style="color:yellow;">**J**</mark>] on the keyboard

To interact with Gaze and click on JioDive click on the \[JioDive button] as shown below.

<div align="center"><figure><img src="../../.gitbook/assets/dive-click.gif" alt="" width="300"><figcaption><p>JioDive gaze and click button</p></figcaption></figure></div>

## How to Implement Gaze and Click Interaction&#x20;

Select the Pointer source and Gaze mode from the editor inside the input manager.

<figure><img src="../../.gitbook/assets/image (93).png" alt=""><figcaption></figcaption></figure>

Drag and drop `JMRGazeInteractable.cs` to use the default Gaze and Click features. For example, 3d objects,2d objects, UI elements, etc.; for more information, refer to the Example scene.

{% hint style="danger" %}
JMRGazeAndDwellInteraction script has been renamed to JMRGazeInteraction as it now functions with gaze and dwell with gaze and click as well.

Therefore all applications using gaze and dwell before JMRSDK 4.30 will get missing component error in unity and will have to replace that component with JMRGazeInteraction.
{% endhint %}

{% hint style="info" %}
IScreenTouchHandler detects when the screen is being touched.
{% endhint %}

To add custom behavior to dwell extent `IScreenTouchHandler` Interface

* ```
  OnScreenTouchBegan
  ```
* ```
  OnScreenTouchEnded
  ```
*   ```
    OnScreenTouchClick
    ```



### Toggle Interaction

To enable and disable interaction, developers can use `JMRPointerManager.Instance.ToggleInteraction(bool, JMRPointerManager.PointingSource.Head)`
