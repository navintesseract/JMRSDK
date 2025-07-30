# Cameras

There are 4 cameras in the JMRMixedReality prefab.

![](<../.gitbook/assets/image (103).png>)

{% hint style="danger" %}
The **head** camera is tagged as the main camera and is disabled when running on target device, hence if you are using `Camera.main` in your application, it will return with a null reference exception.
{% endhint %}

## Rendering from cameras

The head camera renders the application in 2d mono view in the unity editor.

Left and right cameras render the application in 3d stereo view on the target device.

POV camera is used for casting your application to other devices.&#x20;

<figure><img src="../.gitbook/assets/Screenshot_2024-12-20-18-30-50-04_5c33812e51fa9a6c7dd727d7ab1eb025[1].jpg" alt=""><figcaption><p>Mono View - Covers the entire screen - Usually rendered by the main *head* camera in unity editor.</p></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot_2025-01-02-16-32-14-87_8c1639957c55dc4413004aa7405699cb[1].jpg" alt=""><figcaption><p>Stereo View - Split into two views - Rendered by the *left* and *right* cameras.</p></figcaption></figure>

## Skybox

Skybox can be used to render the sky. \
Skybox has other use cases as well as mentioned in [unity's documentation](https://docs.unity3d.com/Manual/skyboxes.html).

{% hint style="info" %}
In the unity editor skybox is enabled by default.
{% endhint %}

Skybox is enabled by default in VR devices i.e., JioDive

Skybox is disabled by default in AR devices i.e., JioPrism and JioGlass.

{% hint style="info" %}
Virtual Controller has the functionality to turn the skybox on and off by changing the camera Clear Flags.
{% endhint %}

### Forcing skybox mode in your application

You can force the cameras to render in skybox mode by changing the camera clear flags on the OnEnable event after 1-2 frames delay.

{% hint style="info" %}
Users can still revert to `Clear flags` - `Solid Color` by toggling VR mode in Virtual Controller.
{% endhint %}

```csharp
public class SkyboxAddition: MonoBehaviour
{
    Camera head, left, right;

    private void Awake()
    {
        head = JMRRigManager.Instance.transform.Find("JMRRenderer/Head")?.GetComponent<Camera>();
        left = JMRRigManager.Instance.transform.Find("JMRRenderer/Head/Left")?.GetComponent<Camera>();
        right = JMRRigManager.Instance.transform.Find("JMRRenderer/Head/Right")?.GetComponent<Camera>();
    }

    private void OnEnable()
    {
        StartCoroutine(AddSkybox());
    }

    IEnumerator AddSkybox()
    {
        for (int i = 0; i < 2; i++) yield return null;
        head.clearFlags = left.clearFlags = right.clearFlags = CameraClearFlags.Skybox;
    }
}
```
