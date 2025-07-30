---
description: JMRSDK v4.57
---

# Jio Mixed Reality SDK Documentation

## Introducing JMRSDK

Welcome to Jio Mixed Reality!

Jio Mixed Reality SDK (JMRSDK) is Jio's mixed reality platform for developing powerful XR experiences. It equips you with various tools that will enable you to build a new digital future.

JMRSDK lets you get started with your application very quickly by setting up most of the things you might require for XR, it ranges from Camera Rig, Controller, Raycast, Interactions, UI toolkit, Recentring, Tracking, and provides much more utility.

## Features

### Input System

We have upgraded the Input System to allow more abstractions between the physical JioGlass controller and the actions developers and users can perform with the objects in the virtual world.

* Controller Ray — You can now use the JioGlass controller to interact directly with objects in 3D by simply pointing the controller towards objects in your scene.
* Select between Head and JioGlass Controller from the **InputManager** prefab to configure the input source.
* Introducing Gaze and Dwell from JMRSDK 4.12.4 onwards for enabling hands-free interactions
* Introducing Gaze and Click from JMRSDK 4.30 onwards for enabling single-click interactions

### Input Actions

Input actions have been decoupled from the Input source, whether you use a JioGlass controller or in the future, voice! This allows the use of multiple input devices to trigger pre-defined actions at the interaction layer without having to recompile/reimport the SDK.

System Actions include:

* Home – Reserved Home interaction
* Back – Reserved Back interaction
* Recenter – Reserved recentering interaction
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
