# URP Support

There is a URP package for JioPrism (Holoboard) and JioDive, that needs to be added to enable URP with JioPrism and JioDive.

### Android

<table><thead><tr><th width="236">Device \ Render Pipeline</th><th width="156">Built-in renderer</th><th width="129">URP</th><th>URP + Post Processing</th></tr></thead><tbody><tr><td>JioGlass</td><td><mark style="color:green;">Supported</mark></td><td><mark style="color:green;">Supported</mark></td><td><mark style="color:green;">Supported</mark></td></tr><tr><td>Holoboard (Prism)</td><td><mark style="color:green;">Supported</mark></td><td><mark style="color:green;">Supported</mark></td><td>Not supported</td></tr><tr><td>Cardboard (Dive)</td><td><mark style="color:green;">Supported</mark></td><td><mark style="color:blue;">Supported</mark><em><mark style="color:blue;">*</mark></em></td><td>Not supported</td></tr></tbody></table>

### iOS

<table><thead><tr><th width="236">Device \ Render Pipeline</th><th width="156">Built-in renderer</th><th width="146">URP</th><th>URP + Post Processing</th></tr></thead><tbody><tr><td>JioGlass</td><td><mark style="color:green;">Supported</mark></td><td>Not Supported</td><td>Not Supported</td></tr><tr><td>Holoboard (Prism)</td><td>-</td><td>-</td><td>-</td></tr><tr><td>Cardboard (Dive)</td><td><mark style="color:green;">Supported</mark></td><td>Not Supported</td><td>Not supported</td></tr></tbody></table>

{% hint style="warning" %}
<mark style="color:blue;">Supported\*</mark> For URP with Jio Dive, ensure that Vulkan is at the top of the list in Project Settings > Rendering > Graphics API.
{% endhint %}
