# Touchpad - Touch

{% hint style="info" %}
In order to enable the below APIs, you must add JMRInteraction Script to a GameObject in your scene.
{% endhint %}

```csharp
Vector2 JMRInteraction.GetTouch();
```

Returns the Vector2 position of the touch coordinates on the trackpad.

Returns (0,0) when the trackpad is not being touched.

When touched in the center the value is **(0.5, 0.5)**

When touched from left to right in horizontal axis keeping center in the vertical axis there is a gradual increase of values from **(0.0, 0.5)** to **(1.0, 0.5).** You can see the values change in the X-Axis of Vector2.

When Touched from Up to Down through in vertical axis keeping center in the horizontal axis there is a Gradual Increase From **(0.5, 0.0)** to **(0.5, 1.0).** You can see the values change in the Y-Axis of Vector2.

Anywhere else the value is a combination of the same.

{% hint style="info" %}
To map it from **–1** to **1** in place of **0** to **1** use

float xTouch = (TouchData.x - 0.5f) \* 2;\
float yTouch = (TouchData.y - 0.5f) \* 2;
{% endhint %}
