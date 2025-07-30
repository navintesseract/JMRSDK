# External Gamepad

JMRSDK supports gamepad integration.

<table><thead><tr><th>Compatability</th><th data-type="checkbox">External Gamepad</th></tr></thead><tbody><tr><td>JioGlass</td><td>true</td></tr><tr><td>JioDive</td><td>true</td></tr></tbody></table>

JMRSDK supports these controllers:

* Xbox Series X|S Controller,&#x20;
* PS4 DualShock 4 Controller,&#x20;
* PS5 Controller,
* Jio Game Controller

## Key Benefits

JioGlass and JioDive keep track of the user's head orientation. When external controllers are connected, JMRSDK InputManager switches to the Head pointing source.&#x20;

{% hint style="info" %}
By default, JMRSDK maps the select button with the A button (Cross button on PlayStation) of the controller. The rest of the keys can be mapped however required by the application.
{% endhint %}

1\. Effortless Tracking: Users can now navigate your application or environment simply by moving their head, providing a more intuitive and immersive experience.

2\. Gamepad Clicks: Clicking, selecting, and interacting with objects or UI elements is a breeze with gamepad controls, ensuring smooth and precise actions.

3\. Increased Engagement: This feature combo elevates user engagement, making your application more accessible and enjoyable.

4\. Flexibility for Developers: Our SDK is designed with you in mind. We've made it easy for you to integrate and customize these functionalities to suit your specific project needs.

{% hint style="danger" %}
A button (Cross button on PlayStation) of the controller is reserved for select button and should not be mapped for gameplay.
{% endhint %}

## Integrating the controller

Unity provides two methods for using input mappings

* Input Manager
* Input System

{% hint style="info" %}
JMRSDK uses the Input Manager. If Input System mapping is required, you must set the Input System to both in Project Settings > Player.
{% endhint %}

### Using the Input Manager

The older system, which is built into the editor, is called the [Input Manager](https://docs.unity3d.com/Manual/class-InputManager.html). The Input Manager is part of the core Unity platform and is the default if you do not install this Input System Package.

To use the InputManager file in your project settings of your project:

Copy the below InputManager.asset file and replace it inside Project > ProjectSettings > InputManger.asset.&#x20;

{% file src="../.gitbook/assets/InputManager.asset" %}

### Using the Input System

**Input System package** is a newer, more flexible system, which allows you to use any kind of Input Device to control your Unity content. It's intended to be a replacement for Unity's classic Input Manager. To use it, you must [install it into your project using the Package Manager](https://docs.unity3d.com/Packages/com.unity.inputsystem@1.7/manual/Installation.html).

#### References

{% embed url="https://docs.unity3d.com/Packages/com.unity.inputsystem@1.7/manual/index.html" %}

{% embed url="https://www.youtube.com/watch?ab_channel=Brackeys&v=p-3S73MaDP8" %}

### Supported Controllers

#### Jio Game Controller

<figure><img src="../.gitbook/assets/image (111).png" alt=""><figcaption></figcaption></figure>

#### Xbox Series X|S Wireless Controller

<figure><img src="../.gitbook/assets/image (112).png" alt=""><figcaption></figcaption></figure>

#### PS4 DualShock 4 Controller

<figure><img src="../.gitbook/assets/image (113).png" alt=""><figcaption></figcaption></figure>

#### PS5 DualSense Controller

<div data-full-width="false"><figure><img src="../.gitbook/assets/image (115).png" alt="" width="375"><figcaption></figcaption></figure></div>
