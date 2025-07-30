# Setting Up Your Project With URP

{% hint style="warning" %}
This feature is only available from JMRSDK 4.24.1 onwards
{% endhint %}

* Import the JMRSDK\_URP.unitypackage
* Install URP in your project using the following steps - \
  &#xNAN;_&#x57;indow -> Package Manager -> Universal RP_

<figure><img src="../../.gitbook/assets/Screenshot 2023-01-17 195952 (1).png" alt=""><figcaption></figcaption></figure>



* Upgrade materials in the current project to URP materials using the following steps - \
  &#xNAN;_&#x4E;avigate to Edit -> Render Pipeline -> Universal Render Pipeline -> Upgrade Project Materials to UniversalRP Materials_

<figure><img src="../../.gitbook/assets/Screenshot 2023-01-17 200029.png" alt=""><figcaption></figcaption></figure>

<div align="center"><figure><img src="https://lh3.googleusercontent.com/cdkyR8-ZrJH_lJwgwOkqdQv1T0dIauTUry8GuYreCqf13gr0LGE7m5hXYR_BmhFK2tfZvg1n6lrJjBkmy4MCxGHHMTM4JUx03ECDnhl7l1rDfnL6Ouf9ypFCVPGlIgyiXkMZuq2b1wkAzg8deQp5yFfo14hHHYKuofVgnR6BPAzGTCDgL1WyJDDDJNguZfxiLMu6qA" alt=""><figcaption></figcaption></figure></div>

* Create **UniversalRenderPipeline** Asset\
  &#xNAN;_&#x52;ight Click in the Asset Folder then Create -> Rendering -> Universal Render Pipeline -> Pipeline Asset (Forward Renderer)_

<figure><img src="../../.gitbook/assets/Screenshot 2023-01-17 200046.png" alt=""><figcaption></figcaption></figure>

<figure><img src="https://lh6.googleusercontent.com/5piPNAMv6QauArco04iyrJ0hA7EieYir20jnpHbRCjV5DTCZ4XqKaRUfILbURGTJOujAFBTa-8-sk832y1atKk_jl--xpam15iOMkuIMmz7biMc9Q81RP1J6vOI0yORT73C1Ia13_G2fMhiOkhMPPDTFlbuWlP-ya9A2FP2Ks4bDNOCFFM25cwyOWWNWo6TBhTTLeg" alt=""><figcaption></figcaption></figure>

* Assign the pipeline asset you have created to the graphic settings.\
  &#xNAN;_&#x45;dit -> Project Settings -> Graphics_

<figure><img src="../../.gitbook/assets/Screenshot 2023-01-17 200104.png" alt=""><figcaption></figcaption></figure>

<figure><img src="https://lh3.googleusercontent.com/zbsJaEv_Nm0EBdjblo4Q8iMtH431gNRz05wxNd9YULHI3wnTjiXWzD4EXvmZmlpsgPcprpW6GE_XRWDa6_fhEw_ltaU-X7u-59UwtK3EWeHo4zLR0tY1cTH2Pipu72drySUvDXEyd4LZqyZinpUR4HOyFZnhAGXWdf2FsOOavfT4u0FRu_rRCemOelz29hUsZb0oYw" alt=""><figcaption></figcaption></figure>

* Add **BlitMaterialFetch** script to the Left and Right Camera in **JMRMixedReality** prefab under JMRRig -> JMRRenderer -> Head. This script will be in the **JMRSDK\_URP\_Extension** folder which you will get after installing the **JMRSDK\_URP** package.

<figure><img src="../../.gitbook/assets/Screenshot 2023-01-17 200125.png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
For Jio Dive you need to turn off the BlitMaterialFetch script if added to cameras.
{% endhint %}

<figure><img src="https://lh5.googleusercontent.com/dzTPN60H-oUmjAL80ie6mESiVrVItYkNJTTBsC7v33O495-3kV7JKMpU3xTJLregLChLk8Hlak2k4pAtSfc4bVg9GV8dqFTNCjDH4oHhLwuKox4b4KUKDP6hPaMrQOVvmNaDDUJJyWFkTMPH78v2Qkt3sOicba-jq4Au23qPuEWlk80garxUSlkTfu9LMxISgZS6tw" alt=""><figcaption></figcaption></figure>

<figure><img src="https://lh5.googleusercontent.com/3pBfAxFwXLDuf343UEXCOn1sEaVnne7gHtWxDB2ZRwZsmaKaXmjbXA6LxpFsHvoz1CxPVwwzgauPG7pW0O3Kul5FhvItSdrCCYZR__-Td8E52rZb1xM7XBmmq7a5YTB9XiIG4GjCwd1HNG70Od6njK68xKjaWiQKXritR79pxvD-Bqa4EhWU8wRaIGwhHgO18Oq7mw" alt=""><figcaption></figcaption></figure>

* Add the custom render features, **CustomBlitFeature\_L** & **CustomBlitFeature\_R** to your pipeline asset renderer. In this case, we have **UniversalRenderPipelineAsset\_Renderer**.&#x20;

<figure><img src="../../.gitbook/assets/Screenshot 2023-01-17 200157.png" alt=""><figcaption></figcaption></figure>

<figure><img src="https://lh5.googleusercontent.com/mheN7kK5Lq9AecGHyr0YuqCe8FrjfP4sTuAD2w1WmkyB1jMPE2ziXcrchHDqjuw65a78fIEb0G8KmLdwd2uv2yGGCbQGzt1AISp1LhgcBPFJg6oqTkN_hofnBV_itRhLc1Akf2EhaPF3ArAod35JCCPSjCAnOsblFmoLMZiQ73BLPX0K1R3jJQT3YewmA45emeLi1g" alt=""><figcaption></figcaption></figure>

*   Replace the **Standard** shader in JMRSDK>Core>Resources>Shader with the one from **JMRSDK\_URP\_Extension** folder.

