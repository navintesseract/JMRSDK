---
description: Action to detect Speech cancel
---

# Speech Cancel

> public void OnSpeechCancelled (string reason, long ts)

| Parameter | Description                                    |
| --------- | ---------------------------------------------- |
| reason    | The reason for the speech session cancellation |
| ts        | The timestamp                                  |

To detect Speech session end, you need to implement callback method exposed through the VoiceManager: (string reason, long timeStamps)

{% hint style="info" %}
Action will be called only when it’s subscribed to a method. Action must be subscribed to the method with a matching signature
{% endhint %}

```csharp
using UnityEngine;
using JMRSDK;

public class JMRDemoVoiceExample : MonoBehaviour
{
    private void OnEnable()
    {
        JMRVoiceManager.OnSpeechCancelled += SpeechCancelled;
    }

    private void OnDisable()
    {
        JMRVoiceManager.OnSpeechCancelled -= SpeechCancelled;
    }

    private void SpeechCancelled(string reason, long ts)
    {
        string spCancelReason = reason;
        long timeStamp = ts;
    }
}
```
