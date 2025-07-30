---
description: Action to detect Speech Session end
---

# Speech Session End

> public void OnSpeechSessionEnd (long ts)

| Parameter | Description                 |
| --------- | --------------------------- |
| ts        | The speech session end time |

To detect Speech session end, you need to implement callback method exposed through the VoiceManager:&#x20;

OnSpeechSessionEnd (long ts)

{% hint style="info" %}
Action will be called only when it’s subscribed to a method. Action must be subscribed to the method with a matching signature.
{% endhint %}

```csharp
using UnityEngine;
using JMRSDK;

public class JMRDemoVoiceExample : MonoBehaviour
{
    private void OnEnable()
    {
        JMRVoiceManager.OnSpeechSessionEnd += OnSpeechSessionEnd;
    }

    private void OnDisable()
    {
        JMRVoiceManager.OnSpeechSessionEnd -= OnSpeechSessionEnd;
    }

    private void OnSpeechSessionEnd(long ts)
    {
        string spEndTime = ts.ToString();
    }
}
```
