# Changelog - 4.13.1

{% hint style="danger" %}
Important notice for users upgrading to JMRSDK 4.12.4+ from any previous versions

* JMRInputField needs to be updated with the new prefab
* Toolkit v1 has been deprecated from JMRSDK 4.12.4, please upgrade to Toolkit v2 to enjoy latest features and upgrades
{% endhint %}

### New Features Released <a href="#new-features-released" id="new-features-released"></a>

* Repository of Example Scenes added
* Core Service Analytics
* Core Unity SDK Analytics
* Performance Improvements
  * Reduced RAM footprint of core services by 30%+
  * GC Reduced from 21.86 MB/min to nearly 0 MB/min for camera preview - 100%
  * GC Reduced from 25.7 MB/min to nearly 23.1 MB/min for camera recording - 8%
  * Optimised RAM: 20\~30 MB - 10%
  * Update Loop - 45% reduction in Update Loop time
  * Ram - 28% Improvement in overall RAM footprint
  * GC - 15% reduction of garbage generation and collection
  * Draw Call reductions

### Bugfixes <a href="#bugfixes" id="bugfixes"></a>

NA

### Known Issues <a href="#known-issues" id="known-issues"></a>

* Toolkit v1 is not compatible with Virtual Keyboard
* Existing applications using SDK versions prior to v4.12.4 will have to be recompile with SDK v.4.12.4+ to make it compatible with Virtual Controller and Virtual Keyboard on smartphones
* Slight glitch is observed in controller ray while switching scene to non-persistent scene
* Launcher - Search - (x) button not working for launcher keyboard&#x20;
* Few null references for MainThreadDispatcher which might cause some stuttering in the application after 20 mins of continuous usage
* Few redundant error logs are present in the console

\
