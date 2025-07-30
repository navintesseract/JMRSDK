# Listening

| Method          | Description         |
| --------------- | ------------------- |
| StartListening  | To start listening  |
| CancelListening | To cancel listening |
| StopListening   | To stop listening   |

## **How to start listening**

> public void StartListening();

To listening need to call StartListening() method exposed by VoiceManage&#x72;**.**

```csharp
using UnityEngine;
using JMRSDK;

public class JMRDemoVoiceExample : MonoBehaviour
{
    public void StartListening()
    {
        // added editor check as this can’t feature can’t tested in editor
        if (!Application.isEditor)
            JMRVoiceManager.Instance.StartListening();
    }

    public void CancelListening()
    {
        if (!Application.isEditor)
            JMRVoiceManager.Instance.CancelListening();
    }
}
```

## **How to Stop listening**

> public void StopListening();

To listening need to call StopListening() method exposed by VoiceManage&#x72;**.**

```csharp
using UnityEngine;
using JMRSDK;

public class JMRDemoVoiceExample : MonoBehaviour
{
    public void StopListening()
    {
        // added editor check as this can’t feature can’t be tested in	editor
        if (!Application.isEditor)
            JMRVoiceManager.Instance.StopListening();
    }
}
```

## **How to Cancel listening**

> public void CancelListening();

To listening need to call CancelListening() method exposed by the VoiceManager.

```csharp
using UnityEngine;
using JMRSDK;

public class JMRDemoVoiceExample : MonoBehaviour
{
    public void CancelListening()
    {
        // added editor check as this can’t feature can’t be tested in the editor
        if (!Application.isEditor)
            JMRVoiceManager.Instance.CancelListening();
    }
}
```
