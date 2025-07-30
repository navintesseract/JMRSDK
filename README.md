---
description: JMRSDK-Beta v4.27.10
---

# Tesseract Mixed Reality SDK Documentation

## Introducing JMRSDK

Welcome to Jio Mixed Reality!

Jio Mixed Reality SDK (JMRSDK) is Jio's Mixed Reality Platform for developing powerful XR experiences by equipping you with a variety of tools that will enable you to build a new digital future.

## Features

You will find the following features in the latest release -&#x20;

### Universal Render Pipeline

We are happy to announce compatibility with Unity's Universal Render Pipeline to help you show off your gorgeous level designs and bring the overall graphic quality to a whole new level!

### UI Toolkits

To make the Jio Mixed Reality interface consistent and easy for developers to build upon, we have introduced drag-n-drop UI toolkits that can be easily configured to suit their needs while adhering to their brand guidelines.

* Colour System – Allowing developers to customize the colours of the toolkits from the menu bar.
* Icon System – Allowing developers to change icons and text from inspector without disturbing alignment, font, and size on each toolkit
* Toolkits **-**
  * Canvas
  * Button
  * Check Box&#x20;
  * Check Box Group
  * DialogBox
  * Error DialogBox
  * Drop Down
  * Image View
  * Progressbar
  * Radio Button
  * Radio Button Group
  * Horizontal Scroll
  * Vertical Scroll
  * Search Field (With Keyboard integrated)
  * Slider
  * Toggle Button
  * Tool Tip
  * Input Field (With Keyboard integrated)
  * VideoPlayer
  * Voice Toolkit

### Input System

We have upgraded the Input System to allow more abstractions between the physical JioGlass controller and the actions that developers and users can perform with the objects in the virtual world.

* Controller Ray – You can now use the JioGlass controller to directly interact with objects in 3D by simply pointing the controller towards objects in your scene.
* Select between Head and JioGlass Controller from **InputManager** prefab to configure the input source.
* Introducing Gaze and Dwell from JMRSDK 4.12.4 onwards for enabling hands-free interactions

### Input Actions

Input actions have been decoupled from the Input source, whether you use a JioGlass controller or in-future, voice! This allows the use of multiple input devices to trigger pre-defined actions at the interaction layer without having to recompile/reimport the SDK.

System Actions include:

* Home – Reserved Home interaction
* Back – Reserved Back interaction
* Menu – Reserved Menu interaction for invoking in-app menus. Coming Soon!
* Recenter – Reserved recentering interaction
* IPD Calibration – Reserved IPD Calibration toggle.
* Standard Interaction Actions include:
  * Focus
  * Select
  * Swipe Up
  * Swipe Down
  * Swipe Right
  * Swipe Left
* Additional option to configure manipulation and hold events to manipulate objects. The **manipulation** class allows developers to use the following actions on 3D objects:
* Grab
* Rotate
* Scale
* Move Along Ray

### Editor Emulator

We have upgraded the editor emulator to allow you to use the keyboard and mouse to have a more natural way of interacting with objects in the JioGlass Mixed Reality environment.

## Analytics

Application analytics have now been released JMRSDK 4.12.4 onwards to track usage of applications on the Jio Mixed Reality platform
