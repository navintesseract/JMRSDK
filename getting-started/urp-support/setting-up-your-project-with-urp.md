# Setting Up Your Project With URP

{% embed url="https://youtu.be/mpYiQoAJqhE?si=aw6bGynPOog3t9Xz" %}

## Converting your project to use URP

* Import the JMRSDK\_URP.unitypackage
* Install URP in your project using the following steps - \
  &#xNAN;_&#x57;indow -> Package Manager -> Universal RP_

<figure><img src="../../.gitbook/assets/Screenshot 2023-01-17 195952.png" alt=""><figcaption></figcaption></figure>

* Upgrade materials in the current project to URP materials using the following steps - \
  &#xNAN;_&#x4E;avigate to Edit -> Render Pipeline -> Universal Render Pipeline -> Upgrade Project Materials to UniversalRP Materials_

<figure><img src="../../.gitbook/assets/Screenshot 2023-01-17 200029.png" alt=""><figcaption></figcaption></figure>

* Create **UniversalRenderPipeline** Asset\
  &#xNAN;_&#x52;ight Click in the Asset Folder then Create -> Rendering -> Universal Render Pipeline -> Pipeline Asset (Forward Renderer)_

<figure><img src="../../.gitbook/assets/Screenshot 2023-01-17 200046.png" alt=""><figcaption></figcaption></figure>

* Assign the pipeline asset you have created to the graphic settings.\
  &#xNAN;_&#x45;dit -> Project Settings -> Graphics_

<figure><img src="../../.gitbook/assets/Screenshot 2023-01-17 200104.png" alt=""><figcaption></figcaption></figure>

* Add **BlitMaterialFetch** script to the Left and Right Camera in **JMRMixedReality** prefab under JMRRig -> JMRRenderer -> Head. This script will be in the **JMRSDK\_URP\_Extension** folder which you will get after installing the **JMRSDK\_URP** package.

<figure><img src="../../.gitbook/assets/Screenshot 2023-01-17 200125.png" alt="" width="563"><figcaption></figcaption></figure>

* Add the custom render features, **CustomBlitFeature\_L** & **CustomBlitFeature\_R** to your pipeline asset renderer. In this case, we have **UniversalRenderPipelineAsset\_Renderer**.&#x20;

<figure><img src="../../.gitbook/assets/Screenshot 2023-01-17 200157.png" alt="" width="563"><figcaption></figcaption></figure>

* Replace the **Standard** shader in JMRSDK>Core>Resources>Shader with the one from **JMRSDK\_URP\_Extension** folder.

## Reverting Back to Built-In Render Pipeline

* Remove the **BlitMaterialFetch** script from the **Left** & **Right** cameras which can be found under in **JMRMixedReality** prefab.
* Delete the **JMRSDK\_URP\_Extension** folder.
* From the package manager remove the **UniversalRP** package.
* Re-Import the **JMRSDK** packages. This will revert the materials in **JMRSDK** which got converted to Universal Render Pipeline/Lit back to the built-in standard shader.&#x20;
* _Convert all materials from URP to Built-In to make sure shaders are rendered correctly._
