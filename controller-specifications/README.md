# Controller Specifications

1. Physical Controllers for JioPrism and JioDive Pro
2. Virtual Controller for JioGlass

The controller provides the following functionality to interact:&#x20;

1. Controller Rotational tracking
2. Select
3. Touchpad / Swipe
4. Special Function Button
5. Back
6. Home
7. Recenter

Gaze is an interactional method, that developers can use. This includes Pointing and selecting a particular option through focus and/or click.&#x20;

{% content-ref url="../interaction/gaze-interaction/" %}
[gaze-interaction](../interaction/gaze-interaction/)
{% endcontent-ref %}

## Interaction Compatibility

Compatibility of Interaction with Platform for **JioDive**

<table><thead><tr><th>JioDive</th><th data-type="checkbox">Android</th><th data-type="checkbox">iOS</th></tr></thead><tbody><tr><td>Gamepad</td><td>true</td><td>true</td></tr><tr><td>Controller</td><td>true</td><td>false</td></tr><tr><td>Virtual Controller</td><td>false</td><td>false</td></tr><tr><td>Gaze and Click</td><td>true</td><td>true</td></tr><tr><td>Gaze and Dwell</td><td>true</td><td>true</td></tr></tbody></table>

Compatibility of Interaction with Platform for **JioGlass**

<table><thead><tr><th>JioGlass</th><th data-type="checkbox">Android</th><th data-type="checkbox">iOS</th></tr></thead><tbody><tr><td>Gamepad</td><td>true</td><td>true</td></tr><tr><td>Controller</td><td>false</td><td>false</td></tr><tr><td>Virtual Controller</td><td>true</td><td>true</td></tr><tr><td>Gaze and Click</td><td>false</td><td>false</td></tr><tr><td>Gaze and Dwell</td><td>true</td><td>true</td></tr></tbody></table>

## Controller Fallback Scenario

In the case where multiple controllers are connected, the system prioritizes the interaction devices in the following order:

1. **Gamepad**
2. **Physical Controller**
3. **Virtual Controller**
4. **Gaze and Click**
5. **Gaze and Dwell**

The highest priority is given to the first available device in this sequence, ensuring seamless interaction by selecting the most responsive and suitable controller.
