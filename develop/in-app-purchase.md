# In-app purchase

In-app purchases (IAP) are now a pivotal feature in our apps, providing a great way to enhance user experience and generate revenue. With IAP, consumers can buy additional content, features, or services directly within the app, making their experience more engaging and personalized. This feature helps developers offer more value to users while creating new income streams through one-time purchases, subscriptions, or consumables. Integrating IAP allows apps to stay competitive, innovative, and financially sustainable.

### In-app purchases in JMR applications

## Integrating IAP

To integrate IAP into your application, follow these steps.

### 1. Modify android manifest:    &#x20;

Apps made with JMRSDK are shown in the JioImmerse app drawer, where the application launches in MR mode. Native popups cannot be displayed on split-screen. To show native popups we must show the application in mono screen mode from Android Launcher. Modify the Android manifest to show the application in the Android launcher. &#x20;

Uncomment / Add this intent in `Android Manifest` file along with the `intent-filter` for `MR-LAUNCHER`

```xml
<intent-filter>
        <action android:name="android.intent.action.MAIN" />
        <category android:name="android.intent.category.LAUNCHER" />
</intent-filter>
```

<figure><img src="../.gitbook/assets/image (132).png" alt=""><figcaption><p>Android Manifest after modification</p></figcaption></figure>

### 2. Creating an IAP Store:

To create an IAP store, make a scene in your project.&#x20;

{% hint style="danger" %}
* The IAP store scene should be in portrait orientation
* Do NOT configure this scene for JioMixedReality
{% endhint %}

* Camera - Setup a Camera from GameObject > Camera. Tag this camera as MainCamera.
* In the IAP store scene, add a Button that says - Open JioImmerse. This button shall trigger the functionality as shown in point 4 below.
* In this scene, utilize [`com.unity.purchasing`](https://docs.unity3d.com/Packages/com.unity.purchasing@4.11/manual/index.html) package provided by Unity to implement in-app purchases in your application through Google Play Billing. Get creative in how you want to showcase in-app purchases to attract the most consumers.&#x20;

### 3. Handling intents to open the IAP store of your application:

* Once, the application is opened/resumed from the Android launcher, it should quickly switch to the Shop scene in portrait orientation.
* If the application is minimized while in the IAP store, we quit the application, this keeps the application ready to be opened from either of the launchers. However, we do NOT`quit` when a transaction is in progress to prevent purchases from failing.

Here is a sample script that does the same, attach this to the first scene of your application.

* Modify the `shopSceneIndex` to the index of the shop scene as present in build settings.
* Change `isPurchasing` to true while any purchase is in progress.

```csharp
using System;
using System.Linq;
using UnityEngine;
using UnityEngine.SceneManagement;

public class SceneStartManager: MonoBehaviour
{
    private static SceneStartManager instance;
    public int shopSceneIndex = 5;    //Modify this
    public bool isPurchasing = false; //Modify this when purchase is in progress
    
    private void Awake()
    {
        if (instance == null)
        {
            instance = this;
            DontDestroyOnLoad(gameObject);
            CheckIntentAndLoadScene();
        }
        else Destroy(gameObject);
    }

    private void OnApplicationPause(bool pauseStatus)
    {
        if (!pauseStatus) CheckIntentAndLoadScene();
        else if (SceneManager.GetActiveScene().buildIndex == shopSceneIndex && !isPurchasing) Application.Quit();
    }

    private string[] categoryArray = Array.Empty<string>();
    private void CheckIntentAndLoadScene()
    {
        AndroidJavaClass unityPlayer = new AndroidJavaClass("com.unity3d.player.UnityPlayer");
        AndroidJavaObject currentActivity = unityPlayer.GetStatic<AndroidJavaObject>("currentActivity");

        AndroidJavaObject intent = currentActivity.Call<AndroidJavaObject>("getIntent");
        AndroidJavaObject categories = intent.Call<AndroidJavaObject>("getCategories");

        categoryArray = categories != null ? categories.Call<string[]>("toArray", new object[] {Array.Empty<string>()}) : Array.Empty<string>();

        if (categoryArray.Contains("android.intent.category.LAUNCHER")) LoadScene(shopSceneIndex);
    }
    private void LoadScene(int sceneIndex)
    {
        if (SceneManager.GetActiveScene().buildIndex != sceneIndex) 
        {
            SceneManager.LoadScene(sceneIndex);
            Screen.orientation = ScreenOrientation.Portrait;
        }
    }
}
```

### 4. Adding an open JioImmerse button:

Make sure to add a button called `Open JioImmerse` at the bottom of the screen and invoke this functionality when pressed.

```csharp
public void OpenJioImmerse()
{
#if UNITY_ANDROID && !UNITY_EDITOR
	AndroidJavaClass unityPlayer = new AndroidJavaClass("com.unity3d.player.UnityPlayer");
	AndroidJavaObject currentActivity = unityPlayer.GetStatic<AndroidJavaObject>("currentActivity");
	AndroidJavaObject packageManager = currentActivity.Call<AndroidJavaObject>("getPackageManager");
	AndroidJavaObject intent = packageManager.Call<AndroidJavaObject>("getLaunchIntentForPackage", "com.jiotesseract.mr.jxr");

	if (intent != null) currentActivity.Call("startActivity", intent);
	else
	{
		Application.OpenURL("https://play.google.com/store/apps/details?id=com.jiotesseract.mr.jxr");
		Debug.Log("App not installed");
	}
#endif
}
```

<figure><img src="../.gitbook/assets/image (133).png" alt=""><figcaption><p>Sample shop screen</p></figcaption></figure>
