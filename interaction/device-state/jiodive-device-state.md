# JioDive Device State

To detect if a person is wearing JioDive or not, JMRSDK provides a method, that works on the principle that there is slight motion when JioDive is worn by a person.&#x20;

{% hint style="warning" %}
This function is expensive, may impact heavily on performance, and should be used with caution.
{% endhint %}

To use this function call this method:

```csharp
JMRTrackerManager.Instance.DiveGyroStatus();
```

Then subscribe to action callbacks to receive the response:

```csharp
JMRTrackerManager.IdleDive += IdleDive;
JMRTrackerManager.UsingDive += UsingDive;
```

This function will keep running the callbacks for 5 seconds every frame.

Example Code

<pre class="language-csharp"><code class="lang-csharp">using JMRSDK.InputModule;
using UnityEngine;

public class JMRDemoInteractionExample : MonoBehaviour
{  
<strong>    void Start()
</strong>    {
        JMRTrackerManager.Instance.DiveGyroStatus();
        JMRTrackerManager.IdleDive += IdleDive;
        JMRTrackerManager.UsingDive += UsingDive;
    }
    
    void IdleDive()
    {
        Debug.Log("Idle State");
    }
    
    void UsingDive()
    {
        Debug.Log("Used State");
    }
}
</code></pre>
