---
description: >-
  This is the new Addition, through this you can quit your applications now in
  the JioGlass, JioPrism and JioDive.
---

# Setting Homepage (Quit functionality)

Enable this checkbox so that a quit menu popup appears when the user presses the back button. You can enable or disable this whenever required to maintain the app journey.

On the Home page of the application, please enter via script:

```
JMRRigManager.Instance.setHomePage = true;
```

Example implementation exposing a function to setup the home page.\
Using this code it is possible to call Set Home Page whenever you want in the application.

```csharp
using System.Collections;
using JMRSDK;
using UnityEngine;

public class JMRHomePage : MonoBehaviour
{
    public void SetHomePage(bool enable)
    {
        StartCoroutine(SetWithDelay(enable));
    }

    IEnumerator SetWithDelay(bool enable)
    {
        yield return null;
        JMRRigManager.Instance.setHomePage = enable;
    }
}
```
