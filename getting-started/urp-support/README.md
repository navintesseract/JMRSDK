# URP Support

There is a URP package for JioPrism (Holoboard) and JioDive, that needs to be added to enable URP with JioPrism and JioDive.

<table><thead><tr><th width="236">Device \ Render Pipeline</th><th width="156">Built-in renderer</th><th width="129">URP</th><th>URP + Post Processing</th></tr></thead><tbody><tr><td>JioGlass Lite</td><td>Supported</td><td>Supported</td><td>Supported</td></tr><tr><td>Holoboard (Prism)</td><td>Supported</td><td>Supported</td><td>Not supported</td></tr><tr><td>Cardboard (Dive)</td><td>Supported</td><td><mark style="color:blue;">Supported</mark><em><mark style="color:blue;">*</mark></em></td><td>Not supported</td></tr></tbody></table>

{% hint style="warning" %}
<mark style="color:blue;">Supported\*</mark> For URP with Jio Dive you need to add Vulkan in Graphics Rendering APIs and move it to the top of the list, from Project Settings > Rendering > Graphics API.

Note: You may face issues if you are using JMRSDK's Media player or Web View as Vulkan is not supported with it.
{% endhint %}
