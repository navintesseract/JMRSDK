---
description: Frequently asked questions related to development
---

# FAQs - Develop

## Rendering

### # Even After Importing the SDK, my screen is rendering in mono view!&#x20;

#### Solution 1: Custom Build files should be selected

Make sure all of these are checked in the project settings > publishing settings:

* Custom Main Manifest
* Custom Main Gradle Template
* Custom Base Gradle Template
* Custom Gradle Properties Template

<div align="left"><figure><img src="../.gitbook/assets/Unity_aWDY7BNNSJ (2).png" alt=""><figcaption></figcaption></figure></div>

#### Solution 2: Using the correct canvas&#x20;

{% hint style="warning" %}
The application can appear to be on a single screen as it covers the entire screen space. Therefore, if you are using overlay canvas, switch it to world space or JMRSDK canvas.
{% endhint %}

#### Solution 3: Incorrectly imported SDK

This issue usually occurs when the files are not properly imported into the project. If you are facing this issue, follow the below-mentioned Steps: \
\
1\. Delete the folder inside the Assets >> Plugins >> Android \
2\. Re-import the JMRSDK plugins folder.

#### Solution 4: Nomenclature of GameObjects

1. Make sure that your gameobjects are not named as "Head" or "Left" or "Right" other than the ones present in JMRMixedReality prefab by default.
2. Make sure that only "Head" Camera is tagged as "MainCamera".

### # Dive Barrel Distortion Shader is not working properly

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption><p>This is the expected Barrel Distortion Shader for JioDive</p></figcaption></figure>

If using properly, follow the URP guide to set it up properly

{% content-ref url="../getting-started/urp-support/setting-up-your-project-with-urp.md" %}
[setting-up-your-project-with-urp.md](../getting-started/urp-support/setting-up-your-project-with-urp.md)
{% endcontent-ref %}

### # Layer not rendering

Go to the head, left, and right cameras and enable/disable the required layer in the culling mask of the cameras.

{% hint style="danger" %}
Do check the culling mask at runtime -&#x20;

On Head camera - Left and Right layer gets disabled\
On Left camera - Head and Right layer gets disabled\
On Right camera - Head and left layer gets disabled
{% endhint %}

{% hint style="warning" %}
Default behavior: Layer number 13 is used internally for the screen casting. So layer 13 does not render anything in left and right cameras. This might change depending on your project settings.
{% endhint %}

Layer "Left" and Layer "Right" does not render on respective cameras so you can use these layers if you want to render some object only on some particular camera.

<figure><img src="../.gitbook/assets/image (50).png" alt=""><figcaption><p>Unity - NOT in Play Mode</p></figcaption></figure>



## General

### # How to check the application's JMRSDK version?

In unity editor, \
Goto JMRSDK > Core > Plugins > Android > Readme > tmrServicesSDK-release-_**JMRSDK Version**_

In apk,\
Check the **AndroidManifest.xml** of your application build using `android studio` or any [3rd party analyzer](https://www.sisik.eu/apk-tool) for `meta data` - `com.jiotesseract.DeviceServiceSDKVersion` \
corresponding to which SDK version is present.



### # How to implement quit functionality from the application?

With JMRSDK 4.27.10, implementing quit functionality is only possible through JMR Toolkit and with the Home page setup.

{% content-ref url="../jmrsdk/jmrrig/setting-homepage-quit-functionality.md" %}
[setting-homepage-quit-functionality.md](../jmrsdk/jmrrig/setting-homepage-quit-functionality.md)
{% endcontent-ref %}



### # There are debug logs/warnings/errors coming from JMRSDK

{% hint style="danger" %}
These are the debug logs/warnings/errors to be <mark style="color:orange;">**ignored**</mark> in the current JMRSDK
{% endhint %}

1. `Cannot destroy GameObject that is part of a prefab instance.`

<figure><img src="../.gitbook/assets/image (86).png" alt=""><figcaption></figcaption></figure>

2. `NullReferenceException: Object reference not set to an instance of an object JMRSDK.JMRCameraManager.OnEnable ()`&#x20;



### # Application is facing Z-Fighting

When two or more primitives have very similar distances to the camera. This would cause them to have near-similar or identical values in the z-buffer, which keeps track of depth.

To fix that, physically move the objects further apart

## Input

### # Input Interaction is not working

1. Make sure that you have added the global listener to the gameobject if you want it to register input when the pointer is not focusing on the gameobject
2. To enable the Controller Input Actions APIs, you must add JMRInteraction Script to a GameObject in your scene.
3. Use [this ](../develop/editor-emulator.md)keybinding for triggering input in the unity editor.



### # How to implement Gaze and Dwell?

Refer to this:

{% content-ref url="../interaction/gaze-interaction/gaze-and-dwell.md" %}
[gaze-and-dwell.md](../interaction/gaze-interaction/gaze-and-dwell.md)
{% endcontent-ref %}



### # How to check which pointing source is being used?

You can get the pointing source from JMRPointerManager. Refer to this:

{% content-ref url="../interaction/gaze-interaction/gaze-and-dwell.md" %}
[gaze-and-dwell.md](../interaction/gaze-interaction/gaze-and-dwell.md)
{% endcontent-ref %}



### # Which controller buttons work with 'Gaze and Dwell' mode?

Although the controller can remain connected when 'gaze and dwell' is enabled, only the home button works to switch the application to the MR Launcher screen.&#x20;

None of the other buttons or actions are registered when 'Gaze and Dwell' is enabled.



## Device

### # How to get the device on which the application is running?

```
JMRRigManager.Instance.getDeviceID();
```

```
Editor = int_max,
JioHoloboard = 1,
JioGlass = 2,
JioCardboard = 3
```

{% hint style="info" %}
Use this code to change the controller in application instructions&#x20;

```
Editor = Unity editor
JioHoloboard = JioPrism - Physical Controller
JioGlass = JioGlass Lite - Virtual Controller
JioCardboard = JioDive - Physical Controller
```
{% endhint %}



### # How to add skybox to AR devices - JioGlass and JioPrism

Refer to [Skybox](../develop/cameras.md#skybox) in AR devices

{% hint style="info" %}
The same method can be used to change the far clipping distance of cameras as well.
{% endhint %}



### # How to change FOV in devices

FOV is changed automatically according to the selected device.&#x20;

However, if you want to update the FOV, you can do so after a few frames from the start of the JMRMixedReality prefab instance.

{% hint style="info" %}
Use this code for [specific device type](faqs-develop.md#how-to-get-the-device-on-which-the-application-is-running) to change FOV only for that device.
{% endhint %}

```csharp
private void Awake()
{
    head = JMRRigManager.Instance.transform.Find("JMRRenderer/Head")?.GetComponent<Camera>();
    left = JMRRigManager.Instance.transform.Find("JMRRenderer/Head/Left")?.GetComponent<Camera>();
    right = JMRRigManager.Instance.transform.Find("JMRRenderer/Head/Right")?.GetComponent<Camera>();
}

private void OnEnable()
{
    StartCoroutine(ChangeFOV());
}

IEnumerator ChangeFOV()
{
    for (int i = 0; i < 2; i++) yield return null;
    head.fov = left.fov = right.fov = targetFOV;
}
```
