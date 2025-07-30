---
description: Frequently asked questions related to building to device
---

# FAQs - Building to device

## Android

### # Gradle build failure

Refer to [Gradle](gradle.md)

### # Build failure with Android 14 (API level 34)

<figure><img src="../../.gitbook/assets/image (130).png" alt=""><figcaption></figcaption></figure>

To fix this issue, follow these steps:

1. Download Maven AAPT2 7.2.2 and extract the jar from below\
   [Windows ](https://dl.google.com/android/maven2/com/android/tools/build/aapt2/7.2.2-7984345/aapt2-7.2.2-7984345-windows.jar)[Mac ](https://dl.google.com/android/maven2/com/android/tools/build/aapt2/7.2.2-7984345/aapt2-7.2.2-7984345-osx.jar)[Linux](https://dl.google.com/android/maven2/com/android/tools/build/aapt2/7.2.2-7984345/aapt2-7.2.2-7984345-linux.jar)

{% hint style="warning" %}
Make sure to download the version that corresponds to your build system.
{% endhint %}

2. Open Assets> Plugins> Android> gradleTemplate.properties
3. Add this line in the gradleTemplate.properties file at the end of the file

```
android.aapt2FromMavenOverride=D:/aapt2/aapt2.exe
```

{% hint style="warning" %}
Replace "_D:/aapt2/aapt2.exe"_ with the path where you extracted _aapt2.exe_&#x20;
{% endhint %}

## iOS

### # Mono Screen / Build Failed in iOS

Refer to [FAQ-iOS](faqs-ios.md)
