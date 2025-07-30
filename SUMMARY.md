# Table of contents

* [Tesseract Mixed Reality SDK Documentation](README.md)
  * [Changelog - 4.32](master/changelog-4.32.md)
* [Device Information](device-information/README.md)
  * [Supported Smartphones](device-information/supported-smartphones.md)
* [Controller Specifications](controller-specifications/README.md)
  * [Physical Controllers](controller-specifications/physical-controllers.md)
  * [Virtual Controller / Virtual Keyboard for JioGlass](controller-specifications/virtual-controller-virtual-keyboard-for-jioglass.md)

## Getting Started

* [Development Platform](getting-started/development-platform.md)
* [Setting Up A Jio Mixed Reality Project in Unity](getting-started/setting-up-a-jio-mixed-reality-project-in-unity.md)
* [URP Support](getting-started/urp-support/README.md)
  * [Setting Up Your Project With URP](getting-started/urp-support/setting-up-your-project-with-urp.md)
  * [Reverting Back to Built-In Render Pipeline](getting-started/urp-support/reverting-back-to-built-in-render-pipeline.md)

## JMRSDK

* [JMRSDK Content](jmrsdk/jmrsdk-content.md)
* [JMRMixedReality Prefab](jmrsdk/jmrmixedreality-prefab.md)
* [System Dock](jmrsdk/system-dock.md)
* [JMRRig](jmrsdk/jmrrig/README.md)
  * [Local Rig](jmrsdk/jmrrig/local-rig.md)
  * [Setting Homepage (Quit functionality)](jmrsdk/jmrrig/setting-homepage-quit-functionality.md)
  * [Recenter Application on Resume](jmrsdk/jmrrig/recenter-application-on-resume.md)

## Develop

* [Editor Emulator](develop/editor-emulator.md)
* [JioGlass Controller Interactions](develop/controller-interactions.md)
* [Cameras](develop/cameras.md)
* [Jio Mixed Reality UI Toolkits](develop/jio-mixed-reality-ui-toolkits.md)
* [Examples](develop/examples.md)

## Interaction

* [Gaze Interaction](interaction/gaze-interaction/README.md)
  * [Gaze and Click](interaction/gaze-interaction/gaze-and-click.md)
  * [Gaze and Dwell](interaction/gaze-interaction/gaze-and-dwell.md)
* [Interaction](interaction/interaction/README.md)
  * [JioGlass Lite Interaction](interaction/interaction/jioglass-lite-interaction.md)
  * [Jio Prism(Holoboard) Interaction](interaction/interaction/jio-prism-holoboard-interaction.md)
  * [Jio Dive Interaction](interaction/interaction/jio-dive-interaction.md)
  * [Pointer Manager](interaction/interaction/pointer-manager/README.md)
    * [Examples](interaction/interaction/pointer-manager/examples.md)
* [Interfaces](interaction/interfaces/README.md)
  * [ISelectHandler](interaction/interfaces/iselecthandler.md)
  * [ISelectClickHandler](interaction/interfaces/iselectclickhandler.md)
  * [IFocusable](interaction/interfaces/ifocusable.md)
  * [ISwipeHandler](interaction/interfaces/iswipehandler.md)
  * [ITouchHandler](interaction/interfaces/itouchhandler.md)
  * [IBackHandler](interaction/interfaces/ibackhandler.md)
  * [IHomeHandler](interaction/interfaces/ihomehandler.md)
  * [IMenuHandler](interaction/interfaces/imenuhandler.md)
  * [IVoiceHandler](interaction/interfaces/ivoicehandler.md)
  * [IFn1Handler](interaction/interfaces/ifn1handler.md)
  * [IFn2Handler](interaction/interfaces/ifn2handler.md)
  * [IManipulationHandler](interaction/interfaces/imanipulationhandler.md)
* [Controller Input Actions](interaction/controller-input-actions/README.md)
  * [Touchpad - Touch](interaction/controller-input-actions/touchpad-touch.md)
  * [Touchpad - Swipe](interaction/controller-input-actions/touchpad-swipe.md)
  * [Source Buttons](interaction/controller-input-actions/source-buttons.md)
  * [Manipulation](interaction/controller-input-actions/manipulation.md)
* [Actions](interaction/actions.md)
* [Device State](interaction/device-state/README.md)
  * [Device Connected](interaction/device-state/device-connected.md)
  * [Device Disconnected](interaction/device-state/device-disconnected.md)
  * [Battery percentage update](interaction/device-state/battery-percentage-update.md)
  * [Scanning for Device](interaction/device-state/scanning-for-device.md)
  * [Battery Percentage](interaction/device-state/battery-percentage.md)

## Voice

* [Voice](voice/voice/README.md)
  * [Speech Events](voice/voice/speech-events.md)
  * [Speech Result](voice/voice/speech-result.md)
  * [Speech Error](voice/voice/speech-error.md)
  * [Speech Session End](voice/voice/speech-session-end.md)
  * [Speech Cancel](voice/voice/speech-cancel.md)
* [Listening](voice/listening.md)

## Tracking

* [Tracking](tracking/tracking/README.md)
  * [Coordinate System](tracking/tracking/coordinate-system.md)
* [Tracking Framework](tracking/tracking-framework/README.md)
  * [TrackerManager Actions](tracking/tracking-framework/trackermanager-actions/README.md)
    * [Get Head Position](tracking/tracking-framework/trackermanager-actions/get-head-position.md)
    * [Get Head Rotation](tracking/tracking-framework/trackermanager-actions/get-head-rotation.md)
    * [Get Head Transform](tracking/tracking-framework/trackermanager-actions/get-head-transform.md)
  * [TrackerManager Methods](tracking/tracking-framework/trackermanager-methods/README.md)
    * [Get Head Position](tracking/tracking-framework/trackermanager-methods/get-head-position.md)
    * [Get Head Rotation](tracking/tracking-framework/trackermanager-methods/get-head-rotation.md)
    * [Get Head Transform](tracking/tracking-framework/trackermanager-methods/get-head-transform.md)
* [Recenter](tracking/recenter.md)

## Building and Testing

* [Building to Target Device](building-and-testing/publishing-to-target-device/README.md)
  * [Merging AndroidManifest](building-and-testing/publishing-to-target-device/androidmanifest-update.md)
  * [Performance Optimization](building-and-testing/publishing-to-target-device/performance-optimization.md)
* [Companion App For Jio Mixed Reality (JMR) Devices](building-and-testing/companion-app-for-jio-mixed-reality-jmr-devices/README.md)
  * [Running the application on Prism (Holoboard)](building-and-testing/companion-app-for-jio-mixed-reality-jmr-devices/running-the-application-on-prism-holoboard.md)
* [IPD Calibration](building-and-testing/ipd-calibration.md)

## Publish

* [Signing App for App Store](publish/signing-apk.md)
* [Publishing to JioGlass Developer Console](publish/publishing-to-jioglass-developer-console.md)
* [Developer Console Analytics](publish/developer-console-analytics.md)

## Capturing and Recording

* [Capture Videos and Screenshots](capturing-and-recording/capture-videos-screenshot-of-bugs/README.md)
  * [Capturing Screenshot/Videos using scrcpy](capturing-and-recording/capture-videos-screenshot-of-bugs/capturing-screenshot-videos-using-scrcpy.md)
  * [Capturing Screenshot/Videos using Vysor](capturing-and-recording/capture-videos-screenshot-of-bugs/capturing-screenshot-videos-using-vysor.md)

## Troubleshooting

* [FAQs - Develop](troubleshooting/faqs-develop.md)
* [FAQs - Building to device](troubleshooting/faqs-building-to-device/README.md)
  * [Gradle](troubleshooting/faqs-building-to-device/gradle.md)
  * [Old aaptOptions error fix](troubleshooting/faqs-building-to-device/old-aaptoptions-error-fix.md)
* [FAQs - Running and Publishing](troubleshooting/faqs-running-and-publishing.md)
* [Laser Point Not Visible](troubleshooting/laser-point-not-visible.md)
