---
description: Optimize application to run with the best performance
---

# App optimization

<table data-view="cards"><thead><tr><th></th><th align="center"></th><th align="center"></th></tr></thead><tbody><tr><td></td><td align="center"><a href="https://docs.unity3d.com/2020.1/Documentation/Manual/MobileOptimizationPracticalGuide.html">A practical guide to Optimization for mobiles</a></td><td align="center"></td></tr><tr><td></td><td align="center"><a href="https://blog.unity.com/games/optimize-your-mobile-game-performance-expert-tips-on-graphics-and-assets">Optimize your mobile game performance</a></td><td align="center"></td></tr><tr><td></td><td align="center"><a href="https://blog.unity.com/games/optimize-your-mobile-game-performance-tips-on-profiling-memory-and-code-architecture-from">Tips on profiling, memory, and code architecture</a></td><td align="center"></td></tr></tbody></table>

## Graphical Optimizations

### Remove Heavy Post Processing effects

Not all post-processing effects are made to be used for mobile AR/VR

{% hint style="danger" %}
Effects that are too expensive for mobile VR and should be **removed** are as follows:

* Screen Space Reflection&#x20;
* Screen Space Ambient Occlusion&#x20;
{% endhint %}

{% hint style="warning" %}
Effects **NOT** to use because they can cause nausea and disorientation are:

* Lens distortion (causes motion sickness)
* Chromatic aberration  (occurs naturally in VR)
* Motion blur (cause motion sickness)
* Depth-of-field (user’s eyes need to focus themselves)
{% endhint %}

{% hint style="success" %}
Light-impacting post-processing effects in the cost of the order are as follows:

* Vignette
* Color grading
* Bloom (with High-Quality Filtering disabled)
* Anti-aliasing (FXAA is recommended for mobile VR)
{% endhint %}

### Bake lights

> Avoid real-time lights and bake lights as much as possible to get the best performance on your app.

### Batching and reducing draw calls

* Set non-moving objects as static
* Combine Meshes together
* Create sprite atlas for materials in your scene

### Occlusion Culling

> Bake occlusion information and enable occlusion culling on all cameras in your scene.

### Billboarding

Use billboards and Level of Detail meshes (LODs) wherever possible to avoid wasting computation on far away objects.

### Quality settings

Change the quality setting to low.

{% hint style="info" %}
Additionally, the quality settings can be optimized to perform on mobile devices and be interchanged depending on device performance.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (63).png" alt=""><figcaption><p>Example of quality setting on low end devices</p></figcaption></figure>

### Optimizing Terrain Settings

* Trees can be rendered as optimized meshes instead of terrain trees
* Allow GPU instancing on materials
* Remove excessive trees and foliage
* Reduce all texture size
* Reduce detail distance

<figure><img src="../../.gitbook/assets/image (71).png" alt=""><figcaption><p>Example of terrain setting on low end devices</p></figcaption></figure>



## Scripting Optimization

### Removing any expensive scripts

* Use object pooling whenever possible
* Avoid debugging logs and stack traces in builds
* Pre-cache data in scripts
* Avoid using every frame calls like Update, LateUpdate, and FixedUpdate.
* Avoid searching the entire hierarchy for objects, and do NOT use functions like FindObjectOfType, FindObjectWithTag, etc.

## Project Settings Optimization

* Set to incremental GC
* Enable multithreaded rendering
* Build with IL2CPP and ARM64

## JMR specific optimization

If you don't want to enable the screencast feature in your application, remove additional cameras that are not being used.

* &#x20;Screencast Camera
* &#x20;POV Camera



