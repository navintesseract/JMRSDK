---
description: This error pops up when using JMRSDK with Unity 2020 or higher.
---

# Old aaptOptions error fix

If you got an error related to the old aaptOptions while making the build like this. Here is the fix:

<figure><img src="../../.gitbook/assets/Unity_ilt0Cy1oq7.png" alt=""><figcaption></figcaption></figure>

Find the "mainTemplate" file inside your project window Assets->Plugins->Android

<figure><img src="../../.gitbook/assets/Unity_qKJMozHa61.png" alt=""><figcaption></figcaption></figure>

Open "mainTemplate.gradle" using notepad and add line&#x20;

"noCompress = \['.ress', '.resource', '.obb'] + unityStreamingAssets.tokenize(', ')"

&#x20;under the heading "aaptOptions" as highlighted in the screenshot

<figure><img src="../../.gitbook/assets/notepad++_JNB5gz7JmG.png" alt=""><figcaption></figcaption></figure>
