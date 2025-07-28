---
description: Addition, Changes and Fixes in JMRSDK
---

# Release Notes

## JMR SDK v4.8.0

### Additions

* System UI - To notify user about device management across apps.
* Drag support in Toolkit scrolls.
* Custom timeout feature added to voice api.&#x20;
* OnKeyboardHide event added to Keyboard script.&#x20;
* Scroll optimiation for new JioGlass Controller.&#x20;

### Fixes

* User SDK dependency issue resolved.
* Scrolls reset on disabling the game object&#x20;
* Life cycle management improved calls improved and should not show exceptions during scene shift or application exit.&#x20;
* Null checks added in JMRPrimaryInputField&#x20;
* Default text in system UI popups added.&#x20;
* Background image added to status text in Voice Toolkit&#x20;
* Data rate controlled in manipulation
* Long press trigger delay fix&#x20;
* Auto hide keyboard on speech cancelled in between of listening.
* Token dependency removed for User Service&#x20;
* Controller connection disconnection callback handling issue fixed&#x20;
* Null reference exception while firing action fixed&#x20;
* JMRPersistant Instance reference issue fixed&#x20;
* Ray passing through UI issue fixed&#x20;
* Object moving towards ray while using manipulation issue fixed&#x20;
* Controller ray stuck issue fixed&#x20;
* Ray cast tracking stuck while using drag issue fixed&#x20;
* Recenter on app launch issue fixed&#x20;
* Infinite scroller reverted to previous version&#x20;
* Swipe up event on trackpad issue fixed&#x20;
* Voice trigger enabled on home button issue fixed

### Known Issues

* Continuous usage of camera for aprroximately 15- 20 min shows an error message “Camera Not Available”
* Nested Scroll takes even spaces while Scrolling to extreme ends.
* Keyboard shows full line in text after using voice input or closing and opening keyboard again
* Controller is connected based on LED but its showing controller pairing screen in application.
* Token expiry time on logout shows old date in example scene.
* Nearest controller doesn't get pair, but some random controller gets paired sometimes
* Slight drift is visible in controller ray while using camera.
* Controller ray stuck and tracking stuck issue was observed.
* On CU observe that after switching between few apps,  Ray was not visible and require frequent calibration.
* Custom Scroll (Circular and Nested) is not working when doing quick transitions multiple times in CU.
* Reliability - Tracking stopped after pressing home button and screen is turned black and user unable to resume experience. (JioGlass)

## JMR Services / Companion App v4.8.0

### Fixes

* Stability and time improvements for controller pairing
* Fixed wrong callback is sent for previously disconnected controller when trying to pair with new controller
* Fixed error codes conflicts between Interaction, Display and Device API
* Fixed location permission issues on different android versions
* Fixed issue of controller battery gives wrong data on connection
* Fixed multiple issues on Android 11
* Fixed Issue with camera sometimes doesn’t start.
* Fixed issue of voice API not working on CU
* Fixed device connection stuck issues
* Device IPD clamped to min and max values
* Fixed Jioglass is not detected if user connects JioGlass and app is installed

### Known Issues&#x20;

* Tracking doesn't work if user force kill and open companion app again while on glass MRLauncher was opened
* Jio Voice service not working
* Tracking: Holoboard: Tracing latency over holoboard is above 25ms
* Companion App: JioGlass is not detected if user connects the JioGlass and then install and setup the Companion App
* Sometimes nearest controller doesn’t get paired
