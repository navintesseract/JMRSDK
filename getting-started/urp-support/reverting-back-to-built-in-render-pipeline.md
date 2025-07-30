# Reverting Back to Built-In Render Pipeline

{% hint style="warning" %}
This feature is only available from JMRSDK 4.24.1 onwards
{% endhint %}

* Remove the **BlitMaterialFetch** script from the **Left** & **Right** cameras which can be found under in **JMRMixedReality** prefab.
* Delete the **JMRSDK\_URP\_Extension** folder.
* From the package manager remove the **UniversalRP** package.
* Re-Import the **JMRSDK** packages. This will revert the materials in **JMRSDK** which got converted to Universal Render Pipeline/Lit back to the built-in standard shader. _Unity does not provide a converter to revert materials from URP to Built-In._
