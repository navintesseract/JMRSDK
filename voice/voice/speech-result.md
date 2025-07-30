---
description: Action to get speech result
---

# Speech Result

> public void OnSpeechResults (String jsonResult, long timestampNs)
>
> public void OnSpeechPartialResults (String jsonResult, long timestampNs)

| Parameters  | Description                    |
| ----------- | ------------------------------ |
| jsonResult  | Speech result in json format   |
| timestampNs | Speech time stamp result in NS |

To get the speech result at runtime need to implement OnSpeechResults (string obj, long ts) and OnSpeechPartialResults (string obj, long ts) exposed through VoiceManager -this callback gives JSON result and timeStamps.

```csharp
using UnityEngine;
using JMRSDK;

public class JMRDemoVoiceExample : MonoBehaviour
{
    private void OnEnable()
    {
        JMRVoiceManager.OnSpeechResults += SpeachResult;
        JMRVoiceManager.OnSpeechPartialResults += SpeechPartialResult;
    }

    private void OnDisable()
    {
        JMRVoiceManager.OnSpeechResults -= SpeachResult;
        JMRVoiceManager.OnSpeechPartialResults -= SpeechPartialResult;
    }

    private void SpeachResult(string obj, long ts)
    {
        long timeStamp = ts;
        string spResult = obj;
    }

    private void SpeechPartialResult(string obj, long ts)
    {
        long timeStamp = ts;
        string spResult = obj;
    }
}
```
