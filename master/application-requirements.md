# Application Requirements

When developing an application make sure of the following:

1. An instance of **JMRAnalyticsManager** should be present at all times with the environment set to **Production**.
2. In Manifest> Category and Devices should be set as per your application every time.
3. Make sure your application does not have Unity 2D splash screen.
4. The application should always have Back functionality.
5. The application should work with Home functionality as provided by the JMRSDK.
6. If using the Physical Controller, Virtual Controller, or Gamepad, include a tutorial for the respective active interaction device.
7. \[JioDive IOS only] If the application is using Gaze and Dwell / Gaze and click, make sure the Home button of Dock returns the user to the home screen.
8. The application should be crash-free and should not lag (try to maintain 60 FPS)
9. The application should show a paused state of the application when minimized and resumed or in case of [JioGlass device is removed](../interaction/device-state/#jioglass-methods).
10. Make sure to adhere to Google Play Console policies for Android and make sure to adhere to Apple App Store Connect policies for iOS.&#x20;

These points are cumulated to avoid rejection of an application in JioImmerse but are not limited to these.
