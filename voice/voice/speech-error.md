---
description: Action to detect Speech error
---

# Speech Error

> public void OnSpeechError (string err)

| Parameter | Description            |
| --------- | ---------------------- |
| err       | The error that occured |

To detect Speech error, you need to implement three callback methods exposed through the VoiceManager:&#x20;

OnSpeechEvent (string err)

{% hint style="info" %}
Action will be called only when it’s subscribed to a method. Action must be subscribed to the method with a matching signature.
{% endhint %}

```csharp
using JMRSDK;
using UnityEngine;

public class JMRDemoVoiceExample : MonoBehaviour
{
    private void OnEnable()
    {
        JMRVoiceManager.OnSpeechError += SpeechError;
    }

    private void OnDisable()
    {
        JMRVoiceManager.OnSpeechError -= SpeechError;
    }

    private void SpeechError(string err)
    {
        string spError = err;
    }
}
```
