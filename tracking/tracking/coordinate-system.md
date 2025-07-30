# Coordinate System

## C**oordinate System**

The mathematical term ‘coordinate system’ describes a way of using numbers to specify the location of a point (or points) in 2D or 3D space. In a game engine, it’s the coordinate system’s role to define both the location of each object and which direction it is facing. With this dat&#x61;**,** you can calculate the distance between objects, rotation, velocity, and all sorts of other useful information.

{% hint style="success" %}
There are multiple systems for calculating and interpreting coordinates. By default, Unity uses (and expects you to use) a Cartesian coordinate system, which is the basis for what we discuss in this guide. However, converting between other systems is possible using C# (and a whole lot of calculation!). That said, no matter which system you’re working with, the information within this guide should remain relevant.
{% endhint %}

## **Plotting your position**

The most important point to remember (and if you take nothing else from this guide – let it be this!) is that the virtual space inside your Unity scene is determined by three axes – X, Y, and Z. They represent the left/right, up/down, and forward/back directions respectively.

Each object in your game world has a value for each axis, the three of which, when combined, tell Unity where to place it in the scene. Should you change your object’s Y value, for example, your object will move up or down. The direction of the motion will depend on whether you add or subtract from the axis’s value. This is what we’d call ‘moving in the Y-axis.\
\
The point at which all three axes intersect is called the origin. On one side of the origin, and axis value will be in positive numbers, and on the othe&#x72;**,** it will be negative. This means a value of zero is right on the origin, and a value of 8 will be the mirror of a value of -8.

The positive direction of each axis is also commonly called the forward vector (z-axis), right vector (x-axis), and up vector (y-axis).

## **Y-Up or Z-Up, why does it matter?**

This is the first key point of difference where Unity may not match the other software you’re using to make your art. Some 3D packages, like Blender, have defined (at least by default) the positive Z-axis as their up vector.

As you might expect, this can cause unexpected results when transferring 3D objects between programs. Changing the definition of an axis (in this instance, moving the up axis from Z to Y) will fundamentally change how that data is interpreted. Things tend to go sideways on you!

## **The difference between left and right-handed systems**

The second important distinction between Unity and some other commonly used engines and packages is that Unity uses a left-handed coordinate system. What this means is that the &#x58;**-**&#x61;xis (which defines your right vector) is inverted when brought into a program that uses a right-handed system.\
\
The easiest way to visualize is to use your hand. Hold it with your palm facing to your side as if you’re reaching to shake someone’s hand. Point your thumb upwards (like a thumbs-up), this is your up vector (Y+). Point your index finger forward, this (unsurprisingly) is your hand’s forward vector (Z+). Finally, curl your middle finger so it points perpendicular to your palm – this is your hand’s right vector (X+).\
\
If you did this exercise with your left hand, then you will be aligned with Unity’s coordinate system – your right vector will be pointing to the right. Instead, if you use your right hand (as Maya does, for example) it will be pointing to the left. This is the difference between left-handed and right-handed systems.

The most common issue that this inverse left/right situation causes is that art assets imported into Unity from right-handed 3D programs will be flipped in their X-axis, as their right vector will be pointing the other way. Just something to keep in mind.

## **World (or Universal) space**

World space is the coordinate system for the scene itself. Its origin is in the center of your scene, and it is to world space that the grid in the editor viewport aligns. You cannot change the direction of this coordinate system. In world space, Y+ is always up, X+ is always right, and Z+ is always forward.

## **Local (or Relative) space**

Local space is a coordinate system that is relative to the rotation of a specific object. Its origin is at the pivot point of the object itself, and its axes will change depending on which direction it is facing.

You can think of an object’s local space like its point of view. If your object is upside down, then its relative up axis (still positive Y for the object) would point downwards in world space, but upwards relative to the object. It’s like our hand example from earlier – if you rotate your wrist, all the local axes (represented by your fingers) will follow.

You can switch your transform tool between coordinate systems by pressing the Toggle Tool Handle Rotation button in the top left of the editor, or by pressing its hotkey ‘x’.

{% hint style="success" %}
_One important thing to keep in mind is that the transform values in the inspector may not reflect the active coordinate system of your transform tool. If your object is a child of another object, those values will be in local space, and relative to its parent. Likewise, if it is not a child, the values will be in world space, regardless of your transform tool’s settings._
{% endhint %}
