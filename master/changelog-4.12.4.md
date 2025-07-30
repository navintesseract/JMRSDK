# Changelog - 4.12.4

{% hint style="danger" %}
* JMRInputField needs to be updated with the new prefab
* Toolkit v1 has been deprecated from JMRSDK 4.12.4, please upgrade to Toolkit v2 to enjoy latest features and upgrades
{% endhint %}

### New Features Released <a href="#new-features-released" id="new-features-released"></a>

* Virtual Controller Support added for JioGlass Lite (Smartphone) Ecosystem
* Virtual Keyboard Support added for JioGlass Lite (Smartphone) Ecosystem
* [Local Rig](../jmrsdk/jmrrig/local-rig.md)
* [Gaze & Dwell](../interaction/gaze-and-dwell.md)
* Application Analytics for App Lifecycle
* [Recenter UI and events for developers](../tracking/recenter.md)
* [Recenter function exposed to developers](../tracking/recenter.md)
* Lifecycle Improvements
* Performance Improvements
  * Reduced RAM footprint of core services by 30%+
  * GC Reduced from 21.86 MB/min to nearly 0 MB/min for camera preview - 100%
  * GC Reduced from 25.7 MB/min to nearly 23.1 MB/min for camera recording - 8%
  * Optimised RAM: 20\~30 MB - 10%

### Bugfixes <a href="#bugfixes" id="bugfixes"></a>

* Fixed issue of notification icon and Intent data on android 29&#x20;
* Changed camera shutter sound and fixed low shutter sound&#x20;
* Lifecycle improvement – limit number of callbacks to 2 in FIFO order for non-system apps
* Fixed multiple controller connect/disconnect event&#x20;
* While registering callback fixed broadcast events for specific client.&#x20;



* Fixed NPE for getter of Firmware Versions&#x20;
* Exposed a function to recenter the scene for developers
* Removed voice toolkit on long press of back button
* Unity Persistent / Non-Persistent ray issue fixed
* System UI re-calibration pop up updated
* New Recenter UI added on long press to recenter
* Recenter Action events exposed to developers
* Swipe interaction correction

### Known Issues <a href="#known-issues" id="known-issues"></a>

* Toolkit v1 is not compatible with Virtual Keyboard
* Existing applications will have to be recompiled with this SDK to make it compatible with Virtual Controller and Virtual Keyboard on smartphones
* Slight glitch is observed in controller ray while switching scene to non-persistent scene
* Text preview area/field above keyboard disappears/cleared when user click on space button
* Launcher - Search - (x) button not working for launcher keyboard&#x20;
* Few null references for MainThreadDispatcher which might cause some stuttering in the application after 20 mins of continuous usage
* Few redundant error logs are present in the console

\
