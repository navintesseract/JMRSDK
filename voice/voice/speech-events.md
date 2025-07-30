---
description: Action to get Speech Events
---

# Speech Events

> public void OnSpeechEvent (SpeechEvent speechEvent, long timeStamp)

| speechEvent | The speech event         |
| ----------- | ------------------------ |
| timeStamp   | Speech time stamp result |

To monitor speech events, you need to implement callback method exposed through the VoiceManager:&#x20;

OnSpeechEvent (JMRVoiceManager.SpeechEvent obj, long ts)

{% hint style="info" %}
Action will be called only when it’s subscribed to a method. Action must be subscribed to a method with a matching signature.
{% endhint %}

```csharp
using UnityEngine;
using JMRSDK;

public class JMRDemoVoiceExample : MonoBehaviour
{
    private void OnEnable()
    {
        JMRVoiceManager.OnSpeechEvent += SpeechEvent;
    }

    private void OnDisable()
    {
        JMRVoiceManager.OnSpeechEvent -= SpeechEvent;
    }

    private void SpeechEvent(JMRVoiceManager.SpeechEvent obj, long ts)
    {
        string spEvents = obj.ToString();
    }
}
```
