---
description: Gradle required with JMRSDK is Gradle 6.1.1
---

# Gradle

You can download gradle 6.1.1 from [here](https://gradle.org/next-steps/?version=6.1.1\&format=all).



## Gradle build failure.

While building if you get Gradle Build failure, you will get multiple error logs in the unity console. There can be multiple reasons why you are getting these errors.

{% hint style="info" %}
For getting the reason you need to refer to CommandInvocationFailure in Build failed logs
{% endhint %}

<figure><img src="../../.gitbook/assets/image (56).png" alt=""><figcaption><p>CommandInvocationFailure in unity console</p></figcaption></figure>

###

### #1 Error: uses-sdk:minSdkVersion 'x' cannot be smaller than version 26 declared in library

<figure><img src="../../.gitbook/assets/image (59).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
JMRSDK has a dependency on SDK version 26 and hence build will fail when the minimum API version specified in project settings will be smaller than version 26.
{% endhint %}

**Fix:** Make sure that the minimum API level is set to 26 and the target API level is set to 29 or higher.

<figure><img src="../../.gitbook/assets/image (49).png" alt=""><figcaption></figcaption></figure>



### #2 Error: Could not get unknown property 'vstsMavenAccessToken' for Credentials \[username: tesseractimg].

<figure><img src="../../.gitbook/assets/image (52).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
There are dependencies of the Gradle properties template on the base Gradle template.&#x20;
{% endhint %}

**Fix:** Make sure to select all the publishing build settings correctly as shown in the image below.

<figure><img src="../../.gitbook/assets/image (62).png" alt=""><figcaption></figcaption></figure>



### #3 Error: Keystore passwords incorrect

<figure><img src="../../.gitbook/assets/image (61).png" alt=""><figcaption><p>Project Keystore incorrect</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (53).png" alt=""><figcaption><p>Project Key password was incorrect</p></figcaption></figure>



{% hint style="warning" %}
This document does not cover manifest merger failure due to multiple manifest files injected due to third-party plugins.
{% endhint %}
