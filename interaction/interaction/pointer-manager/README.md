# Pointer Manager

### PointerManager

Responsible to:

1. Make sure that at least one raycast is available in the scene
2. Create focus details
3. Will drive pointer prefab on data

Pointer manager is the bridge that handles different types of pointing sources like head cursor or pointing ray enabled motion controllers.&#x20;

{% hint style="warning" %}
If you don't have pointing ray-enabled controllers, it defaults to GazeManager.
{% endhint %}

| Public Methods          | Description                                                                                                       |
| ----------------------- | ----------------------------------------------------------------------------------------------------------------- |
| GetHitInfo              | Returns the HitInfo of the current Hit, if any.                                                                   |
| GetCurrentFocusedObject | Gets currently focused object, if any                                                                             |
| GetCursor               | Gets the Cursor object associated with this pointer                                                               |
| GetCurrentRay           | Gets the current ray                                                                                              |
| GetCursorTransform      | Gets the transform of the cursor. This is the transform of the white dot that users use to interact with objects. |
