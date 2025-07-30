# Interaction

## Introduction to Interaction

Interactions are defined as how the user interacts with the content in the JioGlass. Interactions in the Mixed Reality space are done differently than how we are used to in current mobile devices. Having the ability to interact with content brings a new sphere of immersive for the users to experience. The various form of interactions includes – controller interaction, hand interaction, and eye-gaze interaction. Interactions in the current environment of JMRSDK are done using the JioGlass Controller. The controller must be successfully connected. If the controller gets disconnected user needs to scan and connect to the nearby controller to have a smooth experience. The JMR Interaction Manager handles the core functionalities of verifying connection, disconnection of the controller, returning its battery percentage, and scanning for controllers if disconnected.

## Interaction

Interaction is responsible for managing all swipe, touch, select, and click events.

## InputManager

The input Manager is responsible for managing input sources and dispatching relevant events to the appropriate input handlers.

![](<../../.gitbook/assets/image (98).png>)

