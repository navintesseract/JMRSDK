---
description: Running your application on Android
---

# Running your application

## Android

To run your application on Android you need to install a **Companion App.**

There are 2 types of Companion Apps -&#x20;

1. DemoXR&#x20;

DemoXR companion app allows you to run your application with the Debug and Production keys. It is intended for developers.

2. JioImmerse

JioImmerse companion app allows you to run your application with the Production key and is intended for consumers.

| Features           | DemoXR     | JioImmerse |
| ------------------ | ---------- | ---------- |
| Debug Key          | ✅          | ❌          |
| Production Key     | ✅          | ✅          |
| Intended for       | Developers | Consumers  |
| JioVerse App store | ✅          | ✅          |

{% hint style="info" %}
As a developer, you should use **DemoXR** as it will allow you to use the Debug key as well as the production key.
{% endhint %}

JMRSDK apps are not visible by default in the Android Launcher. It is only visible in the MR Launcher present in the Companion apps. Refer to [Merging Android Manifest](../publishing-to-target-device/androidmanifest-update.md).
