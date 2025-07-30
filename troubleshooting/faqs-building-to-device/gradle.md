# Gradle

## Gradle Compatability

The following table shows the compatibility between Gradle version and Unity version.

<table><thead><tr><th width="334.3333333333333">Unity version</th><th width="151">Gradle version</th><th>Android Gradle Plugin version</th></tr></thead><tbody><tr><td>2023.1, 2023.2</td><td>7.6</td><td>7.3.1</td></tr><tr><td>2022.2, 2022.3</td><td>7.2</td><td>7.1.0</td></tr><tr><td>2022.1<br>2021.2, 2021.3<br>2021.1 starting from 2021.1.16f1<br>2020.3 starting from 2020.3.15f1</td><td>6.1.1</td><td>4.0.1</td></tr><tr><td>2021.1 up to and including 2021.1.15f1<br>2020.1, 2020.2<br>2020.3 up to and including 2020.3.14f1</td><td>5.6.4</td><td>4.0.1</td></tr><tr><td>2019.4</td><td>5.1.1</td><td>3.4.3</td></tr></tbody></table>

{% embed url="https://docs.unity3d.com/2023.2/Documentation/Manual/android-gradle-overview.html" %}

## Setting the correct Android Gradle Plugin version.

To setup the correct version of the Android Gradle plugin version -

1.  Open baseProjectTemplate.gradle

    <div align="left"><figure><img src="../../.gitbook/assets/ca6ec683-7072-410e-86ac-f71d98253995.jpg" alt=""><figcaption></figcaption></figure></div>
2. Change the version of 'com.android.tools.build.gradle'

<div align="left"><figure><img src="../../.gitbook/assets/d66412fc-6174-4cdf-8869-26e8a5438454.jpg" alt=""><figcaption></figcaption></figure></div>

## Gradle build failure.

While building if you get Gradle Build failure, you will get multiple error logs in the unity console. There can be multiple reasons why you are getting these errors.

{% hint style="info" %}
For getting the reason you need to refer to CommandInvocationFailure in Build failed logs
{% endhint %}

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption><p>CommandInvocationFailure in unity console</p></figcaption></figure>

###

### #1 Error: uses-sdk:minSdkVersion 'x' cannot be smaller than version 26 declared in library

<figure><img src="../../.gitbook/assets/image (68).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
JMRSDK has a dependency on SDK version 26 and hence build will fail when the minimum API version specified in project settings will be smaller than version 26.
{% endhint %}

**Fix:** Make sure that the minimum API level is set to 26 and the target API level is set to 29 or higher.

<figure><img src="../../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>



### #2 Error: Could not get unknown property 'vstsMavenAccessToken' for Credentials \[username: tesseractimg].

<figure><img src="../../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
There are dependencies of the Gradle properties template on the base Gradle template.&#x20;
{% endhint %}

**Fix:** Make sure to select all the publishing build settings correctly as shown in the image below.

<figure><img src="../../.gitbook/assets/image (70).png" alt=""><figcaption></figcaption></figure>



### #3 Error: Keystore passwords incorrect

<figure><img src="../../.gitbook/assets/image (17).png" alt=""><figcaption><p>Project Keystore incorrect</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (21).png" alt=""><figcaption><p>Project Key password was incorrect</p></figcaption></figure>



{% hint style="warning" %}
This document does not cover manifest merger failure due to multiple manifest files injected due to third-party plugins.
{% endhint %}
