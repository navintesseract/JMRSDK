# Interfaces

Here are the multiple interfaces available for interaction:

<table data-full-width="true"><thead><tr><th width="210">Interface</th><th width="147">JioGlass<select><option value="7OhMA9fKr9w4" label="Supported" color="blue"></option><option value="7QqVEXqdJKRk" label="Not Supported" color="blue"></option></select></th><th width="143">JioDive<select><option value="UV4ZKRPqHFRK" label="Supported" color="blue"></option><option value="m87nniI5pgxH" label="Not Supported" color="blue"></option></select></th><th width="151">Global Listener<select><option value="08GncU9RV6u4" label="Required" color="blue"></option><option value="jFSQ0bQFfthA" label="Not Required" color="blue"></option><option value="toHDJbtsFo3D" label="Supported" color="blue"></option></select></th><th>Description</th></tr></thead><tbody><tr><td>IFocusable </td><td><span data-option="7OhMA9fKr9w4">Supported</span></td><td><span data-option="UV4ZKRPqHFRK">Supported</span></td><td><span data-option="toHDJbtsFo3D">Supported</span></td><td>Handle focus Enter/Exit</td></tr><tr><td>ISelectHandler </td><td><span data-option="7OhMA9fKr9w4">Supported</span></td><td><span data-option="UV4ZKRPqHFRK">Supported</span></td><td><span data-option="toHDJbtsFo3D">Supported</span></td><td>Handle simple pointer inputs like <strong>OnSelectDown</strong> &#x26; <strong>OnSelectUp</strong></td></tr><tr><td>ISelectClickHandler </td><td><span data-option="7OhMA9fKr9w4">Supported</span></td><td><span data-option="m87nniI5pgxH">Not Supported</span></td><td><span data-option="toHDJbtsFo3D">Supported</span></td><td>Handle simple click inputs</td></tr><tr><td>IBackHandler</td><td><span data-option="7OhMA9fKr9w4">Supported</span></td><td><span data-option="UV4ZKRPqHFRK">Supported</span></td><td><span data-option="08GncU9RV6u4">Required</span></td><td>Handle <strong>Back Button</strong> interaction</td></tr><tr><td>IHomeHandler </td><td><span data-option="7OhMA9fKr9w4">Supported</span></td><td><span data-option="UV4ZKRPqHFRK">Supported</span></td><td><span data-option="08GncU9RV6u4">Required</span></td><td>Handle <strong>Home Button</strong> interaction</td></tr><tr><td>IMenuHandler </td><td><span data-option="7OhMA9fKr9w4">Supported</span></td><td><span data-option="m87nniI5pgxH">Not Supported</span></td><td><span data-option="08GncU9RV6u4">Required</span></td><td>Handle <strong>Menu Button</strong> interaction</td></tr><tr><td>IFn1Handler </td><td><span data-option="7OhMA9fKr9w4">Supported</span></td><td><span data-option="m87nniI5pgxH">Not Supported</span></td><td><span data-option="08GncU9RV6u4">Required</span></td><td>Handle <strong>Fn1 Button</strong> interaction</td></tr><tr><td>IFn2Handler </td><td><span data-option="7OhMA9fKr9w4">Supported</span></td><td><span data-option="m87nniI5pgxH">Not Supported</span></td><td><span data-option="08GncU9RV6u4">Required</span></td><td>Handle <strong>Fn2 Button</strong> interaction</td></tr><tr><td>ISwipeHandler </td><td><span data-option="7OhMA9fKr9w4">Supported</span></td><td><span data-option="m87nniI5pgxH">Not Supported</span></td><td><span data-option="08GncU9RV6u4">Required</span></td><td>Handle swipe gestures</td></tr><tr><td>ITouchHandler </td><td><span data-option="7OhMA9fKr9w4">Supported</span></td><td><span data-option="m87nniI5pgxH">Not Supported</span></td><td><span data-option="08GncU9RV6u4">Required</span></td><td>Handle touch events on the trackpad</td></tr><tr><td>IManipulationHandler </td><td><span data-option="7OhMA9fKr9w4">Supported</span></td><td><span data-option="UV4ZKRPqHFRK">Supported</span></td><td><span data-option="toHDJbtsFo3D">Supported</span></td><td>Handle object <strong>Manipulation</strong> interactions. In <strong>Manipulation,</strong> you can <strong>grab</strong> an object and perform actions like <strong>rotating</strong>, <strong>scaling,</strong> or <strong>dragging</strong> it from one place to another</td></tr><tr><td>IScreenTouchHandler</td><td><span data-option="7QqVEXqdJKRk">Not Supported</span></td><td><span data-option="UV4ZKRPqHFRK">Supported</span></td><td><span data-option="08GncU9RV6u4">Required</span></td><td>Handle screen touch interaction</td></tr></tbody></table>

{% hint style="info" %}
**Legend** for the above table _(JioGlass/JioDive)_

Supported - The user can trigger the interface when interacting with the device.

Not Supported - The user can NOT trigger the interface when interacting with the device.
{% endhint %}

{% hint style="info" %}
**Legend** for the above table _(Global Listener)_

Supported - You can use Global Listener to trigger the interface when not hovering on a collider, but is not mandatory and depends on the specific case.

Required - You need to use Global Listener to trigger the interface.

Not Required - Using Global Listener will not help with interface functionality.
{% endhint %}

{% embed url="https://youtu.be/_OZRlNEsoDs?si=2gfLbeYeh9R1FVWF" %}

> ## See also

<table data-view="cards"><thead><tr><th></th><th data-type="content-ref"></th></tr></thead><tbody><tr><td>Global Listener</td><td><a href="../actions.md#global-listener">#global-listener</a></td></tr><tr><td>Manipulation</td><td><a href="../controller-input-actions/manipulation.md">manipulation.md</a></td></tr><tr><td>Device State</td><td><a href="../device-state/">device-state</a></td></tr></tbody></table>
