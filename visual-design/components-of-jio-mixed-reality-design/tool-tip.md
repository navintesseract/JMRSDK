# Tool Tip



A good tooltip briefly describes unlabeled controls or provides a bit of additional information about labeled controls, when this is useful. It can also help customers navigate the UI by offering additional—not redundant—information about control labels, icons, and links. A tooltip should always add valuable information; use it sparingly.

There are two components you can use to display a tooltip:

* **Tooltip:** A styled tooltip that you can display on a chosen target.
* **TooltipHost:** A wrapper that automatically shows a tooltip when the wrapped element is hovered or focused.

## Best Practices <a href="#best-practices" id="best-practices"></a>

### Content <a href="#content" id="content"></a>

* Don’t use a tooltip to restate a button name that’s already shown in the UI.
* When a control or UI element is unlabeled, use a simple, descriptive noun phrase. For example: “Highlighting pen”. Only capitalize the first word (unless a subsequent word is a proper noun), and don’t use a period.
* For a disabled control that could use an explanation, provide a brief description of the state in which the control will be enabled. For example: “This feature is available for line charts.”

For a UI label that needs some explanation:

* Briefly describe what you can do with the UI element.
* Use the imperative verb form. For example, "Find text in this file" (not "Finds text in this file").

For a truncated label or a label that’s likely to truncate in some languages:\
(\*Truncated label - one that has been shortened)

* Provide the untruncated label in the tooltip.
* Don't provide a tooltip if the untruncated info is provided elsewhere on the page or flow.
* Optional: On another line, provide a clarifying description, but only if needed.

## Tooltip&#x20;

### **States**

![](<../../.gitbook/assets/image (31).png>)

### Transitions

| **Transitions** | **Front View**                                                                                                                                                                                                                                                                                                                                                                                                                     | **Isometric View**                                                                                                                                                                                                                                                                                                                                                                                                                 |
| --------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Appear**      | <p><img src="blob:https://tesseractimaging.atlassian.net/c942cc99-42ba-4459-a815-81457fa95de6#media-blob-url=true&#x26;id=ded56ae4-07f4-4034-b974-32eb9b6aa224&#x26;collection=contentId-78775686&#x26;contextId=78775686&#x26;mimeType=image%2Fgif&#x26;name=Tooltip_Appear_Front.gif&#x26;size=1524946&#x26;width=512&#x26;height=512" alt=""></p><p><img src="../../.gitbook/assets/Tooltip_Appear_Front.gif" alt=""></p>       | <p><img src="blob:https://tesseractimaging.atlassian.net/790d3faf-abf2-4380-adc5-d2390ed3b123#media-blob-url=true&#x26;id=3381f0f7-2903-45a0-9a61-ce17de48e6f0&#x26;collection=contentId-78775686&#x26;contextId=78775686&#x26;mimeType=image%2Fgif&#x26;name=Tooltip_Appear_Persp.gif&#x26;size=1503884&#x26;width=512&#x26;height=512" alt=""></p><p><img src="../../.gitbook/assets/Tooltip_Appear_Persp.gif" alt=""></p>       |
| **Disappear**   | <p><img src="blob:https://tesseractimaging.atlassian.net/e169668f-937f-4282-91e9-b9c51feca033#media-blob-url=true&#x26;id=a02b668e-89b5-45dd-a8f4-c0fdbff562c4&#x26;collection=contentId-78775686&#x26;contextId=78775686&#x26;mimeType=image%2Fgif&#x26;name=Tooltip_Disappear_Front.gif&#x26;size=1519398&#x26;width=512&#x26;height=512" alt=""></p><p><img src="../../.gitbook/assets/Tooltip_Disappear_Front.gif" alt=""></p> | <p><img src="blob:https://tesseractimaging.atlassian.net/eb2130c7-1cd2-4784-8644-231135e89852#media-blob-url=true&#x26;id=505ae655-5df5-48d8-a5bf-d54f759e73cf&#x26;collection=contentId-78775686&#x26;contextId=78775686&#x26;mimeType=image%2Fgif&#x26;name=Tooltip_Disappear_Persp.gif&#x26;size=1450351&#x26;width=512&#x26;height=512" alt=""></p><p><img src="../../.gitbook/assets/Tooltip_Disappear_Persp.gif" alt=""></p> |
