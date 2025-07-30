# Pointer Manager

## PointerManager

Responsible to:

1. Make sure that at least one ray cast is available in the scene for interaction whenever required
2. Create focus details
3. Will drive pointer prefab on data

The pointer manager is the bridge that handles different types of pointing sources - head cursor or pointing ray-enabled motion controllers.&#x20;

{% hint style="warning" %}
If you don't have pointing ray-enabled controllers, it defaults to GazeManager.
{% endhint %}

### Enable and Disable Pointer

If you want to enable/disable the pointer and its interaction, you can use&#x20;

<pre class="language-csharp"><code class="lang-csharp"><strong>bool enableInteraction;
</strong><strong>JMRPointerManager.Instance.ToggleInteraction(enableInteraction), JMRPointerManager.PointingSource.Head)
</strong></code></pre>

| Public Methods          | Description                                                                                                       |
| ----------------------- | ----------------------------------------------------------------------------------------------------------------- |
| GetHitInfo              | Returns the HitInfo of the current Hit, if any.                                                                   |
| GetCurrentFocusedObject | Gets currently focused object, if any                                                                             |
| GetCursor               | Gets the Cursor object associated with this pointer                                                               |
| GetCurrentRay           | Gets the current ray                                                                                              |
| GetCursorTransform      | Gets the transform of the cursor. This is the transform of the white dot that users use to interact with objects. |

{% content-ref url="../../gaze-interaction/gaze-and-dwell.md" %}
[gaze-and-dwell.md](../../gaze-interaction/gaze-and-dwell.md)
{% endcontent-ref %}
